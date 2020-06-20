# Ansible role PVE

Configuration de base pour Proxmox.

/!\ Non testé pour le moment.

### host_vars/pve/pve.yml
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

Licence GPLv3 - Auteur : Pierre Coimbra pour Elukerio

Inspiration : https://github.com/lae/ansible-role-proxmox
