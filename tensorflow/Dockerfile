FROM tensorflow/tensorflow:latest-gpu

WORKDIR /usr/src/app

# Install python dependencies
ADD requirements.txt .
RUN pip3 install -U pip setuptools && pip3 install -r requirements.txt

EXPOSE 8888
CMD [ "jupyter", "lab", "--ip=0.0.0.0", "--port=8888", "--allow-root" ]
