FROM "nixos/nix"

ADD default.nix /home/${USER}/default.nix

ENTRYPOINT [ "nix-shell", "--pure", "/home/${USER}/default.nix" ]