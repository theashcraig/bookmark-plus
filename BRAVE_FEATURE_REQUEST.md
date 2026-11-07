# Feature request: Optional inline “Slide” mode for bookmark folders

**Suggested category:** Brave Feature Requests → Desktop Requests

I'd like to propose a small, optional enhancement to Brave's existing bookmarks bar: a new folder **display mode** called a **Slide**.

Currently, clicking a bookmark folder opens a dropdown. That works well for large archives of bookmarks, but it adds extra navigation when repeatedly accessing a small collection of frequently used websites. Leaving all of those links directly on the bar creates clutter.

## Proposed interaction

- Right-click an existing bookmarks-bar folder and choose **Display as Slide**, or leave it in the default **Dropdown** mode.
- Clicking a Slide reveals the folder's existing child bookmarks **inline, immediately after the folder label**, pushing neighboring items to the right.
- Clicking the same Slide again collapses it.
- **Slides are independent.** Several may remain open simultaneously; opening one never automatically closes another.
- Ordinary folders keep the same dropdown behavior they have today.
- Bookmarks remain in their original folders. No new bookmark database, storage hierarchy, or migration is required.
- Native overflow handling, keyboard navigation, and accessibility should be preserved.

## Interactive proof of concept

The independent HTML/JavaScript demonstration illustrates the proposed UX inside simulated browser chrome. It does **not** modify Brave or access real bookmarks.

- **Interactive demo:** [Try Bookmark+](https://ashcraig.com/bookmarkplus/)
- **Source repository:** [Bookmark+ on GitHub](https://github.com/theashcraig/bookmark-plus)
- **Walkthrough video:** [Watch the walkthrough on the demo site](https://ashcraig.com/bookmarkplus/#walkthrough)

The demo includes multiple independently expanded Slides and an optional per-folder display setting.

I'd appreciate feedback about whether this behavior could fit naturally into Brave's native bookmarks bar.
