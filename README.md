# WordPress WP-CLI Commands

## General Commands

### Core Management
- `wp core download` - Download WordPress core files.
- `wp core install --url=example.com --title="My Site" --admin_user=admin --admin_password=pass123 --admin_email=admin@example.com` - Install WordPress using the provided configuration.
- `wp core version` - Check the installed WordPress version.
- `wp core update` - Update WordPress to the latest version.

### Plugin Management
- `wp plugin list` - List all installed plugins.
- `wp plugin install hello-dolly` - Install the Hello Dolly plugin.
- `wp plugin activate hello-dolly` - Activate the Hello Dolly plugin.
- `wp plugin deactivate hello-dolly` - Deactivate the Hello Dolly plugin.
- `wp plugin delete hello-dolly` - Delete the Hello Dolly plugin.

### Theme Management
- `wp theme list` - List all installed themes.
- `wp theme install twentysixteen` - Install the Twenty Sixteen theme.
- `wp theme activate twentysixteen` - Activate the Twenty Sixteen theme.
- `wp theme delete twentysixteen` - Delete the Twenty Sixteen theme.

### Post Management
- `wp post list` - List all posts.
- `wp post create --post_type=post --post_title="My New Post" --post_status=publish` - Create a new post.
- `wp post update 123 --post_title="Updated Post Title"` - Update an existing post with ID 123.
- `wp post delete 123` - Delete the post with ID 123.

### User Management
- `wp user list` - List all users.
- `wp user create john john@example.com --role=author --user_pass=pass123` - Create a new user named John.
- `wp user delete 456` - Delete the user with ID 456.

### Option Management
- `wp option get blogname` - Get the value of the "blogname" option.
- `wp option update blogname "My Site"` - Update the value of the "blogname" option.

## Database Commands

- `wp db export --add-drop-table backup.sql` - Export the WordPress database.
- `wp db import backup.sql` - Import a database backup file.
- `wp db search "example"` - Search for a string in the database.
- `wp db optimize` - Optimize the WordPress database.
- `wp db repair` - Repair the WordPress database.

## Multisite Commands

- `wp site list` - List all sites in a multisite network.
- `wp site create --slug=subsite --title="Subsite" --email=admin@example.com` - Create a new subsite in a multisite network.
- `wp site delete 2` - Delete a subsite from a multisite network.
- `wp site switch 2` - Switch to a subsite in a multisite network.

## Additional Commands

### Cache Management
- `wp cache flush` - Flush the WordPress object cache.

### Rewrite Management
- `wp rewrite flush` - Flush the rewrite rules.

### Transient Management
- `wp transient delete transients_example` - Delete a transient.

### Menu Management
- `wp menu create "Main Menu"` - Create a new menu.
- `wp menu list` - List all menus.
- `wp menu location list` - List available menu locations.
- `wp menu location assign <menu> <location>` - Assign a menu to a specific location.
- `wp menu item add-custom <menu> "Custom Link" "http://example.com"` - Add a custom link to a menu.
- `wp menu item add-post <menu> <post-id>` - Add a post to a menu.
- `wp menu item delete <menu-item-id>` - Delete a menu item.

### Widget Management
- `wp widget list` - List all available widgets.
- `wp widget add text sidebar-1 --title="My Widget" --text="This is my widget content"` - Add a text widget.
- `wp widget delete text-123` - Delete a specific widget by its ID.

### Import/Export Commands
- `wp import example.xml --authors=create` - Import content from an XML file.
- `wp export --dir=exports --post_type=post --post_status=publish` - Export posts to a directory.
- `wp search-replace 'http://oldsite.com' 'http://newsite.com' --precise --dry-run` - Perform a search and replace operation on the database.
- `wp cron event list` - List scheduled cron events.
- `wp cron event run my_custom_event` - Run a specific custom cron event.

### Language Management
- `wp language core install es_ES` - Install the language pack for WordPress core.
- `wp language plugin install my-plugin es_ES` - Install the language pack for a specific plugin.
- `wp language theme install my-theme es_ES` - Install the language pack for a specific theme.
- `wp language core update` - Update the language pack for WordPress core.
- `wp language plugin update my-plugin` - Update the language pack for a specific plugin.
- `wp language theme update my-theme` - Update the language pack for a specific theme.

