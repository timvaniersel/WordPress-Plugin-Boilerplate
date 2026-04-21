# WordPress Plugin Boilerplate

A loader-based boilerplate for building WordPress plugins without shipping outdated defaults.

## What Changed In This Fork

- Plugin metadata reflects current WordPress header fields, including `Requires at least` and `Requires PHP`.
- The plugin slug stays hardcoded as `plugin-name`, which keeps renaming to a real slug a simple search-and-replace operation.
- Placeholder admin and public assets are opt-in, so the scaffold does not enqueue empty files on every request.
- Composer-based standards tooling is included for PHP_CodeSniffer, WordPress Coding Standards, and PHP compatibility checks.

## Project Structure

- `plugin-name/`: The executable plugin scaffold.
- `plugin-name/admin/`: Admin-specific classes, partials, CSS, and JavaScript.
- `plugin-name/includes/`: Shared plugin classes such as the bootstrap loader and i18n setup.
- `plugin-name/public/`: Front-end classes, partials, CSS, and JavaScript.
- `plugin-name/languages/`: Translation files.

## Getting Started

1. Rename the `plugin-name` directory to your plugin slug.
2. Replace the placeholder identifiers throughout the scaffold:
   `plugin_name` -> `your_plugin_slug`
   `plugin-name` -> `your-plugin-slug`
   `Plugin_Name` -> `Your_Plugin_Name`
   `PLUGIN_NAME_` -> `YOUR_PLUGIN_NAME_`
3. Update the metadata in `plugin-name/plugin-name.php` before release:
   plugin name, URIs, author, version, WordPress version requirement, and PHP version requirement.
4. Update `plugin-name/README.txt` with real distribution details.
5. Register admin or public asset hooks only when your plugin has screens or features that actually need them.

## Quality Checks

Install the dev tools:

```bash
composer install
```

Run PHP lint across the scaffold:

```bash
find plugin-name -name '*.php' -print0 | xargs -0 -n1 php -l
```

Run WordPress coding standards:

```bash
composer lint:phpcs
```

## Distribution Notes

- For private or commercial distribution, add a unique `Update URI` header in `plugin-name/plugin-name.php`.
- If the plugin depends on another WordPress.org plugin, add the `Requires Plugins` header in the same file.
- Since WordPress 5.8, WordPress.org reads `Requires at least` and `Requires PHP` from the main plugin file, not from `readme.txt`.

## License

The boilerplate is licensed under the GPL v2 or later.
