# Bloom - Hex Digital

<p align="center">
  <strong>WordPress starter theme with a modern development workflow</strong>
  <br />
  Built with 🌯 at [Hex Digital](https://www.hexdigital.com)
</p>

## Supporting

**Bloom** is an open source project and completely free to use.

However, we highly appreciate you sending us a postcard from your hometown, mentioning which of our package(s) you are using. You'll find our address [in our website footer](https://www.hexdigital.com/). We publish all received postcards on our virtual postcard wall.

**Bloom** wouldn't be possible without the fantastic work by **Roots**, so please consider supporting them with a [sponsorship](https://www.patreon.com/rootsdev).

## About Bloom

Bloom is an opinionated, productivity-driven WordPress starter theme with a modern development workflow.

We recommend using Bloom if you're looking to spend less time building the same functionality for each project.

Any and all features can be disabled if you prefer, so even if you disagree with some of our opinions, it may still be a good fit for you.

## Features

- Environment variables, powered by [env](oscarotero/env) and [dotenv](https://github.com/vlucas/phpdotenv).
- Image Lazy Loading, powered by [Vanilla LazyLoad](https://github.com/verlok/vanilla-lazyload).

Note that some of the functionality relies on our [functionality plugin, Sprout](https://github.com/hex-digital/sprout). This should be added to your `mu-plugins`.
If any functionality is enable that relies on Sprout, and Sprout is not found, you'll see an error in the WordPress dashboard.

See [the Sage repository](https://github.com/roots/sage) for more features from the underlying framework.

## Requirements

Make sure all dependencies have been installed before moving on:

- [WordPress](https://wordpress.org/) >= 5.4
- [PHP](https://secure.php.net/manual/en/install.php) >= 7.3.0 (with [`php-mbstring`](https://secure.php.net/manual/en/book.mbstring.php) enabled)
- [Composer](https://getcomposer.org/download/)
- [Node.js](http://nodejs.org/) >= 12.14.0
- [Yarn](https://yarnpkg.com/en/docs/install)

## Theme installation

Clone the repo into the `themes` directory of your WordPress installation.

## Theme structure

```sh
themes/your-theme-name/   # → Root of your Sage based theme
├── app/                  # → Theme PHP
│   ├── View/             # → View models
│   ├── Providers/        # → Service providers
│   ├── admin.php         # → Theme customizer setup
│   ├── filters.php       # → Theme filters
│   ├── helpers.php       # → Helper functions
│   └── setup.php         # → Theme setup
├── bootstrap/            # → Acorn bootstrap
│   ├── cache/            # → Acorn cache location (never edit)
│   └── app.php           # → Acorn application bootloader
├── config/               # → Config files
│   ├── app.php           # → Application configuration
│   ├── assets.php        # → Asset configuration
│   ├── filesystems.php   # → Filesystems configuration
│   ├── logging.php       # → Logging configuration
│   └── view.php          # → View configuration
├── composer.json         # → Autoloading for `app/` files
├── composer.lock         # → Composer lock file (never edit)
├── public/               # → Built theme assets (never edit)
├── functions.php         # → Theme bootloader
├── index.php             # → Theme template wrapper
├── node_modules/         # → Node.js packages (never edit)
├── package.json          # → Node.js dependencies and scripts
├── resources/            # → Theme assets and templates
│   ├── fonts/            # → Theme fonts
│   ├── images/           # → Theme images
│   ├── scripts/               # → Theme javascript
│   ├── styles/              # → Theme stylesheets
│   └── views/            # → Theme templates
│       ├── components/   # → Component templates
│       ├── form/         # → Form templates
│       ├── layouts/      # → Base templates
│       └── partials/     # → Partial templates
├── screenshot.png        # → Theme screenshot for WP admin
├── storage/              # → Storage location for cache (never edit)
├── style.css             # → Theme meta information
├── vendor/               # → Composer packages (never edit)
└── webpack.mix.js        # → Laravel Mix configuration
```

## Theme setup

Edit files in `/config` for theme configuration.

Edit `app/setup.php` to enable or disable theme features, setup navigation menus, post thumbnail sizes, and sidebars.

## Theme development

- Run `composer install` from the theme directory to install php dependencies
- Run `yarn` from the theme directory to install front end dependencies
- Copy `.env.example` to `.env`, and update  with your local dev URL for browsersync

### Build commands

- `yarn start` — Compile assets when file changes are made, start Browsersync session
- `yarn hot` — Same as `start` with hot module reloading
- `yarn build` — Compile and optimize the files in your assets directory
- `yarn build:production` — Compile assets for production

## Updating Sage framework

The `upstream` branch tracks Sage 10.

The easiest way to update this theme is to pull in the latest changes from Sage
into the `upstream` branch, then create a PR from `upstream` to `main`.

This will highlight all Sage changes, as well as any conflicts to solve.

## Documentation

Please see the [Sage documentation](https://roots.io/sage/docs/) for the underlying theme.

Documentation for Bloom is in the works.

## Contributing

Contributions are welcome from everyone. 
