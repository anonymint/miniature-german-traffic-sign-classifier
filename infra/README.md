## Infrastructure as a Code

This is optional but I found it's quite a big deal when you start looking at automation perspective.

In this folder I have include couple of script 

1. Dockerfile to run the notebook and expert to PDF file, due to error with current Jupyter v4.4.0 so the Docker is to solve this issue
```docker
docker build jupyter-docker . 
docker run -it --rm -p 9999:8888 -v $(pwd):/data jupyter-docker /bin/bash

#inside docker you can run jupyter notebook
```

2. Coming soon! - Terraform code to spin up AWS GPU to train the model, it's 10x faster running in the AWS than my laptop. 