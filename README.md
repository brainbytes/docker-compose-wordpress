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

### Shut it Down

```
docker-compose down
```

## To Install docker

1. Google it
1. Follow the instructions you found

### Quick Note About Windows
You must enable sharing for your local drive in Docker settings -> Shared Drives before volume 
persistance works.