# Livewire

### Livewire Attribute

Suppose you are using [Livewire](https://livewire.laravel.com) and need to debug the  `properties`, `events`, `queries` and `validation errors` a certain component executes. In that case, you should add an attribute to the component's class:

```php
use LaraDumps\LaraDumps\Livewire\Attributes\Ds;

#[Ds]  // [!code ++]
class FiltersTable extends \Livewire\Component 
{
    public function mount() 
    {
        // ..
    }
}
```

### Volt function

```php
\Livewire\Volt\title('todo');

booted(fn() => ds($this));  // [!code ++]

state([
    'todo' => ''
]);

// ...
```

Now, every time the component is updated, the information will be sent to LaraDumps.

#### Profile

![Output](/_media/livewire/profile.png)

#### Propeties

![Output](/_media/livewire/properties.png)


::: info
* LaraDumps can only listen to components if you put the attribute on each component
* The following features will be sent: `properties, queries, profile, events (dispatches) and validation errors`
  :::

