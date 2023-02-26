# Ansible Bug

Reproduces an ansible bug

Even though `become: false` is set for the task running on localhost, the more generic `become: true` from `group_vars/all.yml` takes precedence.

To reproduce:
1. Run `ansible-playbook bug.yml`
2. Playbook fails, expecting a password
