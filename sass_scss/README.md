Sass makes CSS fun again. Sass is an extension of CSS, adding nested rules, variables, mixins, selector inheritance, and more. It's translated to well-formatted, standard CSS using the command line tool or a plugin for your build system.

$font-stack: Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}

@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
      -ms-border-radius: $radius;
          border-radius: $radius;
}

nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { @include border-radius(10px); }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
Install Sass
You can install Sass on Windows, Mac, or Linux by downloading the package for your operating system from GitHub and adding it to your PATH. That's all—there are no external dependencies and nothing else you need to install.

If you use Node.js, you can also install Sass using npm by running
npm install -g sass

However, please note that this will install the pure JavaScript implementation of Sass, which runs somewhat slower than the other options listed here. But it has the same interface, so it'll be easy to swap in another implementation later if you need a bit more speed!

See the Sass website for more ways to install Sass.

Once you have Sass installed, you can run the sass executable to compile .sass and .scss files to .css files. For example:
sass source/stylesheets/index.scss build/stylesheets/index.css

