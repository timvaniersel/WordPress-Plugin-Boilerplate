=== Plugin Name ===
Contributors: (this should be a list of WordPress.org usernames)
Donate link: https://example.com/
Tags: boilerplate, developer, plugin
Requires at least: 6.6
Tested up to: 6.9
Requires PHP: 7.4
Stable tag: 0.1.0
License: GPL v2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

A standardized, organized foundation for building WordPress plugins.

== Description ==

This boilerplate provides a loader-based plugin structure, separate admin and public classes, translation scaffolding, and an uninstall entrypoint.

Before releasing a real plugin, replace all placeholder values in this scaffold:

* Plugin name, slug, text domain, and class names
* Version and support requirements
* URIs, author details, and readme content
* Any placeholder assets, hooks, or views you do not need

The scaffold does not enqueue admin or front-end assets by default. Register those hooks only when your plugin has a screen or feature that requires them.

If you distribute outside WordPress.org, add a unique `Update URI` header to the main plugin file.

If your plugin depends on another WordPress.org plugin, add the `Requires Plugins` header to the main plugin file.

Since WordPress 5.8, WordPress.org reads `Requires at least` and `Requires PHP` from the main plugin file, so keep those values current in `plugin-name.php`.

== Installation ==

1. Rename the `plugin-name` directory to your plugin slug.
2. Rename identifiers throughout the codebase to match your plugin:
   `plugin_name` -> `your_plugin_slug`
   `plugin-name` -> `your-plugin-slug`
   `Plugin_Name` -> `Your_Plugin_Name`
   `PLUGIN_NAME_` -> `YOUR_PLUGIN_NAME_`
3. Update `plugin-name.php` with your real plugin metadata.
4. Upload the renamed plugin directory to `/wp-content/plugins/`.
5. Activate the plugin through the "Plugins" screen in WordPress.
6. Add your plugin-specific hooks, admin screens, and front-end behavior.

== Frequently Asked Questions ==

= Why are the admin and public assets not loading by default? =

Because boilerplate code should not enqueue empty CSS or JavaScript files on every request. Load assets only when your plugin actually needs them.

= Where should I declare plugin requirements? =

Use the main plugin header in `plugin-name.php` for `Requires at least`, `Requires PHP`, `Update URI`, and `Requires Plugins`.

== Changelog ==

= 0.1.0 =
* Refreshed the boilerplate to align with current WordPress plugin metadata and development practices.
