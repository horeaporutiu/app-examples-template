# Miro drag and drop app

This app shows how to implement image drag and drop to a Miro board. 

### App Demo

https://github.com/horeaporutiu/app-examples-template/assets/10428517/d2196d11-2a76-4cb9-8510-39e26b0da5cf

## Table of Contents
1. [Tools and Technologies](https://github.com/horeaporutiu/app-examples-template#tools-and-technologies)
2. [Included Features](https://github.com/horeaporutiu/app-examples-template/tree/main#included-features)
3. [Prerequisites](https://github.com/horeaporutiu/app-examples-template/tree/main#prerequisites)
4. [Associated Developer Tutorial](https://github.com/horeaporutiu/app-examples-template/tree/main#associated-developer-tutorial)
5. [Run the app locally](https://github.com/horeaporutiu/app-examples-template/tree/main#run-the-app-locally)
6. [Optional - Build the app](https://github.com/horeaporutiu/app-examples-template/tree/main#optional---build-the-app)
7. [Folder Structure](https://github.com/horeaporutiu/app-examples-template/tree/main#folder-structure)
8. [License](https://github.com/horeaporutiu/app-examples-template/tree/main#license)

## Tools and Technologies
* [React](https://react.dev/)
* [TypeScript](https://www.typescriptlang.org/)
* [Vite](https://vitejs.dev/)
* [Node.js](https://nodejs.org/en/download)
* [create-miro-app npm package](https://www.npmjs.com/package/create-miro-app)

## Included Features
* [Miro Web SDK](https://developers.miro.com/docs/web-sdk-reference)
    * [drop event](https://developers.miro.com/docs/ui_boardui#drop-event) 
    * [openPanel(options)](https://developers.miro.com/docs/ui_boardui#openpanel)
    * [draggable elements](https://developers.miro.com/docs/add-drag-and-drop-to-your-app#add-draggable-elements-to-the-app-panel)

## Prerequisites
* You have a [Miro account](https://miro.com/signup/).
* You're [signed in to Miro](https://miro.com/login/).
* Your Miro account has a [Developer team](https://developers.miro.com/docs/create-a-developer-team).
* Your development environment includes [Node.js 14.13](https://nodejs.org/en/download) or a later version.
* Chromium-based web browser for local development with HTTP.
* All examples use `npm` as a package manager and `npx` as a package runner.

## Associated Developer Tutorial
> To view a more in depth developer tutorial
of this app (including code explanations) see the [drag-and-drop tutorial](https://developers.miro.com/docs/add-drag-and-drop-to-your-app) on Miro's Developer documentation.

## Run the app locally

1. Run `npm install` to install dependencies.
2. Run `npm start` to start developing. \
   Your URL should be similar to this example:
   ```
   http://localhost:3000
   ```
3. Open the [app manifest editor](https://developers.miro.com/docs/manually-create-an-app#step-2-configure-your-app-in-miro) by clicking **Edit in Manifest**. \
   In the app manifest editor, configure the app as follows:
   - [`sdkUri`](https://developers.miro.com/docs/app-manifest#sdkuri): assign `http://localhost:3000` as a value for this property. \
     It defines the entry point of the app, and it corresponds to the URL of the server that the app runs on.
   - [`scopes`](https://developers.miro.com/docs/app-manifest#scopes): add the permission scopes that users need to grant the app when they install it. \
     To enable the app to read from and write to the board, add the following permissions:
     - `boards:read`
     - `boards:write`

4. Go back to your app home page, and under the `Permissions` section, you will see a blue button that says `Install app and get OAuth token`. Click that button. Then click on `Add` as shown in the video below.

> ⚠️ Make sure to install your app on a [developer team](https://developers.miro.com/docs/create-a-developer-team)! ⚠️

https://github.com/horeaporutiu/app-examples-template/assets/10428517/cb9698e8-fa77-4ad7-a349-ec1323f3cfee

5. Go to your developer team, and open your boards. <b>Refresh your browser</b>.
6. Click on the plus icon from the bottom section of your left sidebar. If you hover over it, it will say `More apps`.
7. Search for your app `Drag and drop` or whatever you chose to name it. Click on your app to use it, as shown in the video below.

https://github.com/horeaporutiu/app-examples-template/assets/10428517/708fb556-0553-4b46-8b74-1eb53ec70c65

## Optional - Build the app

- Run `npm run build`. \
  This generates a static output inside `dist/`, which you can host on a static hosting service.

## Folder structure

```
.
├── src
│  └── styles
│      └── style.css <-- CSS styles for the app.
│  └── App.tsx <-- The main app. Contains structure for the sidebar when launched. This file also contains logic for fetching images from [The Noun Project](https://thenounproject.com/).
│      main.tsx <-- Initializes app, and contains logic for dropping image onto the board.
├── app.html <-- The app itself. This is loaded on the board inside the 'appContainer'.
└── index.html <-- The app entry point. This is the value you assign to 'sdkUri' in the app manifest file.
```

## License
[MIT License](https://github.com/miroapp/app-examples/blob/main/LICENSE).
