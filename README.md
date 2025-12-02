# @eik/semantic-release-config

This is a [semantic-release](https://github.com/semantic-release/semantic-release) config to publish Eik modules meant for internal use in the [metrics-js organisation](https://github.com/metrics-js).

This configuration is not related to our [semantic release plugin](https://github.com/metrics-js/semantic-release#readme).

## Plugins

This shareable configuration uses the following plugins:

- [`@semantic-release/commit-analyzer`](https://github.com/semantic-release/commit-analyzer)
- [`@semantic-release/release-notes-generator`](https://github.com/semantic-release/release-notes-generator)
- [`@semantic-release/changelog`](https://github.com/semantic-release/changelog)
- [`@semantic-release/npm`](https://github.com/semantic-release/npm)
- [`@semantic-release/github`](https://github.com/semantic-release/github)
- [`@semantic-release/git`](https://github.com/semantic-release/git)

## Install

```bash
npm install --save-dev semantic-release @eik/semantic-release-config
```

## Usage

In the [semantic-release configuration file](https://github.com/semantic-release/semantic-release/blob/master/docs/usage/configuration.md#configuration):

```js
export default {
	extends: "@eik/semantic-release-config",
};
```

If you add your own plugins you need to include the ones from the shared config.

```js
import config from '@eik/semantic-release-config';

export default {
  extends: '@eik/semantic-release-config',
  plugins: [
    ...config.plugins,
    [
      'extra-plugin',
      { pluginOpts },
    ],
  ],
};
```
