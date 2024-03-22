# Syntactically Awesome Stylesheets (SASS)

> `SASS`, which stands for **Syntactically Awesome Stylesheets**, is a `CSS` *(Cascading Style Sheets)* preprocessor, a scripting language that extends CSS by allowing developers to write code in one language and then compile it into CSS.

## Overview

At No Clocks, LLC, we use `SASS` for styling UI components and to streamline our `CSS` development process.

`SASS` introduces several key features that make writing `CSS` more efficient and maintainable, including variables, nested syntax, reusable methods and functions, and imports and partials.

## Overview

`SASS` is a stylesheet language that's compiled into `CSS`. It allows you to use variables, nested rules, mixins, functions, and more, all with a fully `CSS`-compatible syntax. `SASS` helps keep large stylesheets well-organized and makes it easy to share design elements across different stylesheets making it
easy to design withing and across projects.

## Resources

- [SASS Official Website](https://sass-lang.com/)
- [SASS Documentation](https://sass-lang.com/documentation)
- [SASS Basics](https://sass-lang.com/guide)

## Advantages

Firstly, SASS introduces the use of variables in your stylesheets. This means you can define a value once, such as a color or font stack, and then use it throughout your stylesheet, making your CSS easier to maintain and change.

Secondly, SASS allows for the use of nested syntax. This means you can nest your CSS selectors in a way that follows the same visual hierarchy of your HTML, making your code easier to read and maintain.

Thirdly, SASS provides the ability to write reusable methods and functions. These can be used to reduce the amount of code you need to write and make your stylesheets more readable.

Lastly, SASS supports the use of imports and partials, allowing you to split your CSS into smaller, more manageable chunks, and then import them into a single, compiled stylesheet. This can greatly improve the organization and maintainability of your code.

`SASS` provides several key advantages over traditional `CSS`:

1. **Variables**: `SASS` introduces the use of variables in your stylesheets. This means you can define a value once, such as a color or font stack, and then use it throughout your stylesheet, making your CSS easier to maintain and change.

2. **Nested Syntax**: `SASS` allows for the use of nested syntax. This means you can nest your CSS selectors in a way that follows the same visual hierarchy of your HTML, making your code easier to read and maintain.

3. **Reusable Methods and Functions**: `SASS` provides the ability to write reusable methods and functions. These can be used to reduce the amount of code you need to write and make your stylesheets more readable.

4. **Imports and Partials**: `SASS` supports the use of imports and partials, allowing you to split your CSS into smaller, more manageable chunks, and then import them into a single, compiled stylesheet. This can greatly improve the organization and maintainability of your code.

In summary, `SASS` is a powerful tool that can help streamline your `CSS` development process, making your code more efficient, maintainable, and readable.

## Installation

To start using `SASS`, you need to install the `SASS` compiler on your system. The `SASS` compiler is a command-line tool that compiles `SASS` code into `CSS`.

You can install the `SASS` compiler using `npm` (Node Package Manager) by running the following command:

```bash
npm install -g sass
```

This will install the `SASS` compiler globally on your system, allowing you to compile `SASS` code into `CSS` from the command line.

## Usage

To compile a `SASS` file into `CSS`, you can use the `sass` command followed by the path to your `SASS` file and the path where you want to output the compiled `CSS` file.

For example, if you have a `styles.scss` file in your project directory and you want to compile it into `styles.css`, you can run the following command:

```bash
sass styles.scss styles.css
```

This will compile the `styles.scss` file into `styles.css`, which you can then include in your HTML file to apply the styles to your web page.

## Example

In your project's `assets` or `styles` directory, you can create a new folder for `sass`. Inside this folder, you can create a `SASS` file, such as `styles.scss`, and write your `SASS` code in it. Another option is to create a `SASS` file for each component or section of your web application and then import them into a main `SASS` file.

Example file structure:

```plaintext
styles/
  styles.css
  sass/
    components/
      _header.scss
      _footer.scss
    core/
      _base.scss
      _fonts.scss
      _keyframes.scss
      _mixins.scss
    elements/
      _buttons.scss
    pages/
      _home.scss
    resets/
      _normalize.scss
      _reset-local.scss
    variables/
      _colors.scss
      _elements.scss
      _typography.scss
    _main.scss
```

In this example, we have a `styles` directory with a `sass` subdirectory that contains various `SASS` files organized by components, core styles, elements, resets, and variables. The `_main.scss` file is the main `SASS` file that imports all the other `SASS` files and compiles them into a single `CSS` file.

### `_main.scss`

Individual `SASS` files are imported into the `_main.scss` file using the `@import` directive. The `_main.scss` file is then imported into the project's primary `App.scss` file or compiled directly into a `CSS` file.

Example `_main.scss` file:

```scss
// _main.scss

@import 'core/base';
@import 'core/fonts';
@import 'core/keyframes';
@import 'core/mixins';

@import 'variables/colors';
@import 'variables/elements';
@import 'variables/typography';

@import 'resets/normalize';
@import 'resets/reset-local';

@import 'elements/buttons';

@import 'components/header';

@import 'pages/home';
```

In this example, the `_main.scss` file imports various `SASS` files that define core styles, variables, resets, elements, components, and pages. This allows you to organize your stylesheets into smaller, more manageable files and import them into a single, compiled `CSS` file.

### `core`

The `core` directory contains `SASS` files that define core styles, such as base styles, fonts, keyframes, and mixins. These files can be imported into the `_main.scss` file to apply core styles to your web application.

- `_base.scss`: Defines base styles for `HTML` elements.
- `_fonts.scss`: Defines font styles used in your project.
- `_keyframes.scss`: Defines keyframe animations used in your project.
- `_mixins.scss`: Defines reusable mixins and functions used in your project.

Example `_base.scss` file:

```scss
// _base.scss

html {
  font-size: 16px;
}

body {
  font-family: 'Arial', sans-serif;
  line-height: 1.5;
  color: #333;
}

h1, h2, h3, h4, h5, h6 {
  font-weight: bold;
}
```

In this example, the `_base.scss` file defines base styles for `HTML` elements, such as the font size, family, and color for the `body` element, as well as the font weight for heading elements (`h1` to `h6`).

Example `_fonts.scss` file:

```scss
// _fonts.scss

@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');
```

In this example, the `_fonts.scss` file imports the `Roboto` font from Google Fonts and applies it to your web application.

Example `_keyframes.scss` file:

```scss
// _keyframes.scss

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
```

In this example, the `_keyframes.scss` file defines a `fadeIn` keyframe animation that fades an element from `opacity: 0` to `opacity: 1`.

Example `_mixins.scss` file:

```scss
// _mixins.scss

@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

In this example, the `_mixins.scss` file defines a `flex-center` mixin that applies `display: flex`, `justify-content: center`, and `align-items: center` styles to an element. This mixin can be reused throughout your project to center elements using flexbox.

### `components`

The `components` directory contains `SASS` files that define styles for reusable UI components, such as headers, footers, cards, and modals. These files can be imported into the `_main.scss` file to apply styles to these components.

- `_header.scss`: Defines styles for the header component used in your project.

Example `_header.scss` file:

```scss
// _header.scss

.header {
  background-color: #333;
  color: #fff;
  padding: 1rem;
}
```

In this example, the `_header.scss` file defines a `.header` class with styles for a header component. The header has a background color of `#333`, text color of `#fff`, and padding of `1rem`.

### `pages`

The `pages` directory contains `SASS` files that define styles for specific pages or sections of your web application. These files can be imported into the `_main.scss` file to apply styles to these pages.

- `_home.scss`: Defines styles for the home page of your project.

Example `_home.scss` file:

```scss
// _home.scss

.home {
  background-color: #f0f0f0;
  padding: 2rem;
}
```

In this example, the `_home.scss` file defines a `.home` class with styles for the home page of your web application. The home page has a background color of `#f0f0f0` and padding of `2rem`.

### `resets`

The `resets` directory contains `SASS` files that define CSS resets, such as `normalize.css` or custom resets for your project. These files can be imported into the `_main.scss` file to apply the resets to your web application.

- `_normalize.scss`: Contains the `normalize.css` reset styles.
- `_reset-local.scss`: Contains custom reset styles specific to your project. This particular example provides cross-browser consistency in the default styling of `HTML` elements.

Example `_normalize.scss` file:

```scss
// _normalize.scss

@import url('https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css');
```

In this example, the `_normalize.scss` file imports the `normalize.css` reset styles from a CDN (Content Delivery Network) and applies them to your web application.

Example `_reset-local.scss` file:

```scss
// _reset-local.scss

html,
body,
div,
span,
applet,
object,
iframe,
h1,
h2,
h3,
h4,
h5,
h6,
p,
blockquote,
pre,
a,
abbr,
...
```

### `variables`

The `variables` directory contains `SASS` files that define variables for colors, elements, typography, and other design elements used in your project. These files can be imported into the `_main.scss` file to define global variables that can be reused throughout your stylesheets.

- `_colors.scss`: Defines color variables used in your project.
- `_elements.scss`: Defines element variables, such as spacing, borders, and shadows.
- `_typography.scss`: Defines typography variables, such as font families, sizes, and weights.

Example `_colors.scss` file:

```scss
// _colors.scss

$primary-color: #007bff;
$secondary-color: #6c757d;
$success-color: #28a745;
$danger-color: #dc3545;
$warning-color: #ffc107;
$info-color: #17a2b8;
```

In this example, the `_colors.scss` file defines color variables that can be used throughout your project. For example, the `$primary-color` variable is set to `#007bff`, which can be used to define the primary color of your web application.

### `elements`

The `elements` directory contains `SASS` files that define styles for common UI elements, such as buttons, forms, and navigation bars. These files can be imported into the `_main.scss` file to apply styles to these elements.

- `_buttons.scss`: Defines styles for buttons used in your project.

Example `_buttons.scss` file:

```scss
// _buttons.scss

.button {
  display: inline-block;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  font-weight: 600;
  text-align: center;
  text-transform: uppercase;
  border: 1px solid transparent;
  border-radius: 0.25rem;
  background-color: $primary-color;
  color: #fff;
  cursor: pointer;
  transition: background-color 0.3s ease;

  &:hover {
    background-color: darken($primary-color, 10%);
  }
}
```

In this example, the `_buttons.scss` file defines a `.button` class with styles for a button element. The button has a background color of `$primary-color` and changes to a darker shade when hovered over.

## Conclusion

`SASS` is a powerful tool that can help streamline your `CSS` development process by introducing variables, nested syntax, reusable methods and functions, and imports and partials. By using `SASS`, you can write more efficient, maintainable, and readable `CSS` code, making it easier to style your web applications.

For more information on `SASS`, you can refer to the official [SASS documentation](https://sass-lang.com/documentation).
