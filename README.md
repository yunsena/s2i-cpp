###  Import template      


`oc create -f templates/s2i-cpp.json`

### Create app using base C++ image

`oc new-app debianmaster/s2i-cpp:latest~https://github.com/debianmaster/s2i-cpp.git --context-dir=/echo --name=my-cpp-app --strategy=source`

###  Creating your own base image   
`oc new-build https://github.com/debianmaster/s2i-cpp.git --context-dir=dockerfiles/builder --strategy=docker --name=s2i-base`
