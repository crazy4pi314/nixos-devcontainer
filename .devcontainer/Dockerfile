FROM "alpine"

ENV USER=devcontainer

USER root
RUN useradd -ms /bin/bash ${USER} && mkdir /nix && chown ${USER} /nix
RUN apk update && apk add sudo shadow bash

USER ${USER}
RUN sh <(curl -L https://nixos.org/nix/install) --no-daemon

ADD default.nix /home/${USER}/default.nix

ENTRYPOINT [ "nix-shell", "/home/${USER}/default.nix" ]
