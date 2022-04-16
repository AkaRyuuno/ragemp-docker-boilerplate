FROM ubuntu:20.04 as base

ARG USER_NAME
ARG USER_ID
ARG GROUP_ID

RUN apt-get update \
    && apt-get -y install \
    bash \
    g++6

RUN useradd -m ${USER_NAME} --uid=${USER_ID}

USER ${USER_ID}:${GROUP_ID}

WORKDIR /opt/ragemp-srv
CMD [ "./ragemp-server" ]
