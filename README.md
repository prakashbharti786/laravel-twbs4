# Laravel 5.5.x Frontend preset for Boostrap 4

A Laravel frontend preset for [Bootstrap 4](http://getbootstrap.com/) (Beta), the next major version of Bootstrap.

Current version: `^4.0.0-beta.2`

## Installation

You can install this package via composer:

```bash
composer require laravelnews/laravel-twbs4
```
The package will automatically register it's service provider.

Install the basic preset to only update the CSS and JavaScript files:

```bash
php artisan preset bootstrap4
```

Or if you want to install everything, including auth views:

```bash
php artisan preset bootstrap-auth
```

Next, update NPM packages and build the CSS/JavaScript:

```bash
yarn && yarn dev
```

Or via NPM:

```bash
npm install && npm run dev
```

**Important**: Make sure you have a backup of your code. The presets update `package.json`, and replace views, CSS, and JavaScript.

### Variables

The Bootstrap 4 presets include the same familiar `resources/assets/scss/_variables.scss` file, with some updated values to match Bootstrap 4 variable changes. This preset looks similar to the current `3.x` version that ships with Laravel, but isn't identical.

Here are the variables ported over thus far:

```scss
// Body
$body-bg: #fff;

// Borders
$laravel-border-color: darken($body-bg, 10%);
$list-group-border-color: $laravel-border-color;

$card-border-color: $laravel-border-color;

// Brands
$primary: #3097D1;
$info: #8eb4cb;
$success: #2ab27b;
$warning: #cbb956;
$danger: #bf5329;

// Typography
$font-family-sans-serif: "Raleway", sans-serif;
$font-size-base: .875rem; // 14px
$line-height-base: 1.6;
$text-color: #636b6f;

// Inputs
$input-border-color: lighten($text-color, 40%);
$input-placeholder-color: lighten($text-color, 30%);
```

## License

The MIT License (MIT). See [License File](LICENSE.md) for more information.