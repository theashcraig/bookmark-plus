# Bookmark+ — Let your bookmarks unfold.

**A proposed native bookmarks-bar feature for Chromium-based browsers, including Brave and Chrome.**

### [▶ Try the interactive Bookmark+ demo](https://ashcraig.com/bookmarkplus/)

Bookmark folders have largely worked the same way for years: click a folder, navigate a dropdown, choose a bookmark, and repeat. Dropdowns are useful for big collections, but less convenient for the small groups of sites we visit throughout the day.

**Bookmark+ introduces Slides:** an optional way for existing bookmark folders to reveal their links **horizontally, right on the bookmarks bar**.

## The idea

- **Choose per folder.** Right-click a folder and select **Display as Slide** or keep the familiar dropdown.
- **Unfold inline.** Click a Slide to reveal its bookmarks immediately to its right, pushing subsequent toolbar items along.
- **Keep multiple Slides open.** Work, Personal, and Banking can all stay expanded independently. Opening one never closes another.
- **Close when you're ready.** Click a Slide's label again to collapse only that Slide.
- **Keep your bookmarks.** Slides are a *display preference* for ordinary bookmark folders—not a new bookmark database or hierarchy.

The concept also explores a restrained dark interface: flat bookmark links, separators, subtle hover states, and translucent dropdown menus.

## Experience the prototype

**[Open the live interactive demonstration →](https://ashcraig.com/bookmarkplus/)**

Try these interactions in the simulated browser:

1. Click **Work**, **Personal**, and **Banking**. Each opens independently.
2. Click any open Slide again to collapse it.
3. Open **Explore** to see the standard folder behavior in a dark-glass dropdown.
4. Right-click a folder to switch between **Dropdown** and **Slide** presentation.
5. Use **Customize folders** to experiment with the demo's folder settings and sample links.

Sample links lead to public websites. The prototype uses illustrative bookmarks rather than your own browser data.

## Proposed native implementation

The goal is a small, optional enhancement to the **existing browser bookmarks bar**:

- Keep the browser's bookmark model and folder structure intact.
- Associate a `dropdown` or `slide` display preference with each folder.
- Render expanded Slide children inline using the native toolbar layout and overflow behavior.
- Preserve keyboard navigation, accessibility, and normal bookmark actions.
- Decide during implementation how open/closed state should persist across windows and sessions.

The visual style is exploratory; the core feature is the **independent inline expansion of ordinary folders**.

## Project status

**Interactive design prototype / feature proposal.** This repository contains a standalone HTML, CSS, and JavaScript simulation. It does **not** modify Brave or Chromium, install an extension, or access or change anyone's real bookmarks.

The proposal documents are available here:

- [Brave feature request draft](BRAVE_FEATURE_REQUEST.md)
- [Chromium feature request draft](CHROMIUM_FEATURE_REQUEST.md)

Feedback on usability, accessibility, overflow, and native integration is welcome.

## License and attribution

The original demonstration code in this repository is offered under the [MIT License](LICENSE). Third-party brand names, icons, and trademarks displayed as examples remain the property of their respective owners. Bookmark+ is an independent concept and is not affiliated with or endorsed by Brave, Google, or the sample websites.
