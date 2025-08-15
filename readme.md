
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
