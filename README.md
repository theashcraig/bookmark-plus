# Bookmark+ — Native browser UI feature proposal (v2.2)

A static, interactive HTML/CSS/JavaScript concept for a **native** bookmark-folder display option, called a *Slide*, in Brave/Chromium.

## The opening animation (new in v2.2)

- The hero contains a compact, real-time illustration of the toolbar interaction.
- It automatically expands **Work** and then **Personal**, showing that they remain open independently.
- It **runs once on page load**, does not loop, and offers a **Replay preview** control.
- Visitors can also toggle the preview folders manually. User interaction interrupts the scheduled animation.
- `prefers-reduced-motion: reduce` skips the movement and immediately displays both expanded.
- The preview uses a **copy of icons from the main working demo**, so it does not separately load another set of favicons.

## The full interactive demonstration

Click **Work**, **Personal**, and **Banking** independently to expand/collapse their existing bookmark examples inside a *simulated* browser toolbar. Use **Explore** to see a dark glass dropdown. Right-click a folder to choose **Display as Slide** or **Display as dropdown**, or use **Customize folders**.

Sample bookmarks open real public websites. Changes made with the demo manager are temporary and remain in the webpage; **no real browser bookmarks are read or changed**.

The static HTML is a **visual proof of concept**, not an extension or an actual Brave/Chromium patch. Brand icons and trademarks belong to their respective owners. No affiliation with Brave, Chrome, or the sample destinations is claimed.

## Publish on ashcraig.com

The site has no build step, package manager, API server, PHP, or database.

1. Find the Apache document root for the existing `ashcraig.com` virtual host. Do **not** change the existing vhost or production configuration.
2. Create a separate `bookmarkplus/` subdirectory in that document root.
3. Upload these files to that directory: `index.html`, `BookmarkPlus-IconFix-Walkthrough.mp4`, and `BookmarkPlus-Source.zip`.
4. Open `https://ashcraig.com/bookmarkplus/` and test the intro, Slide expansion, dropdown, and source/video downloads.
5. Confirm HTTPS is enabled, the page loads on mobile, and no PHP or sensitive server files are exposed.

The source ZIP and video links in `index.html` are relative, so they work from `/bookmarkplus/` without editing URLs.

## Share source on GitHub

Create a public repo such as `bookmark-plus`, then include `index.html`, this README, `BRAVE_FEATURE_REQUEST.md`, `CHROMIUM_FEATURE_REQUEST.md`, and any preview assets you want published. You **do not need GitHub Pages** if the demo is hosted on ashcraig.com.

**Before choosing a license:** Publicly sharing code without an explicit license does not automatically grant reuse or redistribution rights. If you want Brave/Chromium developers to reuse the code, consider applying a suitable open-source license and confirming you own the material being licensed.

## Suggested review workflow

- Review wording, interaction, keyboard behavior, and layout at common screen sizes.
- Search Brave Community and Chromium tracker for similar ideas before creating a new post.
- Replace `[PUBLIC DEMO URL]`, `[SOURCE REPOSITORY URL]`, and `[VIDEO URL]` in the proposal drafts with verified public links.
- Publish the Brave feature request first; then submit a Chromium feature request with the same canonical demo URL.

Do not describe the HTML illustration as a modified browser build or claim that Brave/Chromium has accepted the proposal.
