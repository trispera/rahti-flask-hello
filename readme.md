# Test

> [!IMPORTANT]  
> Bitnami is changing its policy regarding their catalog starting August 28th 2025. Read more [here](https://github.com/bitnami/containers/issues/83267)  
> - Current images will be moved to [Bitnami Legacy Repository](https://hub.docker.com/u/bitnamilegacy) with no more updates.  
> - Some images will still be available in the [Bitnami Secure Images](https://hub.docker.com/u/bitnamisecure) but only with the `latest` tag.  
> - To continue to receive images with the latest updates and access to different tags, you need to subscribe to the full version of Bitnami Secure Images: https://www.arrow.com/globalecs/uk/products/bitnami-secure-images/  
> The Helm Charts that we provide are now meant for testing/development purposes.  
> However, the Bitnami project continues to make its source code available at [bitnami/containers](https://github.com/bitnami/containers) under the Apache 2 license. It is possible to build the image and then push to your CSC project. More information on how to push images [here](https://docs.csc.fi/cloud/rahti/images/Using_Rahti_integrated_registry/)

# Demo: Flask hello-world in Rahti

This simple application will display all JPG photos located in the '/static' folder.

## Quickstart

Create new application with source-to-image tools:
```bash
oc new-app https://github.com/cscfi/rahti-flask-hello --name="course-flask-demo"
```

Create the route for the application
```bash
oc create route edge --service=course-flask-demo --insecure-policy='Redirect' --port=8080
```
