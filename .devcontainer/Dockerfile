ARG     ALPINE_TAG
FROM    alpine:${ALPINE_TAG}

ARG     DOCKER_GROUP_ID
ARG     USER="dev"

RUN     apk add curl doas docker gcc git git-lfs make openssh shadow texlive-full vim && \
        adduser -D ${USER} && \
        addgroup ${USER} docker && \
        groupmod --gid ${DOCKER_GROUP_ID} docker && \
        git config --global core.editor "vim"
