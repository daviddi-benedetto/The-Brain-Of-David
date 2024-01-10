## Creating An App With Electron
I'm giving a dive into creating a desktop-level application, and it seems like Electron is a good framework to build with (although not very lightweight apparently). Slack, Discord, Skype, Notion, are all examples of apps that use Electron successfully. Also, it's developed by GitHub, so the support is good.

"By embedding [Chromium](https://www.chromium.org/) and [Node.js](https://nodejs.org/) into its binary, Electron allows you to maintain one JavaScript codebase and create cross-platform apps that work on Windows, macOS, and Linux — no native development experience required."

Official tutorial is here: https://www.electronjs.org/docs/latest/tutorial/tutorial-prerequisites
### Prerequisites
1. First, make sure Node.js is installed as well as NPM, which is typically packaged with Node.js in its installer.
2. This may be optional, but I had to update NPM using this command to before I could create my Electron app.
```
npm install -g npm
```
### Initial Steps
1. Go into the directory to create a new folder in. In the terminal, enter the below code to generate the initial files.
```
npx create-electron-app [App Name]
```
2. To test the app and make sure it is running properly, run the code in the newly created directory.
```
npm start
```

--- 
Create edits from here. After making changes in the codebase, make sure to type ```rs``` into the command line to reset the page view since there is not auto-refresh.
