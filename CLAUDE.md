# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

A small learning repo from Week 1 of Claude Code Mastery (topics: Terminal, Git, Claude Code). It has no build system, package manager, linter or tests.

## Running the code

- `todo.html` is a self-contained to-do app (inline CSS and vanilla JS, no dependencies). Open it directly in a browser, for example `xdg-open todo.html`.
- `index.html` is a separate Hello World page.
- `scripts/hello.sh` is a practice shell script.

## todo.html architecture

- State is a single `tasks` array of `{id, text, done}`. Every change calls `save()` and then `render()`, and `render()` rebuilds the whole `<ul id="task-list">`.
- Persistence uses `localStorage` under the key `todo-tasks`. Both `load()` and `save()` are wrapped in try/catch so the page still works when storage is unavailable.
- Task text is set with `textContent`, never `innerHTML`, to avoid HTML injection. Keep it that way when editing.

## Other files

`notes/`, `practice/`, `day1.txt`, `my-notes.txt` and `notes-copy` are learning notes and terminal-practice artifacts, not application code.

## Git

Work happens directly on `main`, pushed to `origin` on GitHub. Commit messages are short imperative summaries (for example "Add to-do list app").
