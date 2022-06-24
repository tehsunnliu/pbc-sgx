# SGX enabled PBC Library

PBC library with sgx support.

## Build & Install

This library requires SGX compatible GMP library.

### Install GMP

Follow the instructions at [SGX-enabled GMP library](https://github.com/intel/sgx-gmp) to install GMP library. We recommend you not to set the `--prefix` parameter while configuring the library. This will by default install the library uder `/usr/local/` which is the requirement of Kaleido.

### Build SGX-enabled PBC Library

SGX compatible PBC source code can be found under [cess_pbc/pbc](./cess_pbc/pbc). To build the library please follow the instructions below.

You may set the following environment before executing the following commands

```bash
export SGX_TSTDC_CPPFLAGS=-I/usr/local/include
```

```bash
cd cess_pbc/pbc
./bootstrap
./configure
make
make install
```
