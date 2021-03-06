# Google Tag Manager
[![npm](https://img.shields.io/npm/dt/@nuxtjs/google-tag-manager.svg?style=flat-square)](https://www.npmjs.com/package/@nuxtjs/google-tag-manager)
[![npm (scoped with tag)](https://img.shields.io/npm/v/@nuxtjs/google-tag-manager/latest.svg?style=flat-square)](https://www.npmjs.com/package/@nuxtjs/google-tag-manager)

> Add Google Tag Manager (GTM) to your nuxt.js application.
This plugins automatically sends first page and route change events to GTM.

**Note:** google tag manager is not enabled in dev mode.
You can set environment variable `NODE_ENV` to `production` for testing in dev mode.

## Setup
- Add `@nuxtjs/google-tag-manager` dependency using yarn or npm to your project
- Add `@nuxtjs/google-tag-manager` to `modules` section of `nuxt.config.js`
```js
  modules: [
   ['@nuxtjs/google-tag-manager', { id: 'GTM-XXXXXXX' }],
  ]
```

## Options

### `id`
- Required
Should be in form of `GTM-XXXXXXX`

### All options
```js
{
  id: 'GTM-XXXXXXX',
  layer: 'dataLayer',
  pageTracking: false
  query: {
    // query params...
    gtm_auth:        '...',
    gtm_preview:     '...',
    gtm_cookies_win: '...'
  },
  scriptURL: '//example.com'
}
```

### Router Integration

You can optionally set `pageTracking` option to `true` to track page views. 

This is disabled by default to prevent double events when using alongside with Google Analytics so take care before enabling this option.
