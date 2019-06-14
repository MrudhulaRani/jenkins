# Task #

This Document would provide basic knowledge about this repository


### What is this repository for? ###
This is small application in reactjs prepared with Jenkinsfile

### How to buid application ###

* make sure to have node.js installed.
* install npx to node.js
* create your application with npx
* build your application with npm
* move into your specific application folder
* start your application

``` npm start ```


### Jenkinsfile Steps ###

The below steps explain how teh cicd will get processed.

* Make sure to have integration with installed jenkins by creating service/webhook in settings of this repository.

* Make sure to have GITScm polling enabled from Jenkins job. So that once commit, the build will get started automatically.

* From Jenkinsfile, It clones the repository first.

* Then it build the application (this can be pushed to artifactory if configured)

* Then last stage it runs the application. (This jenkinsfile runs app in jenkins server only, can be configured the deployment on different server also)


### Want to Dockerize this ###

Follow below steps to dockerize the application

* Once you create project and build, make sure prepare dockerfile and add the below steps.
```
    1. Pull the imange required by FROM option.
    2, COPY the required package into Docker after building the app.
    3, Then add the required command to run the app by Using ENTRYPOINT

```

* then build the image and make sure have proper tag.

* Push the image to registry (can be Docker Hub/ECR/NEXUS)

* Pull teh image to deploy on target platform.



#Good Day.