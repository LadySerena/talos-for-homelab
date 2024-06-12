1. setup dhcp reservations in router
2. generate config
  - talosctl gen config home-cluster https://kubernetes.serenacodes.casa:6443 -o rendered/melchior.yaml --with-secrets ./secrets/secrets.yaml --config-patch @patches/cni.patch --config-patch @patches/kernel.patch.yaml --output-types controlplane --config-patch-control-plane @patches/melchior.patch --force
2. apply-config
3. bootstrap etcd (first node)
4. install cni
