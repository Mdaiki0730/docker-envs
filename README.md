# Environment by each docker

This repo will help create various environments by using docker.

Also, these only support you in creating an execution environment. You need to write the source code.

## How use it

Find the environment you want to build and do this under that directory.
```bash
docker-compose up -d --build
```

You can also run environment-specific commands inside the container with one of the following.
```bash
docker-compose exec appname sh
commands
```

```bash
docker-compose exec appname bash -c "commands"
```

## Prepared environments
- golang
- jupyter-lab
- laravel
- node.js
- react
- terraform
- wordpress
