# Ansible Role: Mattermost

Installs and configures Mattermost service

## Requirements

The role assumes that there is an existing postgres database on the server

## Role Variables

All role variables are listed in default/main.yml.

## Dependencies

None.

## Example Playbook

    - hosts: mattermost
      become: yes
      vars_files:
        - vars/main.yml
      roles:
        - { role: ansible-role-mattermost }

*Inside `vars/main.yml`*:

    mattermost_user: mattermost
    mattermost_db_user: mmuser
    mattermost_db_password: hope-you-have-changed-this
    mattermost_enable_tls: true
    mattermost_certificate_file: /Certificate.txt
    mattermost_private_key_file: /private_key.txt


## License

MIT / BSD
