# Sass

Chanel Mepschen heeft het over Sass gehad en dat zij dat bij Triple gebruiken. Ik wilde het ook in sommige projecten gaan gebruiken, vandaar dat ik er een artikel over heb geschreven. De rest zal ik in het engels schrijven, omdat de meeste bronnen in het engels zijn geschreven.

# What is Sass?

Sass stands for Syntactically Awesome Stylesheet and is an extensions to CSS. It is written in `.scss` files. Sass is a CSS pre-processor, which means that it lays on top of CSS and will be compiled into CSS.

# Why use Sass?

According to w3schools: "Sass lets you use features that do not exist in CSS, like variables, nested rules, mixins, imports, inheritance, built-in functions, and other stuff". It also has a fully CSS-compatible syntax.

You can use Tailwind with Sass, which supports mixins. Some people use a combination of Sass and Tailwind to add more customizability to their projects. With this combination, you can use Sass to create custom mixins that uses Tailwind's classes, allowing you to customize your elements further. This enables you to take advantage of the power of both libraries and keep the design consistent and efficient.

The reason why we're using Sass is to customize our styling furthen than if we were to use Tailwind alone.

# How to use Sass

I'll explain on how to use Sass.

## Installing Sass

First we have to install Sass. You can install Sass in different ways, but this is how to install it the pure Javascript implementation of Sass, which can run slower than other options. You can install it by typing the following line in the console: `npm install -g sass`.

## Preprocessing

In order for Sass to be read, these files first need be to compiled into CSS files, before they can be used on the web. To do this, we can `watch` individual files or directories with the `--watch` flag. This will look for changes in the Sass file and re-compiles it into CSS whenever a change has been found, or in other words: when you save it.

On the [documentation](https://sass-lang.com/guide) it is stated that "you can watch and output to directories by using folder paths as your input and output, and separating them with a colon. In this example: `sass --watch app/sass:public/stylesheets`. Sass would watch all files in the app/sass folder for changes, and compile CSS to the public/stylesheets folder."

You can also download the "Live Sass Compiler" as extension, you don't have to use the CLI. Just make sure you have this enabled. You can check this by looking at the bottom of your screen in your code editor where it will say "Watch Sass", this means the extension is disabled OR "Watching", this means the extension is enabled.

### Compressing

To compress your Sass files, you can use the following line in your terminal:

`sass --watch --style=compressed public/style/style.scss:public/style/style.css`

## Variables

With Sass variables, you can store things like colors or any CSS value that you want to reuse. You can use the `$` symbol to make something a variable.

This is how it looks in `.SCSS` files:

```

$font-stack: Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}

```

This is how it looks in `.CSS` files:

```

body {
  font: 100% Helvetica, sans-serif;
  color: #333;
}

```

## Nesting

Sass also makes it possible to nest your CSS selectors, like so:

This is how it looks in `.SCSS` files:

```

nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}

```

This is how it looks in `.CSS` files:

```

nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
nav li {
  display: inline-block;
}
nav a {
  display: block;
  padding: 6px 12px;
  text-decoration: none;
}

```

## Partials

In this [documentation](https://sass-lang.com/guide) it is stated that you can create partial Sass files, by using an underscore, like so: `_partial.scss`. The underscore lets Sass know that the file is only a partial and should not be generated into a CSS file. Partials are used with the `@use` rule.

Using partials is a good way to modularize your CSS and help keep things easier to maintain.

## Modules

Like mentioned earlier, you can use partials with Sass, by using the `@use` rule. According to the [documentation](https://sass-lang.com/guide) "this rule loads another Sass file as a module, which means you can refer to its variables, mixins, and functions in your Sass file with a namespace based on the filename. Using a file will also include the CSS it generates in your compiled output".

This is how it looks in `.SCSS` files:

```

// file 1: _base.scss
$font-stack: Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}

// file 2: styles.scss
@use 'base';

.inverse {
  background-color: base.$primary-color;
  color: white;
}

```

This is how it looks in `.CSS` files:

```

body {
  font: 100% Helvetica, sans-serif;
  color: #333;
}

.inverse {
  background-color: #333;
  color: white;
}

```

## Mixins

According to the [documentation](https://sass-lang.com/guide) "mixin lets you make groups of CSS declarations that you want to reuse throughout your site. It helps keep your Sass very DRY. You can even pass in values to make your mixin more flexible. Here's an example for theme".

This is how it looks in `.SCSS` files:

```

SCSS SYNTAX
@mixin theme($theme: DarkGray) {
  background: $theme;
  box-shadow: 0 0 1px rgba($theme, .25);
  color: #fff;
}

.info {
  @include theme;
}
.alert {
  @include theme($theme: DarkRed);
}
.success {
  @include theme($theme: DarkGreen);
}

```

This is how it looks in `.CSS` files:

```

.info {
  background: DarkGray;
  box-shadow: 0 0 1px rgba(169, 169, 169, 0.25);
  color: #fff;
}

.alert {
  background: DarkRed;
  box-shadow: 0 0 1px rgba(139, 0, 0, 0.25);
  color: #fff;
}

.success {
  background: DarkGreen;
  box-shadow: 0 0 1px rgba(0, 100, 0, 0.25);
  color: #fff;
}

```

# Sources

- https://www.w3schools.com/sass/sass_intro.php
- https://sass-lang.com/install
