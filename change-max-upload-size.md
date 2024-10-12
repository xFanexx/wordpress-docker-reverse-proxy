# Increase `upload_max_filesize` in `.htaccess` for WordPress

## Step 1: Change the `.htaccess` in the Docker Container

Run the following command to add the `upload_max_filesize` setting to the `.htaccess` file in your container:

```bash
docker container exec -it 0406abd88da0f14fb13e0ee2c87eb9aa23869abe9a0d226897ef1daaf1633768 bash -c "echo 'php_value upload_max_filesize 512M' >> /var/www/html/.htaccess && echo 'php_value post_max_size 512M' >> /var/www/html/.htaccess && echo 'php_value memory_limit 512M' >> /var/www/html/.htaccess"
