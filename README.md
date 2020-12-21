# vuepress-plugin-kano

[![Latest Release](https://img.shields.io/github/v/tag/kalisio/k-openradiation?sort=semver&label=latest)](https://github.com/kalisio/k-openradiation/releases)


## Overview

This is a simple [VuePress](https://vuepress.vuejs.org/) plugin that provides a global component wrapping [Kano](https://kalisio.github.io/kano/), _a powerful real-time Geovisualizer_.

See this plugin in action [here](http://localhost:8080/kano/guides/advanced-usage.html#integrating-kano) !

## Installation

You can install it with

```bash
yarn add vuepress-plugin-mermaidjs
```

And then you just need to register the plugin in your `.vuepress/config.js`:

```js
module.exports = {
    // ...
    plugins: [
        'vuepress-plugin-mermaidjs'
    ]
    // ...
}
```

## Usage

The recommended usage is to place your **Kano** declaration as an HTML element:

```html
<kano source="your Kano URL" token="your Kano token" />
```

## Contributing

Found a bug ? Missing a Feature ? Want to contribute ? check out our [contribution guidelines](./CONTRIBUTING.md) for details

## Authors

This project is sponsored by 

[![Kalisio](https://s3.eu-central-1.amazonaws.com/kalisioscope/kalisio/kalisio-logo-black-256x84.png)](https://kalisio.com)

## License

This project is licensed under the MIT License - see the [license file](./LICENSE.md) for details



