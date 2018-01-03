# Lab 1 
In this lab we will inspect a Dockerfile, build a Docker image and Run a Docker container.

The `Dockerfile` this should containes this:
[Dockerfile](Dockerfile)

The `requirements.txt` this should contianers this:
[requirements.txt](requirements.txt)

To BUILD our image, run the following commad:
```
docker image build -t simple-picture-uploader --build-arg app_name=simple-uploader .
```

To RUN our image as a container, run the following commad:
```
docker container run -it --name simple-picture-uploader -e MINIO_ACCESS_KEY=accesskey -e MINIO_SECRET_KEY=secretkey -e MINIO_URL=kw2018-minio.svc.ecs.digital -p 7000:8000 simple-picture-uploader:latest
```
Navigate to the web UI and upload some Pictures
Link: [simple-picture-uploader](localhost:7000)
