FROM "alpine"

ADD default.nix /home/${USER}/default.nix

RUN sh <(curl -L https://nixos.org/nix/install) --daemon

ENTRYPOINT [ "nix-shell", "--pure", "/home/${USER}/default.nix" ]
