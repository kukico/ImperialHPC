

Please Review first: [RCS main Website: Tensorflow](https://www.imperial.ac.uk/admin-services/ict/self-service/research-support/rcs/support/applications/tensorflow/)  

and integrate with the following:

**NOTES :**

- **GPU computational libraries and drivers** (`CUDA`, `cuDNN`, - possibly others?! - ) may be needed in your SW stack and environment (i.e either provided by your locally installed SW -e.g. your build via anaconda- or by loading the correct modules from the HPC-provided environment-modules available.)  

- The relevant **Nvidia drivers** are already installed on all GPU nodes.  
Using the newest `cuda module` is recommended, as these are known to be compatible with the installed drivers.


example:  
for a full list of available cuda-drivers/libraries module versions try:

```
module avail cuda
module avail cudnn
```   

---

### Anaconda-based TF/TF-GPU installations


TensorFlow provides multiple APIs.
The lowest level API, TensorFlow Core provides you with complete programming control.

- the **Base package** contains only tensorflow with CPU integration    <!-- not tensorflow-tensorboard.  -->  
- the **Base GPU package** contains only tensorflow for GPU integration    <!-- not tensorflow-tensorboard.  -->


[Tensorflow](https://anaconda.org/search?q=tensorflow)  - VS - [Tensorflow-GPU](https://anaconda.org/search?q=tensorflow-gpu)

some examples are reported below:  

- conda-forge / tensorflow 2.8.1 :  `conda install -c conda-forge tensorflow`


- anaconda / packages / tensorflow-base 2.6.0 :  `conda install -c anaconda tensorflow-base`




- anaconda / packages / tensorflow-gpu 2.6.0 : `conda install -c anaconda tensorflow-gpu`  


- anaconda / packages / tensorflow-gpu-base 1.8.0 : `conda install -c anaconda tensorflow-gpu-base`




## (UN)common Warning and errors

`W tensorflow/core/common_runtime/bfc_allocator.cc:456] Allocator (GPU_0_bfc) ran out of memory trying to allocate `  

`W tensorflow/core/kernels/gpu_utils.cc:49] Failed to allocate memory for`   


If the cause is memory fragmentation maybe the environment variable `TF_GPU_ALLOCATOR=cuda_malloc_async` will improve the situation.  


See this link [TF docs](https://www.tensorflow.org/guide/gpu#limiting_gpu_memory_growth) for the topics :   

- Limiting GPU memory growth  

- Using a single GPU on a multi-GPU system  









---

Refs:

