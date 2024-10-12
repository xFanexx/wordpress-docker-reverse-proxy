# Increase `upload_max_filesize` in `.htaccess` for WordPress

## Step 1: Change the `.htaccess` in the Docker Container

Run the following command to add the `upload_max_filesize` setting to the `.htaccess` file in your container:

```bash
docker container exec -it YOUR_CONTAINER_ID bash -c "echo 'php_value upload_max_filesize 512M' >> /var/www/html/.htaccess && echo 'php_value post_max_size 512M' >> /var/www/html/.htaccess && echo 'php_value memory_limit 512M' >> /var/www/html/.htaccess"

