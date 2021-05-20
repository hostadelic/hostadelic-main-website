Hostadelic main website
=======================

Public website for Hostadelic.

### Install the dependencies:

```bash
npm install # or just yarn
```

### Start Project:

```bash
npm start # or npm run dev
```

Navigate to [localhost:3000](http://localhost:3000). You should see your app running.

This spawns a development server, so simply edit a file in `src`, save it, and reload the page to see your changes.

You can also see a live demo of this template: [https://elderjs.pages.dev/](https://elderjs.pages.dev/)

### To Build HTML for Production:

```bash
npm run build
```

Let the build finish. It will put all of your staticly generated files in `./public`.

If you wish to preview you can use:

```bash
npx sirv-cli public
```

### To Run in SSR Mode for Production:

```bash
npm run serve
```

### What to Expect

- Nodemon is watching your files for changes. It will restart when it needs to.
- Rollup is watching your files for changes. It will restart when it needs to.
- If your `elder.config.js` has `@elderjs/plugin-browser-reload': {}` in it's plugins, your browser will automatically restart after the server restarts.

# Contributing

[Icons](https://icons8.com/icons/nolan).

[CSS gradients](https://cssgradient.io).

# History

This website uses `Elder.js` and started from the `Elder.js Template Project`,
a project template for [Elder.js](https://elderguide.com/tech/elderjs/) apps.
The template lives at https://github.com/elderjs/template and the Elder.js
source is here: https://github.com/elderjs/elderjs

Here is a demo of the template:
[https://elderjs.netlify.app/](https://elderjs.netlify.app/)

<img
src="https://img.shields.io/badge/dynamic/json?color=brightgreen&label=Node&query=engines.node&url=https%3A%2F%2Fraw.githubusercontent.com%2Felderjs%2Ftemplate%2Fmaster%2Fpackage.json"
alt="node version" />


## Start

The project started on May 16, 2021 following the template's "Getting Started"
section, so by using [degit](https://github.com/Rich-Harris/degit):

```bash
npx degit Elderjs/template hostadelic-main-website
cd hostadelic-main-website
```
