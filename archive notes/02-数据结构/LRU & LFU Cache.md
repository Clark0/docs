# LRU cache
https://leetcode.com/problems/lru-cache/

maintain an LRU doubly linked list, insert front and pop back

```cpp
struct Node {
	int k, v;
};

unordered_map<int, list<Node>::iterator> key_to_iter;
list<Node> lru_list;
int capacity;

int get(int key) {
	auto it = key_to_iter.find(key);
	if (it == key_to_iter.end())
		return -1;
	
	auto & node = it->second;
	lru_list.splice(lru_list.begin(), lru_list, node);
	return node->v;
}

void put(int key, int value) {
	auto it = key_to_iter.find(key);
	if (it != key_to_iter.end()) {
		auto & node = it->second;
		node->v = value;
		lru_list.splice(lru_list.begin(), lru_list, node);
		return;
	}
	
	lru_list.emplace_front(key, value);
	key_to_iter[key] = lru_list.begin();
	if (key_to_iter.size() > capacity) {
		key_to_iter.erase(lru_list.back().k);
		lru_list.pop_back();
	}
}
```


# LFU Cache

https://leetcode.com/problems/lfu-cache/description/

1. `frequency_to_list`: Maps frequency count to a LRU list with that frequency.
2. `key_to_iter`: Maps key to iterator in the corresponding frequency list.
- Tracks `min_freq` to quickly find the least frequently used nodes.

```cpp
struct Node {
    int k, v, freq;
};

int capacity = 0;
int min_freq = 0;
unordered_map<int, std::list<Node>> frequency_to_list;
unordered_map<int, std::list<Node>::iterator> key_to_iter;

void move(std::list<Node>::iterator it) {
    int freq = it->freq;
    auto& source = frequency_to_list[freq];
    auto& target = frequency_to_list[freq + 1];
    source.splice(target.begin(), target, it);
    it->freq++;

    if (min_freq == freq && source.empty())
        min_freq++;
}

int get(int key) {
    auto it = key_to_iter.find(key);
    if (it == key_to_iter.end())
        return -1;

    move(it->second);
    return it->second->v;
}

void put(int key, int value) {
    auto it = key_to_iter.find(key);
    if (it != key_to_iter.end()) {
        it->second->v = value;
        move(it->second);
        return;
    }

    if (key_to_iter.size() == capacity) {
        key_to_iter.erase(frequency_to_list[min_freq].back().k);
        frequency_to_list[min_freq].pop_back();
    }

    frequency_to_list[1].emplace_front(key, value, 1);
    key_to_iter[key] = frequency_to_list[1].begin();
    min_freq = 1;
}
```