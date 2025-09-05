# Jupyer Lab 

Dockerized version of Jupyter Lab for Python 3.13. This image **should not** run on production environments, as I configured a passwordless Lab. The image is built for both Intel and AMD architectures.

## Running
This image runs over the `8888` port and the notebooks are stored under `/home/user/projetos` within the container.

Run the following command to start the Jupyter Lab, sharing the `./projetos` directory in the host:
```sh
docker run --restart=always --name jupyter-lab -d -p 8888:8888 -v $(pwd)/projetos:/home/user/projetos hrchlhck/jupyter
```

