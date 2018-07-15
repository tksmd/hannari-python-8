# Hannari Python #8 Demonstration

This project includes demonstration code for the presentation at [Hannari Python #8](https://hannari-python.connpass.com/event/91757/) at Jul 20th 2018.

## Prerequisites

* Docker

## Start Jupyter

Build docker image as follows. Don't forget the last `.` (dot). This is required only once.

    docker build -t hannari-python-8 .

Then run jupyter notebook like this

    docker run --rm -p 8888:8888 -v $(pwd):/opt/local/work hannari-python-8

To debug docker environment, run bash as follows.

    docker run --rm -ti hannari-python-8 /bin/bash -l

## Run Cython

Requires Python 3.6 or later

    python -m venv venv
    source venv/bin/activate
    pip install -r requirements.lock


# References

* [Jupyter Docker Stacks](https://github.com/jupyter/docker-stacks/)
