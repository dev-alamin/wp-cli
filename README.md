# WordPress WP-CLI Commands

## General Commands

### Core Management

```bash
wp core download
wp core install --url=example.com --title="My Site" --admin_user=admin --admin_password=pass123 --admin_email=admin@example.com
wp core version
wp core update
```

### Plugin Management

```bash
wp plugin list
wp plugin install hello-dolly
wp plugin activate hello-dolly
wp plugin deactivate hello-dolly
wp plugin delete hello-dolly
```

### Theme Management

```bash
wp theme list
wp theme install twentysixteen
wp theme activate twentysixteen
wp theme delete twentysixteen
```

### Post Management

```bash
wp post list
wp post create --post_type=post --post_title="My New Post" --post_status=publish
wp post update 123 --post_title="Updated Post Title"
wp post delete 123
```

### User Management

```bash
wp user list
wp user create john john@example.com --role=author --user_pass=pass123
wp user delete 456
```

### Option Management

```bash
wp option get blogname
wp option update blogname "My Site"
```

## Database Commands

```bash
wp db export --add-drop-table backup.sql
wp db import backup.sql
wp db search "example"
wp db optimize
wp db repair
```

## Multisite Commands

```bash
wp site list
wp site create --slug=subsite --title="Subsite" --email=admin@example.com
wp site delete 2
wp site switch 2
```

## Additional Commands

### Cache Management

```bash
wp cache flush
```

### Rewrite Management

```bash
wp rewrite flush
```

### Transient Management

```bash
wp transient delete transients_example
```

### Menu Management

```bash
wp menu create "Main Menu"
wp menu list
wp menu location list
wp menu location assign <menu> <location>
wp menu item add-custom <menu> "Custom Link" "http://example.com"
wp menu item add-post <menu> <post-id>
wp menu item delete <menu-item-id>
```

### Widget Management

```bash
wp widget list
wp widget add text sidebar-1 --title="My Widget" --text="This is my widget content"
wp widget delete text-123
```

### Import/Export Commands

```bash
wp import example.xml --authors=create
wp export --dir=exports --post_type=post --post_status=publish
wp search-replace 'http://oldsite.com' 'http://newsite.com' --precise --dry-run
wp cron event list
wp cron event run my_custom_event
```

### Language Management

```bash
wp language core install es_ES
wp language plugin install my-plugin es_ES
wp language theme install my-theme es_ES
wp language core update
wp language plugin update my-plugin
wp language theme update my-theme
```
```
