# Components

### Text Input


The TextInput Laravel Blade component seamlessly integrates a labeled input field into your views, enhancing form development. It includes error handling, dynamically adjusting the UI to highlight input errors. Streamline your user experience with this component, promoting efficient data entry and robust form validation in Laravel applications.
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
```php
<x-TextInput label="Username" name="username" type="text" />
```