# Components

### Text Input
1. Component
```bash
php artisan make:component Inputs/TextInput --view
```

 ```php
<!-- resources/views/components/TextInput.blade.php -->

<div>
    <label for="{{ $name }}">{{ $label }}</label>
    <input 
        type="{{ $type }}" 
        id="{{ $name }}" 
        name="{{ $name }}" 
        value="{{ $value ?? old($name) }}" 
        class="{{ $errors->has($name) ? 'border-red-500' : '' }}"
    >
    
    @if ($errors->has($name))
        <p class="text-red-500">{{ $errors->first($name) }}</p>
    @endif
</div>
 ```
2. Usage
 ```php
<x-TextInput label="Username" name="username" type="text" />
 ```