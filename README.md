# Theme Development Helpers

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat&colorA=338fbb&colorB=1c1c1c&logoColor=ffffff)](/.github/CONTRIBUTING.md)
[![Discord Shield](https://img.shields.io/discord/983602196493004820?style=flat&colorA=338fbb&colorB=1c1c1c&label=discord&logo=discord&logoColor=ffffff)](https://discord.gg/blanklob-community-983602196493004820)

[Contributing](#contributing) |
[License](#license)

A growing collection of useful helpers and fully functional, ready-made utils for Liquid theme development. If you make a snippet that is generic enough to be useful to others, think about [CONTRIBUTING](./CONTRIBUTING.md).

## Usage

Copy the code from the snippet you want to use and paste it into your theme's snippets folder. Then include the snippet in your theme's sections.

```liquid
{% render 'snippet-name' %}
```

### Theme App Extensions

For theme app extensions, you can do the same thing as above, but instead of section, you include theme in your app blocks.

## Tools

### Development screen indicator

A simple indicator that shows if you are on a development screen. Useful for debugging and development.

Built with [Tailwind CSS](https://tailwindcss.com/) and can be added on the `theme.liquid` layout file.

```liquid
{% liquid 
    if settings.enable_development_mode
        render 'development-screen-indicator' 
    endif
%}
```

An example setting to enable the development screen indicator:

```json
{
    "type": "checkbox",
    "id": "enable_development_mode",
    "label": "Enable development mode",
    "default": false
}
```

## Metas

### Social share

A social share to render all necessary meta tags for social sharing.

```liquid
{% render 'social-share' %}
```

You can check Shopify recommandations on social sharing [here](https://help.shopify.com/manual/online-store/images/showing-social-media-thumbnail-images).

## Contributing

We'd love your help! Please read our [contributing guide](./CONTRIBUTING.md) to learn about our development process, how to propose bug fixes and improvements.

## License

Copyright (c) 2023-present Odestry. See [LICENSE](/LICENSE.md) for further details.
