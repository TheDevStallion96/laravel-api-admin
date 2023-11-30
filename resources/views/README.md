# Default View

```php
<x-app-layout>
    <x-slot name="header">
        {{ __('Dashboard') }}
    </x-slot>

    {{-- TODO: Add an Alert component section --}}

    <div class="p-4 bg-white rounded-lg shadow-xs">
        {{ __('You are logged in!') }}
    </div>
</x-app-layout>
```