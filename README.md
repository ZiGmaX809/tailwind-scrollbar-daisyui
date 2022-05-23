# Scrollbar Plugin for Tailwind CSS And daisyUI
![Tests](https://github.com/adoxography/tailwind-scrollbar/workflows/Tests/badge.svg)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/af892fe4afc048c4860462c5fc736675)](https://www.codacy.com/gh/adoxography/tailwind-scrollbar/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=adoxography/tailwind-scrollbar&amp;utm_campaign=Badge_Grade)

# Update

Fork From [adoxography/tailwind-scrollbar](https://github.com/adoxography/tailwind-scrollbar)

1. Updated to support TailwindCss 3.x, mainly for the `rounded` property.
2. Support [daisyUI](https://github.com/saadeghi/daisyui).So you can use properties like `scrollbar-thumber-base-300` with this plugin,but the property `scrollbar-thumber-base-300/50` what to transform opacity is not supported.The main purpose is to change the scrollbar color according to the theme color when switching themes, but it is not guaranteed to be available in other component libraries as well.

### 简体中文
1. 升级支持Tailwind 3.x，主要是有关于`rounded`属性。
2. 支持了daisyUI的颜色库，所以你现在可以使用类似于`scrollbar-thumber-base-300`这样的颜色属性，但是不支持透明度`scrollbar-thumber-base-300/50`的调整。主要是为了切换主题时根据主题颜色变更滚动条颜色，但是不保证在其他的组件库中同样可用。

### Todo
1. Support `opacity`;
   
Adds styling utilities for scrollbars in Firefox and webkit-based browsers.

## Installation

```bash
yarn add -D tailwind-scrollbar-daisyui
```
or

```bash
npm install --save-dev tailwind-scrollbar-daisyui
```

Add it to the plugins array of your Tailwind config.

```js
plugins: [
    // ...
    require('tailwind-scrollbar-daisyui'),
],
```

# Origin ReadMe

## Usage

**NB:** This plugin *styles* scrollbars; it does not force them to appear. Use typical CSS techniques to force content to overflow and trigger a scrollbar.

For every element that you want to style, add either the `.scrollbar` or `.scrollbar-thin` class. You may then add any `scrollbar-track-{color}`, `scrollbar-thumb-{color}` or `hover:scrollbar-thumb-{color}` classes you like. (Note that `hover:scrollbar-thumb-{color}` classes only have effects in webkit-based browsers.)

Here's a minimal example (keeping in mind that the `h-32` and `h-64` classes are just there to force the scrollbar to appear):

```html
<div class="h-32 scrollbar scrollbar-thumb-gray-900 scrollbar-track-gray-100">
    <div class="h-64"></div>
</div>
```

A live version of this demo [can be found here](https://tailwind-scrollbar-example.adoxography.repl.co/).

## Configuration

If you'd like to add variants for the scrollbar utilities (e.g. [dark mode](https://tailwindcss.com/docs/dark-mode)), add them to the `variants` object in your Tailwind config:

```js
variants: {
    // ...
    scrollbar: ['dark']
}
```

This plugin also capable of adding utilties for creating rounded scrollbars (by referencing your configured [border radius](https://tailwindcss.com/docs/border-radius#customizing) settings). However, as they are only supported in Webkit-based browsers, their usage is inadvisable in cross-browser applications. To enable rounded scrollbar utilities, add `'rounded'` to the list of scrollbar variants in your config file. This will add utilities such as `scrollbar-thumb-rounded` or `scrollbar-thumb-rounded-md`.

## License

This project is licensed under the [MIT License](/LICENSE).
