CPPSP - C++ server pages
=========
For documentation see http://xa.us.to/cppsp

To clone this repo:
```
git clone --recursive https://github.com/xaxaxa/cppsp.git
```
**Make sure the --recursive flag is included, as there are dependent submodules.**

To compile and install:

```
autoreconf &&
./configure --enable-websocket &&
make -j2 &&
sudo make install
```

To run cppsp with example pages:
```
cd examples
./run_example
```
OR:
```
./run_example -m dir_list.cppsm
```
... to enable directory listing.


