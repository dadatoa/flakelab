dashboard: nix run .#glance -- --config glance/config.yml
consul: export NIXPKGS_ALLOW_UNFREE=1 && nix run --impure .#consul agent -- -node server1 -data-dir=./consul -ui -client 0.0.0.0 -server -bootstrap -advertise 100.85.101.149
gitea: nix run .#gitea -- -C gitea/custom -c gitea/config web
