# gatsby-plugin-stylable

![npm](https://img.shields.io/npm/v/gatsby-plugin-stylable.svg)

Gatsby plugin for enabling [wix/stylable](https://github.com/wix/stylable) support.

## Install

```
npm install --save stylable gatsby-plugin-stylable
```

## How to use

Just install this plugin alongside `stylable` and enable it in your `gatsby-config.js`.

```js
// gatsby-config.js

module.exports = {
  plugins: [`gatsby-plugin-stylable`],
}
```

If you have any other plugins that add CSS loaders to your Webpack config, make sure to place this plugin **after** them.

If you want to configure `@stylable/webpack-plugin`, you may pass additional configuration (`experimentalHMR` is enabled by default):

```js
// gatsby-config.js

module.exports = {
  plugins: [
    {
      resolve: `gatsby-plugin-stylable`,
      options: {
        experimentalHMR: false,
      },
    },
  ],
}
```

## Options

This plugin support any configuration options available to `@stylable/webpack-plugin`. For a full list, see [here](https://github.com/wix/stylable/tree/master/packages/webpack-plugin#plugin-configuration-options).

## License

Copyright &copy; 2019 Aaron Ross. Use of this project is governed by an [ISC license](LICENSE).
