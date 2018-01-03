FROM alpine:latest

# Arguments are variables available at build time
ARG app_name

# Install python and pip
RUN apk --no-cache add py-pip

# Copy files required for the app to run
COPY $app_name.py /usr/src/app/
COPY requirements.txt /usr/src/app/

# Install Python modules needed by the Python app
RUN pip install --no-cache-dir -r /usr/src/app/requirements.txt

# Create Images and Maylogs directories
RUN mkdir /maylogs /images

EXPOSE 8000
ENV app $app_name

# Run the application
ENTRYPOINT python /usr/src/app/$app.py
