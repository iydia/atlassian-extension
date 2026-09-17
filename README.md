# atlassian-extension
Backlit Card Theme for Jira Boards

## Getting started

A minimal Chrome Manifest V3 extension using plain JavaScript, HTML, and CSS.
No dependencies or build step are required.

1. Open `chrome://extensions` in Chrome.
2. Enable **Developer mode**.
3. Click **Load unpacked** and select this repository's `extension/` folder.
4. Open the extension from Chrome's toolbar to view its popup.

After editing files, click **Reload** on the extension's card in
`chrome://extensions`. Refresh Jira tabs to reload the content script.

## Structure

```text
extension/
  manifest.json       # Extension metadata and entry points
  content/
    index.js          # Jira content-script entry point
  popup/
    index.html        # Toolbar popup
    styles.css        # Popup styling with system light/dark support
```

The content script runs on `https://*.atlassian.net/*` and currently makes no
changes to Jira. Board detection, hierarchy mapping, and card illumination are
not implemented yet. The scaffold requests no additional API permissions and
does not collect or transmit data.

## Publishing

The `extension/` directory is the extension package root. When preparing a
Chrome Web Store release, ZIP its contents with `manifest.json` at the ZIP root.
Store icons, screenshots, listing details, and privacy disclosures still need
to be prepared before submission.
