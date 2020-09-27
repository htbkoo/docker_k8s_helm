FROM tensorflow/tensorflow:latest-gpu

WORKDIR /usr/src/app

# Install python dependencies
ADD requirements.txt .
RUN pip3 install -U pip setuptools && pip3 install -r requirements.txt

# Install node and npm
# Reference: https://github.com/nodesource/distributions/blob/master/README.md#installation-instructions
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -
  && apt-get install -y nodejs

# Install git
RUN apt install -y git-all

EXPOSE 8888
CMD [ "jupyter", "lab", "--ip=0.0.0.0", "--port=8888", "--allow-root" ]
