# Using AlpineJS persist to save Magewire component data
To persist [Magewire](https://github.com/magewirephp/magewire) component data between page visits, follow these steps:

In your AlpineJS component, use x-data to define the state of your component. Use `$wire.entangle` method to sync the state of AlpineJS and Magewire. Then, add `$persist` to restore the component data after page refresh:
```html
<div x-data="{ count: $persist($wire.entangle('count')) }">
    <button x-on:click="count++">Increment</button>
    <span x-text="count"></span>
</div>
```

```php
<?php declare(strict_types=1);

use Magewirephp\Magewire\Component;

class MagewireCounter extends Component
{
    public $count = 0;
}
```
That's it! Now your Magewire component data will persist between page visits.

See the [Livewire docs on entangle](https://laravel-livewire.com/docs/2.x/alpine-js#sharing-state) for more details.
