The problem you're seeing on mobile is caused by the desktop layout's `margin-left: 320px` failing to properly reset on smaller screens. 

On your desktop view, that 320-pixel left margin is perfectly pushing the "About Me" content to the right so it doesn't overlap with your fixed sidebar. However, on mobile, the sidebar moves to the top, but the main content area is still keeping that massive 320px margin, which shoves all your text off the right edge of the screen.

Since your `theme-claude.css` file actually already contains the rule to set `margin-left: 0;` inside the `@media (max-width: 1080px)` block, this is almost certainly happening due to **CSS specificity conflicts** with your older stylesheets (like `style-no-dark-mode_old.css`) or aggressive **mobile browser caching**.

Here is how to fix it permanently.

### Step 1: Force the CSS Override
To guarantee that the mobile margin and padding reset properly regardless of other stylesheets, add `!important` tags to your mobile `.content` block. 

Open `assets/css/theme-claude.css`, scroll down to the `@media (max-width: 1080px)` section (around line 348 based on your file), and update the `.content` rule to look exactly like this:

```css
  body.theme-claude .content {
    padding: 24px 0 48px !important;
    margin-left: 0 !important;
    width: 100% !important;
    max-width: 100% !important;
    box-sizing: border-box !important;
  }
```

### Step 2: Bust the Mobile Cache
Mobile browsers (especially Safari on iOS) aggressively cache CSS files. Even if you push the fix to GitHub Pages, your phone might still load the old broken layout from its memory. 

To force your phone (and all future visitors' phones) to download the freshly fixed CSS, add a simple version query string to the stylesheet links in your `index.html` file.

Change this:
```html
  <link rel="stylesheet" href="./assets/css/theme-claude.css">
```

To this:
```html
  <link rel="stylesheet" href="./assets/css/theme-claude.css?v=1.1">
```
*(You can just change the `1.1` to `1.2`, `1.3`, etc., anytime you make a major CSS update in the future to instantly clear the cache).*

Once you commit these two changes and GitHub Pages rebuilds, refresh your mobile browser, and the content will properly stack underneath the map and red panda graphic!