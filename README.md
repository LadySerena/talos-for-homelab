# talos homelab

1. setup dhcp reservations in router
2. generate config
   - `talosctl gen config home-cluster https://kubernetes.serenacodes.casa:6443 -o rendered/melchior.yaml --with-secrets ./secrets/secrets.yaml --config-patch @patches/cni.patch --config-patch @patches/kernel.patch.yaml --output-types controlplane --config-patch-control-plane @patches/melchior.patch --force`
3. apply-config
4. bootstrap etcd (first node)
5. install cni
   - `cilium install --version 1.15.6`

## TODO

- makefile for generating manifests
- prometheus for monitoring
- makefile for generating talos machine config

## Docs

- [talos linux](https://www.talos.dev/v1.7/)
- [cilium](https://docs.cilium.io/en/stable/)
