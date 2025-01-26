FROM Ubuntu

RUN apt-get update
RUN apt-get install python

RUN pip install flask
RUN pip install flask-mysql

COPY . /opt/source-code

ENTRYPOINT FLASK_APP=/opt/source-code/app.py flask run

# Build Image command
# docker build Dockerfile -t kamrul/my-custom-app (kamrul =>  my repo name d hub my-custom-app  => image name)

# publish in docker hub
# docker push kamrul/my-custom-app