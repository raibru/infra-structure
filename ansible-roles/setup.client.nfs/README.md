Role setup.nfs.client
=========

This role installs NFS client 


Requirements
------------

No Requirements

Role Variables
--------------

```yaml
# Role behavior:
nfs_package:            install latest package nfs-kernel-server in server node
                        nfs-kernel-server
nfs_server_share_point: NFS server exported access point
                        "192.168.59.11:/mnt/nfs"
nfs_remote_mount_point: Mount point with NFS server exported access point plus current client
                        created inventory hostname
                        "{{ nfs_server_share_point}}/{{ inventory_hostname_short }}"
nfs_mount_dir:          NFS mount point
                        /mnt/nfs
nfs_client_dirs:        list of artifact directories used by NFS client 
                        - "/mnt/nfs/wireshark"
                        - "/mnt/nfs/logs"
                        - "/mnt/nfs/session"
                        - "/mnt/nfs/archive"
```

Dependencies
------------

In combination with setup.nfs.server.
**First** use setup.nfs.server and than this role

Example Playbook
----------------

```yaml
- name: setup nfs client 
  hosts: all
  become: true
  roles:
    - setup.nfs.client
```


License
-------

MIT

Author Information
------------------

raibru

