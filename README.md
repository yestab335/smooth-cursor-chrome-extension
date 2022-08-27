<p align="center">
  <img src="assets/logotype.png" alt="Smooth Cursor Logo" height="150px">
  <p align="center">Apply a Microsoft Word-like smooth caret animation to multiple online text editors.</p>
  <p align="center">
    <a href="https://addons.mozilla.org/fr/firefox/addon/smooth-cursorify/">Firefox</a>
    &nbsp; &bull; &nbsp;
    <a href="https://chrome.google.com/webstore/detail/smooth-cursorify/ohhjfajndpfpbimipmehmdkblnbelaec?hl=fr&authuser=0">Chrome</a>
    &nbsp; &bull; &nbsp;
    <a href="https://www.youtube.com/watch?v=35It5ijWl_0">Demo video</a>
  </p>
</p>

## Supported Websites
> Please open an issue to request a new website

* Google Docs (https://docs.google.com/)

## How does it work?
Some websites use custom rendering engines to edit rich text, instead of relying on `contenteditable` or using a plain `<textarea>`/`<input>`. When using such custom methods, the cursor is not the native one, and is instead an HTML element, that can be stylized like any other. For example, Google Docs uses a 2-pixels-wide div with a black background to render its cursor.

Since those cursors are plain in HTML elements, they can be **stylized**, that's where this extension comes in.

The process is simple:

1. Find the element
2. Append `transition: all 310ms` to its style tag

The problem with this is that methods using the native cursor can't really have them applied: I _can't_ access the system cursor to style it with CSS.

## Manual Installation