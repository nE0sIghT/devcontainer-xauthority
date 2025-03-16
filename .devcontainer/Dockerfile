FROM debian:12
SHELL ["/bin/bash", "-exo", "pipefail", "-c"]


RUN apt-get update ;\ 
    apt-get -y install \
        bash-completion \
        sudo \
        x11-apps \
    ;\
    apt-get autoremove -y ;\
    apt-get clean -y ;\
    rm -rf /var/lib/apt/lists/* /tmp/library-scripts/ ;\
    adduser --disabled-password --gecos '' vscode ;\
    echo "vscode ALL=(root) NOPASSWD: ALL" > /etc/sudoers.d/vscode

ENTRYPOINT [ "/bin/sh" ]
CMD [ "-c", "sleep infinity" ]
