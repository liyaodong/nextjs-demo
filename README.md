# Nextjs antdesign dynamic theme demo

## Live example

Default: [nextjs.liyaodong.com](http://nextjs.liyaodong.com)

Dark: [darknextjs.liyaodong.com](http://darknextjs.liyaodong.com)

Red: [rednextjs.liyaodong.com](http://rednextjs.liyaodong.com)

## How to customize
Refer to `pages/index.tsx` #getThemeFromHostName function

```
function getThemeFromHostName(context) {
  let theme = 'default';

  // only run on client side
  if (!process.browser) {
    return theme;
  }

  // can be an api call as well
  if (/dark/i.test(window.location.hostname)) {
    theme = 'dark';
  }

  if (/red/i.test(window.location.hostname)) {
    theme = { '@primary-color': '#ff0000' };
  }

  return theme;
}
```

## Major plugin used
[next-dynamic-antd-theme](https://github.com/OhYee/next-dynamic-antd-theme)

[//]: <> (Force trigger deploy)
