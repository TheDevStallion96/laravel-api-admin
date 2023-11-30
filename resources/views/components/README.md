# Components

### Text Input
1. Component
```php
<!-- resources/views/components/TextInput.blade.php -->

<div>
    <label for="{{ $name }}">{{ $label }}</label>
    <input type="{{ $type }}" id="{{ $name }}" name="{{ $name }}" value="{{ $value ?? '' }}">
</div>
```
2. Usage
```php
<x-TextInput label="Username" name="username" type="text" />
```