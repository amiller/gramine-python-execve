
## Building for Linux

Run `make SGX=1` or `make` in the directory. Gramine is required, but SGX is not required to build.

Note the makefile builds `scripts/hello.c` as an elf binary

## Run with and without SGX

First the obvious way

```
python3 scripts/execve.py

```

Then run with the gramine loader
```
gramine-direct python scripts/execve.py
```

Finally the real deal with SGX
```
gramine-sgx python scripts/execve.py
```
