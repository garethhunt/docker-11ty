# docker-11ty
A simple way of running [11ty](https://www.11ty.dev/) without having to install [node](https://nodejs.org/)

## Build the docker image

```
$ docker build -t <your-image-name> .
```

## Run the image with local src directory as the document root

```
$ docker run -p 3000:3000 -p 3001:3001 -it --mount type=bind,source="$(pwd)"/src,target=/usr/src/app/src <your-image-name>
```

## Edit files

Edit files in the document root and 11ty will transform them to HTML
