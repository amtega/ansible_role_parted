# Ansible <!-- this role name --> role

This is an [Ansible](http://www.ansible.com) role which manage disk partitions through the parted module.

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

## Usage

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - amtega.parted
  vars:
    parted_disks_sample:
      - device: /dev/sdb
        number: 1
        part_type: primary
        state: present

    parted_disks_load_from_hostvars: yes
```

## Testing

Tests are based on [molecule with vagrant virtual machines](https://molecule.readthedocs.io/en/latest/installation.html).

```shell
cd amtega.parted

molecule test --all
```

## License

Copyright (C) 2022 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- José Enrique Mourón Regueira.
