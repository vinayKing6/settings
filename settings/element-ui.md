### Install element-ui

```shell
npm i element-ui -S
```

### Use element-ui  by need

```shell
npm install babel-plugin-component -D
```

Then change the babel.conf.js into this:

```javascript
module.exports = {
  presets: [
    '@vue/cli-plugin-babel/preset',
    ["@babel/preset-env", { "modules": false }]
  ],
  //按需引入element-ui
  plugins: [
    [
      "component",
      {
        "libraryName": "element-ui",
        "styleLibraryName": "theme-chalk"
      }
    ]
  ]
}

```

