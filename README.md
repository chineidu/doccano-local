# Doccano Local Deployment

## Table of Contents

- [Doccano Local Deployment](#doccano-local-deployment)
  - [Table of Contents](#table-of-contents)
  - [Setup](#setup)
    - [Create Virtual Environment](#create-virtual-environment)
    - [Use Project Setup](#use-project-setup)
    - [Run Server](#run-server)
    - [Run Upload Server](#run-upload-server)

## Setup

### Create Virtual Environment

- You can use [UV](https://docs.astral.sh/uv/getting-started/installation/) or venv to create a virtual environment

```sh
# Create virtual environment using uv (it must be installed)
uv init --python 3.11
. .venv/bin/activate

uv add  "marshmallow==3.15"
uv add doccano
```

### Use Project Setup

- Ensure uv is already installed

```sh

# Install project dependencies
uv sync
```

### Run Server

```sh
doccano webserver --port 8000

# Run and save logs in a file (Optional)
doccano webserver --port 8000 > logs.txt 2>&1
```

### Run Upload Server

- In a new terminal, run:

```sh
doccano task  
```
