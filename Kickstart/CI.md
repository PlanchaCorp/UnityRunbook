# Continuous integration with Github and Unity

> ℹ️ We rely on those tools to continuously build and deploy the game:   
>- **Github Actions**
>   - We use existing actions, most notably from `GameCI`
>- **Github Pages** (static web server where the Webgl build is hosted)

## Build automatically 

For the first steps, we rely on [the open source project **GameCI**](https://game.ci/docs/github/getting-started).  
You can follow the process on their website, here is an overview of what you'll have to do:  
- Create a `.github/workflows` folder in your Unity project for your workflow definition
- Request a Unity license. The license is needed for build, and we want to have it as well as the associated Unity email and password in Github secrets ot be used later on
- Now our workflows have everything they need to build the project

Use our workflows to automatically build and deploy a WebGL project (so you can play test directly on a url, and download the built project if you want) and semi-automatically (= on demand) build linux/windows project
- In Unity, go to **Project Settings**, **Player**, WebGL part, **Publishing Settings**, and set the **Compression Format** to **Gzip**. Save.
- Copy the workflows you need in the `.github/workflows` folder:  
  - `unity-webgl.yml` (build a WebGL app on every commit on `main` and upload it as an archive and on Github Pages)
  - `unity-desktop.yml` (build a Windows and Linux app when you trigger the workflow)
- Enable GitHub Pages in the project settings, for the branch automatically created with the workflow
