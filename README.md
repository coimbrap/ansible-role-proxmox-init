# Ansible role - proxmox-init

Ansible role to initialize the PVE configuration
- Deleting subscription messages
- Change of repositories
- Download images / iso
- Users / Groups creation

Inspiration : https://github.com/lae/ansible-role-proxmox

### Example

```yaml
pve_groups:
  - name: adminsys
    comment: Adminsys
pve_users:
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

GPLv3

### Author Information

Pierre Coimbra
