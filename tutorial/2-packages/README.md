# 2 - Installing and using an NPM package

In this section we will install and use an NPM package. A "package" is simply a piece of code that someone else wrote, and that you can use in your own code. It can be anything. Here, we're going to try a package that helps you manipulate colors for instance.

- Install the community-made package called `color` by running `npm install --save color`.

Open `package.json` to see how `--save` automatically added `color` in  `dependencies`.

A `node_modules` folder has also been created to store the package.

- Create a `.gitignore` file and put `node_modules` and `npm-debug.log` in it (and `git init` a new repo if you haven't done that yet).

- Add `const Color = require('color');` in `index.js`
- Use the package like this for instance: `const redHexa = Color({r: 255, g: 0, b: 0}).hexString();`
- Print `redHexa`, it should show `#FF0000`

Congratulations, you installed and used an NPM package!

`color` is just used in this section to teach you how to use a simple package. We won't need it anymore, so you can uninstall it:

- Run `npm uninstall --save color`

**Note**: There are 2 kinds of package dependencies, `"dependencies"` and `"devDependencies"`. `"dependencies"` is more general than `"devDependencies"`, which are packages that you only need during development, not production (typically, build-related packages, linters, etc). For `"devDependencies"`, we will use the `--save-dev` parameter instead of `--save`.


Next section: [3 - Setting up ES6 with Babel and Gulp](/tutorial/3-es6-babel-gulp)

Back to the [previous section](/tutorial/1-npm-and-package-json) or the [table of contents](https://github.com/verekia/js-stack-from-scratch).
