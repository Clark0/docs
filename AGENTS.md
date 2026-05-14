# Repository Guidelines

## Project Structure & Module Organization

This repository is a Markdown knowledge base for algorithm notes, intended to work well in Obsidian and plain Git.

- `算法笔记/` contains current curated notes and problem lists, such as `如何科学刷题.md`, `题单-DP.md`, and `题单-Data Structure.md`.
- `archive notes/` stores older topic notes grouped by numbered categories, for example `01-基础/`, `02-数据结构/`, `04-动态规划/`, and `07-字符串/`.
- `Clippings/` stores imported web clippings. Keep original source titles when preserving imported content.
- `.obsidian/` contains local Obsidian configuration; avoid committing workspace or theme noise covered by `.gitignore`.

Place new algorithm notes under the most specific topic directory. Use Chinese topic names already present in the repo when possible.

## Build, Test, and Development Commands

There is no package build or automated test suite. Validate changes with lightweight repository checks:

- `git status --short` shows staged, modified, deleted, and untracked files.
- `rg --files -g '*.md'` lists Markdown notes and helps verify placement.
- `rg "keyword" 算法笔记 "archive notes"` searches existing terminology before adding duplicate material.

Preview edited notes in Obsidian or a Markdown renderer before committing, especially when changing tables, links, or math.

## Coding Style & Naming Conventions

Write notes in Markdown with `#` headings, short paragraphs, bullet lists, and fenced code blocks where examples are useful. Keep existing Chinese naming conventions for directories and files, such as `05-图论/LCA.md` or `02-数据结构/线段树.md`.

Use relative Markdown links for internal references. Preserve spaces in existing filenames, but prefer concise names for new files. Keep mathematical notation readable in Markdown using inline `$...$` or block `$$...$$` syntax.

## Testing Guidelines

For documentation changes, test by rendering. Check that headings create a usable outline, tables align correctly, formulas render, and internal links point to existing files. For copied or clipped content, confirm source links are still present and attribution is clear.

## Commit & Pull Request Guidelines

Recent commits use short imperative messages such as `add prefix sum` and `update balanced tree`. Follow that style: concise, lowercase is acceptable, and name the topic changed.

Pull requests should include a brief summary, affected folders, and screenshots only when rendering changes are hard to review from Markdown alone. Link related issues or source materials when adding problem lists or copied references.

## Agent-Specific Instructions

Do not reorganize large note trees unless asked. Preserve user edits and Obsidian metadata. Avoid introducing generated assets or build tooling unless the repository explicitly needs them.

When helping with algorithm problems, prefer guided reasoning over giving the full solution immediately. Start with the core model, invariants, data structure choice, or a small example; ask or prompt the next step when the user is exploring. Provide full code only when the user explicitly asks for an implementation, submits code for review, or is clearly blocked after the guided hints.

### Daily Problem Planning

When the user says `start my day`, update `算法笔记/每日题单.md` instead of creating a new planning file. Query the current LeetCode daily challenge first and put it as item `0` in 今日题目. Then choose a small set of follow-up problems based on current checked progress in the local topic lists, prioritizing recent unfinished items, common data structures, DP continuity, and weekly-contest-relevant patterns.

Keep the daily list modest: usually one daily challenge plus three mainline problems and, when useful, one or two DP or contest-skill problems. Prefer core problems with difficulty `<=1700` for a topic, but do not mechanically clear an entire list. Avoid repetitive template drills; pick representative variants that are worth reviewing.

Overwrite `算法笔记/每日题单.md` for the new date, preserving its simple structure: frontmatter, 今日题目, 今日主线, 复盘, 更新 Prompt, and 更新规则. If problems from yesterday or today are already complete, mark them checked. When the user says the day is done, mark completed items in 今日题目 and also check the matching entries in the relevant topic lists such as `题单-Data Structure.md`, `题单-DP.md`, or `题单-Grid.md`. Leave unfinished carry-over items unchecked.
