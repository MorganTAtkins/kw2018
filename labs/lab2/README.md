# Lab 2
In this lab we will write a Dockerfile, build a Docker image and Run a Docker container.

Our Docker container will read a remote storage location and display pictures

The `Dockerfile` this should containes this:
[Dockerfile](Dockerfile)

The `requirements.txt` this should contianers this:
[requirements.txt](requirements.txt)

To BUILD our image, run the following commad:
```
docker image build -t simple-picture-unloader --build-arg app_name=get-image .
```

To RUN our image as a Contianer, run the following commad:
```
docker container run -it --rm --name simple-picture-unloader -p 8000:8000 -e AWS_ACCESS_KEY_ID="" -e AWS_SECRET_ACCESS_KEY="" simple-picture-unloader:latest
```
Navigate to the web UI and upload view the Pictures
Link: [simple-picture-unloader](localhost:8000)
