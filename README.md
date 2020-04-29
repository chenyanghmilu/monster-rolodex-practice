# monster-rolodex-practice

## check it on [here](https://chenyanghmilu.github.io/monster-rolodex-practice/) to view

### Deploy to GitHub Pages

The following instructions allow you to deploy any of your front-end **only** React apps using GitHub Pages (GitHub Pages is unable to hostfull-stack apps).

Please follow these steps to deploy your app to GitHub Pages:

1. In Terminal, create a local git repo: `$ git init`

2. In your GitHub account, create a new repository named **< the app name >**.

3. Back in Terminal, add the `origin` remote:
   `$ git remote add origin https://github.com/<your github username>/<the app name>.git`

   > Be sure to replace **< your github username >** with your personal GitHub username!

4. To save time, there's no need to make a commit, the tool we are going to use will automatically make a commit and create a `gh-pages` branch.

5. In VS Code, open your **package.json** and add an additional **top-level** key/value pair:
   `"homepage": "https://<your github username>.github.io/<the app name>",`.

6. Also in **package.json**, add two additional key/value pairs, `"predeploy"` and `"deploy"`, **within the existing** `"scripts"` key:

   ```
   	"scripts": {
     		// add these two new keys, don't forget to add a comma above
     		"predeploy": "npm run build",
     		"deploy": "gh-pages -d build"
   	}
   ```

7. In Terminal, let's install the `gh-pages` npm package we just referenced in the `"deploy"` entry:
   `$ npm i gh-pages`

8. Now run the command `$ npm run deploy` to deploy! (enter your GitHub credentials if asked).

> The `"predeploy"` script automatically builds the app.

> The `https:// < your github username >.github.io/<the app name> link might take a minute to become active.
