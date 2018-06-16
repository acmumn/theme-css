ACM Website Theme
=================

This is the theme for ACM-related websites, extracted into a set of SCSS stylesheets for extensibility. Compiled stylesheets (*.css) will be available with tagged releases.

Usage
-----

This library can be installed through the `npm` repositories. Use your favorite node package manager client to add this library as one of your dev dependencies. This library should be a dev depedency because sources files aren't required during runtime. If you're using the `npm` client, you can add it using

```bash
npm install --save-dev git://github.com/acmumn/theme
```

Alternatively, for yarn, you can add it using

```bash
yarn add -D git://github.com/acmumn/theme
```

Once you have the library installed, you can integrate the stylesheets into your current SCSS workflow. The best way is to import `variables.scss` and `theme.scss` into your main SCSS file. To customize the theme, override anything in `variables.scss` before importing `theme.scss` to use the new variables. For example,

```scss
// First, import variables.scss in case you don't want to override everything.
@import "/path/to/src/variables";

// Here, override whatever you want
// ...
$primaryColor: #a949b6;

// Now, import theme.scss to use the variables in the actual theme.
@import "/path/to/src/theme";
```

It's up to you where you place these files for the imports to work. If you're using `webpack` to compile your scss sheets, you may have the option to use the `~` include operator.

```scss
@import "~acm/src/variables";
```

Happy theming!

Contact
-------

Author: Michael Zhang

License: MIT
