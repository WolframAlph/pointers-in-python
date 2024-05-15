# pointers-in-python

git clone https://github.com/python/cpython \
cd cpython

## docker setup
docker pull wolframalph/cpython-env \
docker run --rm -d --name=cpython --volume=$(pwd):/workspaces/cpython -w /workspaces/cpython --platform=linux/amd64 wolframalph/cpython-env sleep infinity

## compile python
./configure --with-pydebug \
make -j
