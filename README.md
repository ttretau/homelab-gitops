# homelab-gitops

K8s Homelab automation, running
* Home Assistant
* Nextcloud
* ..

Automation using:
* Flux
* Sops

Based on a lot of stuff from:
https://github.com/k8s-at-home/awesome-home-kubernetes

#Documentation

TBD

```
export KEY_NAME="homelab.tretau.net"
export KEY_COMMENT="flux secrets"

gpg --batch --full-generate-key <<EOF
%no-protection
Key-Type: 1
Key-Length: 4096
Subkey-Type: 1
Subkey-Length: 4096
Expire-Date: 0
Name-Comment: ${KEY_COMMENT}
Name-Real: ${KEY_NAME}
EOF
```

````
gpg --list-secret-keys "${KEY_NAME}"
````
