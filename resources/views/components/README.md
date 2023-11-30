# Components

### Text Input


The <code>TextInput</code> Laravel Blade component seamlessly integrates a labeled input field into your views, enhancing form development. It includes error handling, dynamically adjusting the UI to highlight input errors. Streamline your user experience with this component, promoting efficient data entry and robust form validation in Laravel applications.
- Artisan Command
```bash
php artisan make:component Inputs/TextInput --view
```
- Component Code
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
- Usage
```php
<x-TextInput label="Username" name="username" type="text" />
```
---
### Button

The "Button" Laravel Blade component streamlines button creation with a clean interface. Easily customize styles, such as background color, text, and font weight, by leveraging Tailwind CSS classes. Simplify your views with this reusable component, enhancing code readability and promoting consistency across your Laravel project.
```bash
php artisan make:component Button
```
```php
<!-- resources/views/components/Button.blade.php -->

<button {{ $attributes->merge(['class' => 'bg-blue-500 text-white font-bold py-2 px-4 rounded']) }}>
    {{ $slot }}
</button>
```
```php
<x-Button>
    Click me
</x-Button>
```