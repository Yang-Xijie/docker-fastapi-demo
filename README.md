# FastAPI Get Started

- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [FastAPI in Containers](https://fastapi.tiangolo.com/deployment/docker/)

## development

```sh
pip3 install -r requirements.txt

uvicorn main:app --reload
```

<http://localhost:8000> & <http://localhost:8000/docs>

## production

```sh
sudo docker build --tag service0:v0.0.1 .
sudo docker run --detach --name service0test --publish 1234:80 service0:v0.0.1
```

- `docker build`
    - Usage:  docker build [OPTIONS] PATH | URL | -
    - Build an image from a Dockerfile
    - `-t, --tag list` Name and optionally a tag in the 'name:tag' format
- `docker run`
    - Usage:  `docker run [OPTIONS] IMAGE [COMMAND] [ARG...]`
    - Run a command in a new container
    - `-d, --detach`                         Run container in background and print container ID
    - `--name string`                    Assign a name to the container
    - `-p, --publish list` Publish a container's port(s) to the host

<http://server_ip:1234> & <http://server_ip:1234/docs>
