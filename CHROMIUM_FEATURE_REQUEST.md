# Feature request: Optional inline expansion mode for bookmarks-bar folders (“Slides”)

**Suggested component:** UI > Browser > TopChrome > BookmarksBar (subject to Chromium triage)
**Type:** Feature Request

## Problem

The existing bookmarks-bar folder interaction uses a vertical dropdown. This is efficient for occasional browsing of large collections, but adds a menu-navigation step for small groups of links used frequently across contexts. Displaying every frequently used bookmark directly on the bar leads to clutter.

## Proposal

Introduce an optional per-folder toolbar **display mode**: `dropdown` (default/current behavior) or `slide`.

For folders displayed as Slides:

1. Clicking the folder reveals its immediate bookmark children as inline items on the bookmarks bar, immediately following the folder control.
2. Items to the right are reflowed according to the existing toolbar layout/overflow logic.
3. Clicking the same folder collapses only that Slide.
4. Open state is independent across folders: several Slides may be expanded concurrently; opening one never automatically closes another.
5. Bookmark links activate normally, and folders that retain dropdown mode behave as they do today.
6. Users can switch a folder's mode through the native context menu. Folder content, order, and the core bookmark model remain unchanged.

## Design constraints / questions for review

- Preserve standard keyboard navigation, accessibility semantics, and drag-and-drop where applicable.
- Use existing bookmarks-bar overflow affordances rather than creating extra rows.
- Avoid changes to the bookmark storage hierarchy merely to support presentation.
- Determine whether expanded state is scoped to a window or profile, and whether it should be persisted locally.
- Nested folders within expanded Slides may continue opening their standard menus.

## Interactive proof of concept

The following independent HTML/JavaScript demonstration illustrates the proposed UX inside simulated browser chrome. It does **not** alter Chromium or read real bookmarks.

- Interactive demo: [PUBLIC DEMO URL]
- Source repository: [SOURCE REPOSITORY URL]
- Walkthrough video: [VIDEO URL]

The goal is to evaluate whether this would be a useful **native Chromium browser UI** feature, not an extension API request.
