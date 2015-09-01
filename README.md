## infinitewp

[![Build Status](https://travis-ci.org/Oefenweb/ansible-infinitewp.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-infinitewp) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-infinitewp-blue.svg)](https://galaxy.ansible.com/list#/roles/4574)

Set up [infinitewp](https://code.google.com/p/phpmemcacheadmin/) (Memcached server admin in php for monitoring and debugging).

#### Requirements

None

#### Variables

* `infinitewp_version`: [default: `1.2.2-r262`]: Version to install

* `infinitewp_install_dir`: [default: `{}`]: Install directory declaration
* `infinitewp_install_dir.dest`: [required]: The remote path of the installation (e.g. `/var/www`)
* `infinitewp_install_dir.owner`: [required]: The name of the user that should own the directories and file(s) that need to be writable
* `infinitewp_install_dir.group`: [optional, default `owner`]: The name of the group that should own the directories and file(s) that need to be writable
* `infinitewp_install_dir.state`: [optional, default: `present`]: State

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - infinitewp
  vars:
    infinitewp_install_dir:
      dest: /var/www
      owner: www-data
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-infinitewp/issues)!
