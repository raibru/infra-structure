Role setup.nfs.server
=========

This role installs NFS server 


Requirements
------------

No Requirements

Role Variables
--------------

```yaml
# Role behavior:
nfs_package:        install latest package nfs-kernel-server in server node
                    nfs-kernel-server
nfs_service:        nfs package name as used service
                    nfs-kernel-server
nfs_artifacts_dirs: list of artifacts directories used under current inventory host name
                    - wireshark
                    - logs
                    - session
                    - archive
nfs_export_dir:     directory name wich shell be exportet for NFS
                    /mn/nfs
nfs_export_params:  used NFS export parameter
                    "*(rw,all_squash,insecure,async,no_subtree_check,anonuid=1000,anongid=1000)"
```

Dependencies
------------

In combination with setup.nfs.client.
**First** use this role and than setup.nfs.client role

Example Playbook
----------------

```yaml
- name: setup nfs server 
  hosts: all
  become: true
  roles:
    - setup.nfs.server
```


License
-------

MIT

Author Information
------------------

raibru

