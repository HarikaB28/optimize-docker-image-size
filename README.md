# optimize-docker-image-size
Optimizing Docker Images with Multi-Stage Builds and Distroless Container Images

With this project we observe how the usage of multi-stage docker builds and distroless container images reduce the docker image size drastically.

we chose a simple calculator application in GOLANG. 

The following image shows the output of the "docker image ls" command.

![](./Screenshot%202026-09-19%20144454.png)

### 🚀 Image Optimization

By implementing **Multi-Stage Builds** paired with a **Distroless Runtime Image**, the application's container footprint was drastically reduced:

* **Initial Size:** 251 MB (Included heavy Go SDK compilers, package managers, and shell utilities).
* **Optimized Size:** 1.47 MB (Contains strictly the compiled machine-code binary).
* **Reduction:** **~171x smaller** (a **99.41%** reduction in total size).

#### Why Multi-Stage & Distroless Works:

1. **Multi-Stage Build:** Separates the build pipeline from runtime. Large compilers and source files are permanently discarded after producing the binary.
2. **Distroless Base:** Replaces standard OS layers (like Ubuntu/Alpine) with a minimal runtime environment containing no package managers or shells—leaving zero overhead and a microscopic attack surface.



