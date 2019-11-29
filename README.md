# golang_blas
use go to do numeric maths computing by BLAS

## install gonum and netlib
```
$go get -u gonum.org/v1/gonum/...
$go get -d gonum.org/v1/netlib/...
```

## run bench with openblas and 4 threads
```
OMP_NUM_THREADS=4 CGO_LDFLAGS="-lopenblas" go test  -benchtime 5s -bench .
```

## run bench with MKL and 4 threads
```
$source /opt/intel/bin/compilervars.sh intel64
$OMP_NUM_THREADS=4 CGO_LDFLAGS="-lmkl_rt" go test  -benchtime 5s -bench .
```
