# vuepress-plugin-kano

[![Latest Release](https://img.shields.io/github/v/tag/kalisio/vuepress-plugin-kano?sort=semver&label=latest)](https://github.com/kalisio/vuepress-plugin-kano/releases)


## Overview

This is a simple [VuePress](https://vuepress.vuejs.org/) plugin that provides a global component wrapping [Kano](https://kalisio.github.io/kano/), _a powerful real-time Geovisualizer_.

See this plugin in action [here](http://localhost:8080/kano/guides/advanced-usage.html#integrating-kano) !

## Installation

You can install it with

```bash
yarn add vuepress-plugin-kano
```

And then you just need to register the plugin in your `.vuepress/config.js`:

```js
module.exports = {
    // ...
    plugins: [
        'vuepress-plugin-kano'
    ]
    // ...
}
```

## Usage

The recommended usage is to place your **Kano** declaration as an HTML element:

```md
<kano source="your Kano URL" token="your Kano token" />
```

The tag handles the following attributes:

| Attribute | Description |
| --- | --- |
| `source` | the url to the Kano website. The default value is `https://kano.dev.kalisio.xyz` |
| `token` | the token to be used if you want to be authenticated automatically. There is no default token and if you do not provide any token you have to authenticate yourself. |
| `css-style` | The style to apply to the **iframe**. The default value is `width: 100%; height: 50vh` |

## Contributing

Found a bug ? Missing a Feature ? Want to contribute ? check out our [contribution guidelines](./CONTRIBUTING.md) for details

## Authors

This project is sponsored by 

[![Kalisio](https://s3.eu-central-1.amazonaws.com/kalisioscope/kalisio/kalisio-logo-black-256x84.png)](https://kalisio.com)

## License

This project is licensed under the MIT License - see the [license file](./LICENSE) for details



