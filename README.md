# React Chrome Extension

This extension is built with React as a view engine to render a popup. Use this as a starting point to continue and build your own extension functionality.

## Installing

`npm install -g create-react-app`

## Create a new project

`create-react-app react-chrome-extension` or whatever you want to name it.

## Configure the manifest.json

Chrome extensions need to have a manifest.json file in their root folder. That manifest tells Chrome how to create the extension and how to run it. In the manifest, you will configure things like the logo, name, and description of your extension. Since you will want to make the manifest part of your build root folder, the manifest file should be in the project's public folder. `create-react-app` builds the files from the public folder and puts it into the build folder when you compile the project. Other things to put in the public folder include content, background scripts and assets.

```
{
  "manifest_version": 2,
  "name": "My Extension",
  "description": "This extension is a starting point to create a real Chrome extension",
  "version": "0.0.1",
  "browser_action": {
    "default_popup": "index.html",
    "default_title": "Open the popup"
  },
  "icons": {
    "16": "logo-small.png",
    "48": "logo-small.png",
    "128": "logo-small.png"
  },
  "permissions": [
  ]
}
```

`browser_action` tells Chrome that we will have a popup which will run the index.html file.

`icons` will be used to present the icon in the extension tray and in Chrome extension list. Icons must be 128px wide.

## Build the project

`npm run build`

## Add extension to Chrome

`chrome://extensions/`

Press `Load unpacked extension` (might need to show dev options).

Browse to the build folder and press the OK button.

Later on, if you have a developer account in the Chrome extension store you will be able to load it to the store and distribute it publicly.
