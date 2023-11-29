# Components

```php
<!-- resources/views/components/TextInput.blade.php -->

<div>
    <label for="{{ $name }}">{{ $label }}</label>
    <input type="{{ $type }}" id="{{ $name }}" name="{{ $name }}" value="{{ $value ?? '' }}">
</div>
```