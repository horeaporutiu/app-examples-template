# app-examples-template

This app shows how to implement image drag and drop to a Miro board. 

### App Demo

https://github.com/horeaporutiu/app-examples-template/assets/10428517/d2196d11-2a76-4cb9-8510-39e26b0da5cf

### Featured Technologies
* React
* TypeScript
* Vite
* [create-miro-app npm package](https://www.npmjs.com/package/create-miro-app)

### Associated Developer Tutorial
> To view a more in depth developer tutorial
of this app (including code explanations) see the [drag-and-drop tutorial](https://developers.miro.com/docs/add-drag-and-drop-to-your-app) on Miro's Developer documentation.

**&nbsp;ℹ&nbsp;Note**:

- We recommend a Chromium-based web browser for local development with HTTP. \
  Safari enforces HTTPS; therefore, it doesn't allow localhost through HTTP.
- All examples use `npm` as a package manager and `npx` as a package runner. \
  If you prefer, you can install and use equivalent alternatives, such as `yarn` or `pnpm`.

### How to start locally

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
4. Open a board: you should see your app in the apps toolbar or in the apps panel.