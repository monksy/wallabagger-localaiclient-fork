# wallabagger-localaiclient-fork

This is an independent fork of Wallabagger that explores configuring AI tag
suggestions on each user's client with an inference provider they choose,
rather than through a centralized AI service. It reflects a different view
about where AI features should run; there is no ill will toward the upstream
project or its maintainers.

AI tag suggestions are not currently an active feature in upstream Wallabagger.
This fork will be archived if upstream adds AI-powered tag suggestions. Until
then, there is no guarantee that this fork will stay current with upstream or
receive future updates.

[Wallabagger Local AI Client Fork](https://github.com/monksy/wallabagger-localaiclient-fork) is a Firefox and Chromium-based browser (Chrome, Vivaldi, Brave…) extension for [wallabag v2](https://wallabag.org), based on [Wallabagger](https://github.com/wallabag/wallabagger).

## What is wallabag?

wallabag is a self hostable application allowing you to not miss any content anymore. More informations on website: [wallabag.org](https://wallabag.org) and [github.com](https://github.com/wallabag/wallabag)

* save the current page
* send the content from a paywalled page to wallabag
* edit the title
* add (with autocomplete!) and remove tags
* set starred and archived status
* delete the page

## Requirement

* [wallabag v2](https://wallabag.org) on server side.
* Firefox or Chromium-based browser (Chrome, Vivaldi, Brave, Edge v48+…)

## Installation

- Chromium-based browsers users can install extension from the [Chrome WebStore](https://chrome.google.com/webstore/detail/wallabagger/gbmgphmejlcoihgedabhgjdkcahacjlj)
- Firefox browsers users can install the extension from [Mozilla add-ons storage](https://addons.mozilla.org/en-US/firefox/addon/wallabagger/)

## Useful links

- [Documentation](https://wallabagger.wallabag.org/)

## Build the Firefox add-on for AMO

The build was verified on Arch Linux (x86_64) with Node.js 26.13.1 and npm
12.2.2. It requires Node.js and npm; the same commands can be run on Linux,
macOS, or Windows. Install Node.js 26.13.1 from
[nodejs.org](https://nodejs.org/); npm 12.2.2 is included. Dependency
installation requires access to the npm registry.

To reproduce the Firefox package, extract the source archive, open a terminal,
and run:

```sh
cd wallabagger-localaiclient-fork
npm ci
npm run build-for-amo
```

The Firefox package is written to `web-ext-artifacts/wallabagger-<version>.zip`,
with the version taken from `package.json`. The build script first generates
the Firefox manifest from `manifest-builder/manifest.mjs`, then packages the
extension with `web-ext`. The extension's first-party JavaScript is not
transpiled, bundled, or minified.

## Many thanks to

* [Yuriy Evdokimov](mailto:rurik19@yandex.ru) for being at the origin of this extension
* [All the wallabag contributors](https://github.com/wallabag/wallabag/graphs/contributors)
* [Yan Zhu](https://github.com/picturepan2) for the [Spectre CSS framework](https://github.com/picturepan2/spectre)

## License

This work is free. You can redistribute it and/or modify it under the terms of the MIT License. See the COPYING file for more details.
