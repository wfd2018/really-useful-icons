# Really Useful Icons

The Really Useful Icons set is made up of around 200 icons selected from 6 different icon sets ([Clarity](https://clarity.design/icons/get-started), [Elegant themes](https://www.elegantthemes.com/blog/resources/elegant-icon-font), [Font Awesome v4.x](https://fontawesome.com/v4.7.0/), [Font Awesome v5](https://fontawesome.com/icons?d=gallery&m=free), [IcoMoon](https://icomoon.io/#preview-free) and [Ionicons](https://ionicons.com)).

[Really Useful Icons - Reference Guide](https://argenteum.github.io/really-useful-icons/)

The icon fonts were created using [Fontastic](http://fontastic.me) and the SVG files were generated by the [IcoMoon app](https://icomoon.io/#app-features)

## Getting started

### How to include Really Useful Icons in a regular HTML website
1. [Download the .zip file](https://argenteum.github.io/really-useful-icons/really-useful-v1.zip)
2. Unzip to your website's documents folder
3. Link to the Really Useful Icons stylesheet (`really-useful-icons/ru-style.css`) in your HTML

### How to include Really Useful Icons in your custom WordPress theme
1. [Download the .zip file](https://argenteum.github.io/really-useful-icons/really-useful-v1.zip)
2. Unzip to your theme's folder
3. [Enqueue the stylesheet](https://code.tutsplus.com/tutorials/loading-css-into-wordpress-the-right-way--cms-20402) in your theme's `functions.php` file with `wp_enqueue_style( 'really-useful-icons', get_template_directory_uri() . 'really-useful-icons/ru-style.css' );`

## Using the Icons

Listed below are three ways in you can use Really Useful Icons in your web project.  Icons can be styled (size, colour etc.) in CSS.

### Inline HTML

The easiest way to use the icons is in HTML using the icon class.

Example: `<i aria-hidden="true" class="ru-star"></i>`

You can find a list of the icons and their classes in the [Quick Reference](https://github.com/argenteum/really-useful-icons/blob/master/quick-reference.txt).

### Pseudo-classes in CSS

Imagine that you want to put an icon of a user before your CSS class `.foo`, an icon of a asterisk after your CSS class `.bar` and the icon for a PDF after every link to a PDF file.

You would add the following to your CSS:
```
@supports (font-family: "really-useful") {
.foo::before,
.bar::after,
a[href$=".pdf"]::after {
  display: inline-block;
  font-family: "really-useful";
  font-size: 1em;
  font-style: normal;
  font-variant: normal;
  font-weight: normal;
  line-height: 1;
  text-align: center;
  text-decoration: none;
  text-transform: none;
  speak: none;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
}

.foo::before {
  content: "\e01b";
}

.bar::after {
  content: "\e000";
}

a[href$=".pdf"]::after {
  content: "\e04d";
}
```

### SVG link

Example:
```
  <svg role="img" aria-labelledby="gh" focusable="false" tabindex="-1">
    <title id="gh">Github logo</title>
    <use xlink:href="https://www.yourwebsite.com/really-useful-icons/sprite.svg#github"/>
  </svg>
```

## Accessibility

Remember that icons cannot be read by screen readers.  You should always ensure that information is not conveyed _only_ via icons, for example by adding [visually hidden text for screen readers](https://webaim.org/techniques/css/invisiblecontent/) and by hiding icons using the `aria-hidden="true"` attribute.  

[Creating accessible SVGs](https://www.deque.com/blog/creating-accessible-svgs/)

## License

The copyright and licensing for all the _icons_ in the Really Useful Icons set can be found in detail in the [License document](https://github.com/argenteum/really-useful-icons/blob/master/LICENSE).  Everything else, that is not an icon, is licensed under MIT.
