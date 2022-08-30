# near-react-boilerplate

Setup React without using npx create-react-app command.

## Fast setup

**copy and paste the following commands in CLI.**

```
git clone https://github.com/NEARworld/near-react-boilerplate.git && cd ./near-react-boilerplate && git remote remove origin && npm i && npm run build && npm start
```

### If you want Typescript React setup, here.

https://github.com/NEARworld/near-ts-react-boilerplate

### Detailed setup

This is just to show you what kind of npm modules are required for this boilerplate.

#### setup webpack

```
npm i --save-dev webpack webpack-cli webpack-dev-server
```

#### setup babel

```
npm i --save-dev babel-loader babel-eslint @babel/core @babel/preset-react @babel/preset-env @babel/plugin-transform-react-jsx @babel/runtime
```

#### setup react

```
npm i react react-dom
```

## How to start the app?

```
npm run build
```

```
npm start
```

## Note

You don't need following codes when using my template.

```jsx
import React from "react";
```

The reason is it's unnecessary from `React 17`.
This babel plugin allows you to not use the import statement above.

```
@babel/plugin-transform-react-jsx
```

Babel configuration for this.
Inside `.babelrc`

```json
"plugins": [
    [
      "@babel/plugin-transform-react-jsx",
      {
        "runtime": "automatic"
      }
    ]
  ]
```

For more information, check the following documentation.

https://reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html
