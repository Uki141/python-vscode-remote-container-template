FROM python:3

USER root

WORKDIR /usr/src/app

# COPY ./requirements.txt ./
# RUN pip install --no-cache-dir -r requirements.txt

COPY . /usr/src/app

ARG GID
ARG UID
RUN groupadd -g ${GID} docker\
 && useradd -u ${UID} -g ${GID} -s /bin/bash -m docker

USER docker

CMD [ "python3", "./main.py" ]