# Feature request: Optional inline expansion mode for bookmarks-bar folders (“Slides”)

**Suggested area:** Browser UI / Bookmarks Bar (component subject to Chromium triage)  
**Request type:** Feature

## Problem

Bookmarks-bar folders currently open as vertical menus. That's helpful for browsing larger collections but less efficient for groups of links repeatedly accessed throughout the day. Pinning every frequently used link directly to the bar causes clutter.

## Proposal

Introduce an optional per-folder **display preference**: `dropdown` (current/default behavior) or `slide`.

For a folder displayed as a Slide:

1. Clicking its toolbar control expands the folder's immediate bookmark children as **inline bookmarks**, immediately following the folder.
2. Subsequent items are reflowed using native bookmarks-bar layout and overflow handling.
3. Clicking the same Slide collapses *only* that folder.
4. Expanded state is independent: multiple Slides may remain open concurrently.
5. Existing bookmarks and folders, their order, and the bookmark data model remain unchanged.
6. Folder context menus let users switch between Slide and Dropdown presentation.

## Design questions

- Preserve keyboard access, focus handling, screen-reader semantics, and drag-and-drop behavior.
- Reuse existing overflow affordances rather than adding a second row.
- Decide whether open/closed states belong to the window or user profile and whether they persist across sessions.
- Continue using standard dropdown behavior for nested folders where appropriate.

## Interactive proof of concept

This independent HTML/JavaScript demonstration illustrates the proposed UX inside simulated browser chrome. It does **not** modify Chromium or read real bookmarks.

- **Interactive demo:** [Try Bookmark+](https://ashcraig.com/bookmarkplus/)
- **Source repository:** [Bookmark+ on GitHub](https://github.com/theashcraig/bookmark-plus)
- **Walkthrough video:** [Watch the walkthrough on the demo site](https://ashcraig.com/bookmarkplus/#walkthrough)

The simulation lets reviewers interact with multiple independently expanded Slides, standard dropdown folders, and the optional per-folder display preference.
