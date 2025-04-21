> <span style="color:red;">CMake Error at /home/jetson/cmake-3.27.9-linux-aarch64/share/cmake-3.27/Modules/FindPackageHandleStandardArgs.cmake:230 (message):
  Could NOT find CUDA (missing: CUDA_NVCC_EXECUTABLE) (Required is exact
  version "10.2")
Call Stack (most recent call first):
  /home/jetson/cmake-3.27.9-linux-aarch64/share/cmake-3.27/Modules/FindPackageHandleStandardArgs.cmake:600 (_FPHSA_FAILURE_MESSAGE)
  /home/jetson/cmake-3.27.9-linux-aarch64/share/cmake-3.27/Modules/FindCUDA.cmake:1291 (find_package_handle_standard_args)
  /usr/lib/aarch64-linux-gnu/cmake/opencv4/OpenCVConfig.cmake:86 (find_package)
  /usr/lib/aarch64-linux-gnu/cmake/opencv4/OpenCVConfig.cmake:108 (find_host_package)
  CMakeLists.txt:23 (find_package)</span>

Значит, что opencv не может найти cuda. Нужно явно указать:
```
export CUDA_TOOLKIT_ROOT_DIR=/usr/local/cuda-10.2
export PATH=$CUDA_TOOLKIT_ROOT_DIR/bin:$PATH
export LD_LIBRARY_PATH=$CUDA_TOOLKIT_ROOT_DIR/lib64:$LD_LIBRARY_PATH
export CUDNN_INCLUDE_DIR=/usr/local/cuda-10.2/include
export CUDNN_LIB_DIR=/usr/local/cuda-10.2/lib64
```
