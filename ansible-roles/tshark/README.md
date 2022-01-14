Role tshark
=========

This role installs tshark tool wich is a CLI like wireshark


Requirements
------------

No Requirements

Role Variables
--------------

```yaml
# Role behavior:
tshark_group:               the tshark group name
                            tshark
tshark_package:             install package tshark for ubuntu
                            tshark
system_capture_dir:         system capture directory
                            /var/capture
tshark_log_dir:             log directory used by tshark
                            /var/log/tshark
tshark_capture_dir:         capture directory for pcap files created by tshark
                            "{{ system_capture_dir }}/tshark"

nfs_artifact_wireshark_dir: mount directory for outside exports
                            /mnt/nfs/wireshark

setup_tshark_service:       setup tshark as a service. This need scripts from file
                            true

tshark_group_members:       add tshark_group_members like vagrant
  vagrant:
    state: present
```

Dependencies
------------

In combination with nfs.client as longs as capture shall be exported outside.

Example Playbook
----------------

```yaml
- name: setup tshark
  hosts: all
  become: true
  roles:
    - tshark
```


License
-------

MIT

Author Information
------------------

raibru


