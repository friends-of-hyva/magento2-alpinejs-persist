# FriendsOfHyva_AlpineJsPersist
This is a Magento module specifically for Hyvä, which adds the [AlpineJS persist plugin](https://alpinejs.dev/plugins/persist) to [Hyvä](https://www.hyva.io/). This plugin allows you to persist Alpine.js component data between page reloads.

## Alpine.js Persist Plugin
The Alpine.js persist plugin is a plugin that allows you to persist Alpine.js component data between page reloads. This plugin can be used to store data associated with Alpine.js components in the browser's local storage or session storage, allowing it to be retrieved and restored when the user returns to the page.

For more information on how to use the AlpineJS persist plugin, please refer to the [official Alpine.js documentation](https://alpinejs.dev/plugins/persist).

## Example
To use the persist plugin in your Hyvä theme, you can add the `$persist` property to your Alpine.js component and specify which data properties should be persisted.

```html
<div x-data="{ count: $persist(0) }">
    <button x-on:click="count++">Increment</button>
    <span x-text="count"></span>
</div>
```

In this Alpine.js example, the count property is initialized with a default value of 0 using the `$persist` function, which enables the property to persist its value between page reloads using local storage.

## Installation
To install the FriendsOfHyva_AlpineJsPersist module via composer, run the following command:

``` bash
composer require friends-of-hyva/magento2-alpinejs-persist
```

**This module requires Hyvä theme 1.2.0 or higher and AlpineJS v3.**

## Using AlpineJS persist to save Magewire component data
[See more details here.](docs/magewire.md)

## Note
This module is made specifically for Hyvä and doesn't work with native Magento.

For more information on Hyvä, please visit the [official Hyvä website](https://hyva.io/).

## Copyright & License

Copyright (c) 2023 Friends of Hyvä

The module is released under the [MIT](LICENSE.txt).
