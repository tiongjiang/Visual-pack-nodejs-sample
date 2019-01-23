 Quick start template on using nodejs as a development workflow

 ## Getting Started
 These instructions will assist on setting up your development enviroment, and deployment into a giant environment.

 ## Prerequisite:
 - Has access to a version of giant
 - Know what is nodeJs and have [a version installed](https://nodejs.org/en/)

 ## Setup
 1. Git clone this environment
 2. Delete the .git (and setup your own git)
 3. Update the below files to your repective values

    - package.json (name, desciption, author)
    - webpack.config.js ('myCustomVisual' 2 places, change to your visual name)
    - package-lock.json ('myCustomVisual' 1 place, change to your visual name)
    - program.js ('myCustomVisual' 1 place, change to your visual name)
    - src/quadrant-properties.js ('myCustomVisual 1 place, change to your visual name)
    - publish/config.js (visual name, display name)
    - publish/config.js install.visualConfig
    - publish/config.js install.authcookie **GIANT WEB ACCESS COOKIE**
    - publish/config.js install.giantUrl **RELATIVE TO AUTH COOKIE**

## How to obtain GIANT web access cookie

After logging into GIANT, open web debugger console (press **F12**) and switch to **Network** tab. Select one of the network action at the right panel, look for **Request Headers** of that network action and copy the **Cookie** value.

## Development Files

| File        | Description            |
| ------------- |-------------|
| publish/visual/icon.png | icon file of custom visual |
| publish/visual/quadrant-properties.html | properties html for quadrant configuration      |  
| publish/visual/quadrant-properties.js | javascript for properties html. parse by giant during configuration stage
| src/app.js | main rendering of custom visual |
| src/app.scss | main styling of custom visual |
| program.js | Development only files. Dump any debugging configuration here for testing purpose |

See [Visual pack documentation](https://github.com/fx-giant/giant-documentations/blob/master/visual/visual-pack.md#quadrant-properties-html-js) for more information about quadrant properties HTML and javascript.

>Protip: for additional scripts/style for your visual pack, add the files in the src folder and import in the app.js.

## How to Run
```bash

--Debug visual application (browser will launch localhost:8080)
npm run debug 

-- Deploy visual pack to giant base on configuration
npm run publish

--see package.json for other relevant commands

```

## How I install Amchartv4 webpack dependencies
