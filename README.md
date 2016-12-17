# docker-compose-wordpress
A simple docker-compose YAML for quickly running WordPress

## Using This Script

### Reference it in your Git Repository

```
$ git submodule add git@github.com:brainbytes/docker-compose-wordpress.git
```

### Run It

```
$ cd docker-compose-wordpress
docker-compose up -d
```

The first time you run this, it might take a while to load especially if you haven't already 
downloaded the images. The next time will be WAY faster though.

### Using WP-CLI

Use `docker exec <containername> wp`, for example `docker exec <containername> wp theme install 
quark`. See the [WP-CLI Docs](http://wp-cli.org/) for more info.

If you're creating a development environment from production data, the [wp 
search-replace](http://wp-cli.org/commands/search-replace/) command may be useful, for example:

```
docker exec <containername> wp search-replace 'http://www.production-url.com' 'http://localhost:8000'
docker exec <containername> wp search-replace 'https://www.production-url.com' 'http://localhost:8000'
```

### Shut it Down

```
docker-compose down
```

## Other Useful Information

### Open a Bash Shell

```
docker ps
sudo docker exec -it [container name or id] bash
```

On Windows:

```
docker ps
winpty docker exec -it [container name or id] bash
```

### To Install docker

On Window:

Download [here](https://docs.docker.com/docker-for-windows/) and be sure to read about the prerequisites. Can't get it working? Try running [this PowerShell script](https://github.com/Microsoft/Virtualization-Documentation/tree/master/windows-server-container-tools/Debug-ContainerHost) to diagnose common issues.

On MacOS:

Download [here](https://docs.docker.com/docker-for-mac/) and have fun. It's easier to get Docker going on MacOS than Windows.

1. Google it
1. Follow the instructions you found

#### Quick Note About Windows

You must enable sharing for your local drive in Docker settings -> Shared Drives before volume 
persistance works.
