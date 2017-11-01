# PHP-Composer

Docker image based on `php:7.1-cli-alpine`and adds Composer, Git, Unzip, Zip.

## Usage

Go to directory of project and run this command

```bash
docker run --rm \
    -v $(pwd):/tmp \
    -w /tmp \
    -u $(id -u):$(id -g) \
    ferri/php-composer \
    composer install
```

You can replace `$(pwd)` with your actual path directory if you are not in the current working directory.

If you don't mind running composer with `root` user, then you can remove `-u $(id -u):$(id -g)`.