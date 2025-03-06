## Consul

Commande pour lancer consul depuis le flake. L'adresse IP est celle de l'interfce de Tailscale pour le node.

```bash
export NIXPKGS_ALLOW_UNFREE=1 && nix run --impure .#consul agent -- -node server1 -data-dir=./consul -ui -client 0.0.0.0 -server -bootstrap -advertise 100.85.101.149

```

Pour réduire la longueur de la commande, j'ai mis un alias `nixconsul` qui passe la commande 

```bash
alias nixconsul "export NIXPKGS_ALLOW_UNFREE=1 && nix run --impure .#consul agent"

```
