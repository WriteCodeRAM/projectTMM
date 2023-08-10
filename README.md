In here, we can add any packages we want to install as we did in the `project-code-along`. Whenever we add any packages to `dependencies`, remember to run the following to have everything installed:

 

```bash

npm install

```

 

Whenever we run `npm install`, it will look at the `package.json` and install any of the packages stated in `dependencies`. This will generate a `/node_modules` folder. This is where all the packages installed live. It will also generate a `package-lock.json`. This is where node records the exact versions of the packages that were installed.

 

By default, the project will be treated as CommonJS, meaning we would need to import in this manner:

 

```js

const chalk = require('chalk')

```

CommonJS is older and some newer packages (like `chalk`) are not supported by it. So I do recommend using `ES Module` to import your packages as we did in `project-code-along`. To allow this, add the following to `package.json`:

 

```bash

"type": "module"

```

 

This will allow you to now import in such manner:

 

```js

import chalk from 'chalk';

```

 

 

The final `package.json` should look like:

 

```bash

{

  "name": "your-project-name",

  "version": "1.0.0",

  "description": "Description of your project.",

  "main": "app.js",

  "scripts": {

    "test": "echo \"Error: no test specified\" && exit 1",

    "start": "node app.js"

  },

  "author": "Your name",

  "license": "ISC",

  "type": "module",

  "dependencies": {}

}

```

 

You can write all your code in `app.js` and check your code by running:

 

```bash

npm start

```

 

## Links

- [NPM](https://www.npmjs.com/)
