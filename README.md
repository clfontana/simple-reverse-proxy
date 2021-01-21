# Overview
This project is a sample Nginx service listens for requests at port 8080, for
understand reverse-proxy pattern (Udacity Nanodegree Cloud Development exercise) 

Any requests with endpoints prefixed with /api/ will be redirected to the 
Kubernetes service my-app-2-svc 
[simple-express image](https://github.com/clfontana/simple-express.git). 

my-app-2-svc is a name that our Kubernetes cluster recognizes internally.

# docker file
Dockerfile for the reverse-proxy is very simple:

FROM nginx

COPY nginx.conf /etc/nginx/nginx.conf

We don’t need to worry about installing Ngnix dependencies so we take advantage of the base image
