# Feature request: Optional inline “Slide” mode for bookmark folders (interactive demo)

**Category:** Brave Feature Requests → Desktop Requests

I'm proposing a small enhancement to Brave's existing bookmarks bar: an optional display mode for ordinary bookmark folders called **Slide**.

Today, folder clicks open dropdown menus. That works for large archives of infrequently visited bookmarks, but it's less convenient when switching between a handful of frequently used links for different projects. Leaving all of those links permanently on the bar also creates clutter.

**Proposed behavior**

- Right-click a folder on the bookmarks bar and choose **Display as Slide** (or return it to **Dropdown** mode).
- Click a Slide folder; its existing child bookmarks appear **inline, immediately to its right**, pushing subsequent bar items to the right.
- Click the same Slide again to collapse it.
- Multiple Slides can remain open at the same time. **Opening Personal or Banking never closes Work.** Each Slide is closed manually.
- Regular bookmark folders remain unchanged and continue opening their dropdown menus.
- When space is limited, use the browser's established bookmarks overflow behavior; preserve keyboard and accessibility support.

**Importantly:** this would not be a separate bookmark manager or new bookmark storage format. A Slide would still be a normal bookmark folder with a different toolbar display preference. The underlying bookmarks would stay exactly where they are.

I've built a self-contained interactive demonstration (HTML/CSS/JavaScript). It shows the behavior inside a simulated browser toolbar and can be used without installing anything. It's not a modified Brave build or browser extension.

**Try the interactive demo:** [PUBLIC DEMO URL]

**View the working demo source:** [SOURCE REPOSITORY URL]

**Short walkthrough:** [VIDEO URL]

I would welcome feedback about the interaction, overflow behavior, and how this could fit naturally into Brave's native bookmarks bar.
