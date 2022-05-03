# ifcjs-101

Hello world example of IFC.js

This project is set-up by following the instruction provided in the IFC.js [Hello World documentation](https://ifcjs.github.io/info/docs/Hello%20world)

## Setting up the project

### Install libraries

The first thing to do is to create an empty folder and start a new npm project with the command npm init. This will generate a package.json file containing some data such as the project name, version, commands and dependencies. In addition, the following dependencies must be installed with npm:

```bash
npm i web-ifc-three

npm i three

npm i rollup --save-dev
npm i @rollup/plugin-node-resolve --save-dev
```

### Index.html

The next step is to create an HTML file named index.html as the main document of the application. The HTML will have:

- A canvas element, used to render the Three.js scene.
- An input element, which will open IFC files from our computer to the application.
- A script referencing a file called bundle.js, which is the bundle of the app that we will produce with rollup.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>Document</title>
  </head>
  <body>
    <input type="file" name="load" id="file-input" />
    <canvas id="three-canvas"></canvas>
    <script src="bundle.js"></script>
  </body>
</html>
```

### Adding style

The following CSS file will make the canvas full screen:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body {
  overflow: hidden;
}

#three-canvas {
  position: fixed;
  top: 0;
  left: 0;
  outline: none;
}

#file-input {
  z-index: 1;
  position: absolute;
}
```
