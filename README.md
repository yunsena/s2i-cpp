> Import template
`oc create -f templates/s2i-cpp.yaml`


> Creating your own base image   
`oc new-build https://github.com/debianmaster/s2i-cpp.git --context-dir=dockerfiles/builder --strategy=docker --name=s2i-base`
