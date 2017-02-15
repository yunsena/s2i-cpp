###  Import template      


`oc create -f templates/s2i-cpp.yaml`

### Create app using base C++ image

`oc debianmaster/s2i-cpp~https://github.com/debianmaster/s2i-cpp.git  --context-dir=/echo --name=my-cpp-app`    


###  Creating your own base image   
`oc new-build https://github.com/debianmaster/s2i-cpp.git --context-dir=dockerfiles/builder --strategy=docker --name=s2i-base`
