# WordPress WP-CLI Commands

## General Commands

### Core Management

- Download WordPress core files:
  ```bash
  wp core download
  ```

- Install WordPress using the provided configuration:
  ```bash
  wp core install --url=example.com --title="My Site" --admin_user=admin --admin_password=pass123 --admin_email=admin@example.com
  ```

- Check the installed WordPress version:
  ```bash
  wp core version
  ```

- Update WordPress to the latest version:
  ```bash
  wp core update
  ```

### Plugin Management

- List all installed plugins:
  ```bash
  wp plugin list
  ```

- Install the Hello Dolly plugin:
  ```bash
  wp plugin install hello-dolly
  ```

- Activate the Hello Dolly plugin:
  ```bash
  wp plugin activate hello-dolly
  ```

- Deactivate the Hello Dolly plugin:
  ```bash
  wp plugin deactivate hello-dolly
  ```

- Delete the Hello Dolly plugin:
  ```bash
  wp plugin delete hello-dolly
  ```

### Theme Management

- List all installed themes:
  ```bash
  wp theme list
  ```

- Install the Twenty Sixteen theme:
  ```bash
  wp theme install twentysixteen
  ```

- Activate the Twenty Sixteen theme:
  ```bash
  wp theme activate twentysixteen
  ```

- Delete the Twenty Sixteen theme:
  ```bash
  wp theme delete twentysixteen
  ```

### Post Management

- List all posts:
  ```bash
  wp post list
  ```

- Create a new post:
  ```bash
  wp post create --post_type=post --post_title="My New Post" --post_status=publish
  ```

- Update an existing post with ID 123:
  ```bash
  wp post update 123 --post_title="Updated Post Title"
  ```

- Delete the post with ID 123:
  ```bash
  wp post delete 123
  ```

### User Management

- List all users:
  ```bash
  wp user list
  ```

- Create a new user named John:
  ```bash
  wp user create john john@example.com --role=author --user_pass=pass123
  ```

- Delete the user with ID 456:
  ```bash
  wp user delete 456
  ```

### Option Management

- Get the value of the "blogname" option:
  ```bash
  wp option get blogname
  ```

- Update the value of the "blogname" option:
  ```bash
  wp option update blogname "My Site"
  ```

## Database Commands

- Export the WordPress database:
  ```bash
  wp db export --add-drop-table backup.sql
  ```

- Import a database backup file:
  ```bash
  wp db import backup.sql
  ```

- Search for a string in the database:
  ```bash
  wp db search "example"
  ```

- Optimize the WordPress database:
  ```bash
  wp db optimize
  ```

- Repair the WordPress database:
  ```bash
  wp db repair
  ```

## Multisite Commands

- List all sites in a multisite network:
  ```bash
  wp site list
  ```

- Create a new subsite in a multisite network:
  ```bash
  wp site create

 --slug=subsite --title="Subsite" --email=admin@example.com
  ```

- Delete a subsite from a multisite network:
  ```bash
  wp site delete 2
  ```

- Switch to a subsite in a multisite network:
  ```bash
  wp site switch 2
  ```

## Additional Commands

### Cache Management

- Flush the WordPress object cache:
  ```bash
  wp cache flush
  ```

### Rewrite Management

- Flush the rewrite rules:
  ```bash
  wp rewrite flush
  ```

### Transient Management

- Delete a transient:
  ```bash
  wp transient delete transients_example
  ```

### Menu Management

- Create a new menu:
  ```bash
  wp menu create "Main Menu"
  ```

- List all menus:
  ```bash
  wp menu list
  ```

- List available menu locations:
  ```bash
  wp menu location list
  ```

- Assign a menu to a specific location:
  ```bash
  wp menu location assign <menu> <location>
  ```

- Add a custom link to a menu:
  ```bash
  wp menu item add-custom <menu> "Custom Link" "http://example.com"
  ```

- Add a post to a menu:
  ```bash
  wp menu item add-post <menu> <post-id>
  ```

- Delete a menu item:
  ```bash
  wp menu item delete <menu-item-id>
  ```

### Widget Management

- List all available widgets:
  ```bash
  wp widget list
  ```

- Add a text widget:
  ```bash
  wp widget add text sidebar-1 --title="My Widget" --text="This is my widget content"
  ```

- Delete a specific widget by its ID:
  ```bash
  wp widget delete text-123
  ```

### Import/Export Commands

- Import content from an XML file:
  ```bash
  wp import example.xml --authors=create
  ```

- Export posts to a directory:
  ```bash
  wp export --dir=exports --post_type=post --post_status=publish
  ```

- Perform a search and replace operation on the database:
  ```bash
  wp search-replace 'http://oldsite.com' 'http://newsite.com' --precise --dry-run
  ```

- List scheduled cron events:
  ```bash
  wp cron event list
  ```

- Run a specific custom cron event:
  ```bash
  wp cron event run my_custom_event
  ```

### Language Management

- Install the language pack for WordPress core:
  ```bash
  wp language core install es_ES
  ```

- Install the language pack for a specific plugin:
  ```bash
  wp language plugin install my-plugin es_ES
  ```

- Install the language pack for a specific theme:
  ```bash
  wp language theme install my-theme es_ES
  ```

- Update the language pack for WordPress core:
  ```bash
  wp language core update
  ```

- Update the language pack for a specific plugin:
  ```bash
  wp language plugin update my-plugin
  ```

- Update the language pack for a specific theme:
  ```bash
  wp language theme update my-theme
  ```
```
