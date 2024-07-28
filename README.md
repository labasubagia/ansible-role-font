Font
=========

This role can be used to install font in Linux

Requirements
------------
- Ansible Core >= 2.1
- Linux Distribution
  - Debian >= 10
  - Ubuntu >= 20.04
  - Linux Mint >= 21
> Note: Other distributions likely to work but not been tested

Role Variables
--------------

The following variables will change the behavior of this role (default values are shown below):

```yaml
# Archive font url (usually zip)
font_url: https://github.com/adobe-fonts/source-sans/releases/download/3.052R/TTF-source-sans-3.052R.zip

# Installed font directory
font_dir: "{{ ansible_env.HOME }}/.fonts"

# State of font (present or absent)
font_state: 'present'
```


Example Playbook
----------------
```yaml

- hosts: servers
  roles:
    - role: labasubagia.font
      vars:
        font_url: https://github.com/adobe-fonts/source-sans/releases/download/3.052R/TTF-source-sans-3.052R.zip
        font_dir: ~/.local/share/fonts
        font_state: present
```

License
-------

MIT

Author Information
------------------

[Laba Subagia](https://github.com/labasubagia)
