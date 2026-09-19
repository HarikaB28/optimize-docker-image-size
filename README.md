# optimize-docker-image-size
Optimizing Docker Images with Multi-Stage Builds and Distroless Container Images

With this project we observe how the usage of multi-stage docker builds and distroless container images reduce the docker image size drastically.

we chose a GOLANG application as golang is a statically-typed programming language that does not require a runtime in the traditional sense, unlike dynamically-typed languages like Python, Ruby, and JavaScript, which rely on a runtime environment to execute thier code. Go compiles directly to machine code, which can then be executed directly by the operating system.

The following image shows the output of the "docker image ls" command.
![](./Screenshot%202026-09-19%20144454.png)
