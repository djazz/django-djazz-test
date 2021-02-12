# Installation

## Prerequisites

- **Virtual Environment:** [`Python 3`](https://www.python.org/downloads/), [`pyenv`](https://github.com/pyenv/pyenv).
- **Docker:** [`Docker`](https://docs.docker.com/get-docker/).


## The Easy Way

```bash
cd <PROJECT_DIR>
./dj install
```


## The Hard Way

### Virtual Environment

```bash
cd <PROJECT_DIR>

# Create virtual environment.
python -m venv .venv
source .venv/bin/activate

# Make CLI tools available in PATH.
cd .venv/bin/
ln -s ../../dj
ln -s ../../manage.py
cd - &> /dev/null

# Install dependencies.
pip install --upgrade pip setuptools
pip install -r requirements/local.txt

# Create database.
./bin/db-create.sh
manage.py migrate
```


### Docker

```bash
cd <PROJECT_DIR>

# Create the images.
mkdir -p docker/app/build
cp -a requirements docker/app/build/
docker-compose -p "<PROJECT_SLUG>" -f "docker/local.yml" build
rm -fr docker/app/build

# Create and run the containers.
docker-compose -p "<PROJECT_SLUG>" -f "docker/local.yml" up -d "$@"

# Install dependencies.
docker-compose -p "<PROJECT_SLUG>" -f "docker/local.yml" exec app pip install --upgrade pip setuptools
docker-compose -p "<PROJECT_SLUG>" -f "docker/local.yml" exec app pip install -r "/app/requirements/local.txt"

# Create database.
docker-compose -p "<PROJECT_SLUG>" -f "docker/local.yml" exec app python manage.py migrate
```
