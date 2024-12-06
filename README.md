Install pytorch lib (CPU)

```bash
mkdir libtorch
wget https://download.pytorch.org/libtorch/cpu/libtorch-cxx11-abi-shared-with-deps-2.5.1%2Bcpu.zip
unzip libtorch-cxx11-abi-shared-with-deps-2.5.1+cpu.zip

export LIBTORCH=$(pwd)
export LIBTORCH_INCLUDE=$LIBTORCH
export LIBTORCH_LIB=$LIBTORCH
export LIBTORCH_BYPASS_VERSION_CHECK=1
#export LD_LIBRARY_PATH=/data/rust_tensorflow/libtorch/libtorch/lib:$LD_LIBRARY_PATH
export LD_LIBRARY_PATH=$(pwd)/libtorch/lib:$LD_LIBRARY_PATH

echo $LIBTORCH
#example ==> /data/rust_tensorflow/libtorch/libtorch

```

```bash
cargo run --example tigre model/model.pt model/tigre.jpeg
```
