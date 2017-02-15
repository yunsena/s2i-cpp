###  Import template      
`oc create -f templates/s2i-cpp.json`

### Create app using base C++ image

`oc new-app debianmaster/s2i-cpp:latest~https://github.com/debianmaster/s2i-cpp.git --context-dir=/echo --name=my-cpp-app --strategy=source`

###  Creating your own base image   
`oc new-build https://github.com/debianmaster/s2i-cpp.git --context-dir=dockerfiles/builder --strategy=docker --name=s2i-base`



### Notes
Creating s2i for c++ is pretty straight forward,  select a base image which has all the necessary tools for building c++ application  i.e.    debianmaster/s2i-cpp  or   dockerfiles/builder   
then in your source code create two files  .s2i/bin/run   and .s2i/bin/assemble   
`assemble` tells how to compile and `run` tells how to runt the application.   openshift understand these two files and does your build and run.    
Advanced build contains steps for eliminating the need for having in the build tools in final run time image. check  buildconfigs/advanced folder for more info (not working yet,but will give you idea)


