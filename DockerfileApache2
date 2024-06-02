FROM httpd

ARG UID
ARG GID
ARG USERNAME
ARG SERVICE

ENV UID ${UID}
ENV GID ${GID}
ENV USERNAME ${USERNAME}

RUN groupadd -g ${GID} ${USERNAME}
RUN useradd -u ${UID} -g ${USERNAME} -m ${USERNAME}

COPY ${SERVICE}/httpd.conf /usr/local/apache2/conf
RUN chown ${USERNAME}:${USERNAME} /usr/local/apache2/logs
