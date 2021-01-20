## MOTD Ansible Role

[![CI](https://github.com/bilalcaliskan/motd-ansible-role/workflows/CI/badge.svg?event=push)](https://github.com/bilalcaliskan/motd-ansible-role/actions?query=workflow%3ACI)

Configures MOTD(Message of the day) on RHEL/CentOS 7/8 servers.

### Requirements

No special requirements. Also note that this role requires root access, so either run
it in a playbook with a global `become: true`, or invoke the role in your playbook like:

```yaml
- hosts: all
  roles:
    - bilalcaliskan.motd
```

### Role Variables
See the default values in [defaults/main.yml](defaults/main.yml). You can overwrite them in [vars/main.yml](vars/main.yml) if neccessary or you can set them while running playbook.

### Dependencies

None

### Example Playbook File

```yaml
- hosts: all
  become: true
  roles:
    - role: bilalcaliskan.motd
      vars:
        message: "{{ YOUR_CUSTOM_MESSAGE }}"
```

### License

MIT / BSD
