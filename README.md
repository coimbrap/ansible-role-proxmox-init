# Ansible role PVE

Configuration de base pour Proxmox.

/!\ Non testé pour le moment.

Inspiration : https://github.com/lae/ansible-role-proxmox

### host_vars/pve/pve.yml
```yaml
pve_groups:
  - name: adminsys
    comment: Elukerio Adminsys
pve_users:
  - name: mablr@pam
    firstname: mablr
    groups: [ "adminsys" ]
  - name: coimbrap@pam
    firstname: coimbrap
    groups: [ "adminsys" ]
pve_acls:
  - path: /
    roles: [ "Administrator" ]
    groups: [ "adminsys" ]

deploy_ssh_keys: true
```

### License

GPLv3 - Elukerio

### Author Information

Pierre Coimbra
