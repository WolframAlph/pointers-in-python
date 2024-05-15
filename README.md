# pointers-in-python

git clone https://github.com/python/cpython \
cd cpython \
git checkout v3.9.0

## docker setup
docker pull wolframalph/cpython-env \
docker run --rm -d --name=cpython --volume=$(pwd):/workspaces/cpython -w /workspaces/cpython --platform=linux/amd64 wolframalph/cpython-env sleep infinity \
docker exec -it cpython /bin/bash

## get patches
git clone https://github.com/WolframAlph/pointers-in-python \
cp -r pointers-in-python/patches/ patches \
rm -rf pointers-in-python/

## compile python
./configure --with-pydebug \
make -j
