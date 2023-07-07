# CheckMateUI ☑️

Welcome to CheckMateUI, an opinionated list of checklist items for comprehensive UI manual testing. This adaptable framework is tailored to meet your specific needs and works seamlessly with the Kanban method.

‼️ **Note.** Items marked with the 🔃 symbol denote areas that require regular regression checks, helping to ensure that your UI stays up-to-date and flawless. Items without the symbol are considered one-time tasks.

CheckMateUI is your strategic ally in the chess game of UI testing - delivering a checkmate that leaves no room for errors!

## Table of Contents

‼️ **Important.** Consider priorities just as an order of execution. For example, there is no point in checking all links if the page is under development (because we may not have all final URLs for links). It is better to check the layout and the core functionality first. This is why the tasks are divided into priority groups.
    
- [1st priority tasks](#1st-priority-tasks)
- [2nd priority tasks](#2nd-priority-tasks)
- [3rd priority tasks](#3rd-priority-tasks)
- [4th priority tasks](#4th-priority-tasks)

## 1st priority tasks

These tasks are the most important and should be completed first. They are going to be the foundation of our UI testing strategy.

✅ 🔃 Review project requirements and documentation. Explore UI designs in Figma, Adobe XD, etc.
- Explore project features based on designs, requirements, and documentation.
- Study small decorative details from design mockups (it may help in future testing).
- Learn how the layout changes when rebuilding on other screen resolutions (tablets, mobile and wide screens, if any).
- Ask designers and product managers questions if you have any doubts about some points.

## 2nd priority tasks

These tasks are related to pixel-perfect markup checking. They are the next step in our UI testing strategy.

✅ 🔃 [desktop] Pixel-perfect markup checking.

✅ 🔃 [tablet] Pixel-perfect markup checking.

✅ 🔃 [mobile] Pixel-perfect markup checking.
    
## 3rd priority tasks

✅ 🔃 Checking interactive elements (popups, sliders, carousels, etc.).
- All interactive elements work as expected.
- A click on the brand logo (in the header or in the footer, for example) should lead to the site's main page. On the main page, it should scroll to the beginning of the page (unless other mechanics are specified).
- Check that the duration of hiding/closing interactive elements (for example, popups) is short (within 0.1-0.2s). The speed of appearance/opening of such elements can be longer (for example, 0.35-0.5s). This approach will improve the overall user experience with the UI.
- Draggable elements (e.g. carousels) must have an appropriate cursor on hover and drag (cursor: grab, cursor: grabbing).

✅ 🔃 Reduce the screen height to a minimum and check for vertical scrolling in popups, modals and other elements that can have their own scrollbar.

✅ 🔃 Checking the responsive design. Ensure the site looks great on popular screen resolutions: 320, 375, 568, 768, 1024, 1280, 1366, 1440, 1920, and 2560px. It is good to check the resolutions between these states by resizing the window. Also, it is helpful to set, for example, window widths of 1023px and 1024px or 767px and 768px, etc. - sometimes, there might be issues at the borders of breakpoints.

✅ 🔃 Image sizes on the site are checked through the Network panel (Img tab) in Chrome Dev Tools. Approximate guidelines for image weights: for full-screen images - no more than 500-800kb; for all others - no more than 100-200kb. Ensure that the modern image formats (.webp, .avif) are used for all image assets. Also, recheck when images were replaced.

✅ 🔃 Pictures are not blurry (recheck when pictures were replaced).

✅ 🔃 Ensure there are no errors in the developer console.

✅ 🔃 Accessibility. Ensure it is possible to navigate the site using the Tab and arrow keys.

✅ 🔃 Accessibility. The <img> tags have appropriate content in the alt attribute. Decorative <img> elements have empty alt tag contents.

✅ 🔃 Accessibility. Use the Lighthouse tool in Chrome Dev Tools to discover potential accessibility issues.

✅ 🔃 Accessibility. Ensure it is possible to use dropdowns, popups and other interactive elements with the keyboard.

✅ Resizing <textarea> should not break markup (check all textarea on the website).

## 4th priority tasks

✅ 🔃 Checking buttons and links.
- All buttons and links work on all pages as expected.
- All buttons and links have a right cursor on hover (usually `pointer`).
- Buttons on hover have a shorter transition duration. When retracting, a longer transition duration is allowed. This approach will make the site respond more quickly to user actions.
- Buttons/links that have an active state should have a default cursor and nothing should happen when clicking on such elements. [An example of such an element](https://drive.google.com/file/d/1Vb1Ct-_Wm86Eah6Bskj-8rhbUh5iYbmN/view).
- Check that the buttons' text cannot be selected with the mouse (to avoid text selection when double-clicking).
- For small buttons, the click area should be expanded. [Example](https://codesandbox.io/s/expanded-click-area-example-bltliu?file=/src/main.scss)
- Buttons and links have standard :hover, :active states. These states should be noticeable (e.g. changing opacity from 1 to 0.9; won't work).
- Links leading to external sites should open pages in a new tab to avoid taking the user away from the page (setting the `target="_blank"` attribute will allow you to achieve such behaviour). The same goes for `mailto` links.

✅ 🔃 There is no horizontal scroll on all pages and at all resolutions (on touch devices, swipe right/left of the pages to check).

✅ 🔃 There is no horizontal scroll on all pages and at all resolutions (on touch devices, swipe right/left of the pages to check).

✅ 🔃 Check that a custom 404 page is displayed (and not the standard nginx/Apache, for example). Recheck the 404 page also on the production version of the site.

✅ Favicon is added. [How to Favicon in 2023: Six files that fit most needs](https://evilmartians.com/chronicles/how-to-favicon-in-2021-six-files-that-fit-most-needs)

✅ Webmanifest is added.

✅ For the production version of the site, the sharing image should be loaded when posting to social networks and messengers.
- Facebook.
- LinkedIn.
- Twitter.
- etc.

✅ The <title> and <meta name="description"> tags have the correct content on all pages.

✅ Page speed tested using Lighthouse tool in Chrome Dev Tools and using [PageSpeed Insights](https://pagespeed.web.dev/). Invite developers to make changes based on the review results, guided by common sense.

✅ Testing all pages in different browsers on different devices. 
- [real device] MacBook Pro, Google Chrome – current version.
- [real device] MacBook Pro, Firefox – current version.
- [real device] MacBook Pro, Safari – current version.
- [real device] iPad, Safari – old version.
- [real device] iPhone SE 1, Safari – old version.
- [real device] iPhone SE 1, Chrome – current version.
- [real device] iPhone 11, Safari – older version.
- [real device] Xiaomi 5A/6A, Chrome – current version.
- [virtual] macOs Big Sur, Safari 14.
- [virtual] Windows 11, Firefox 107.
- [virtual] Windows 11, Edge 100.
- [virtual] Windows 7, Opera 80.
