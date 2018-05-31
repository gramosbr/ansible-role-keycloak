Ansible role for Keycloak

### Features

- Installs Keycloak
- Installs a systemd service
- Creates an admin user


### Instructions

Include the role and define any variables as described below


### Variables

- `keycloak_admin_password` (required)
    - Password for the admin user
- `keycloak_admin_username` (optional)
    - Username for the admin user
    - Default value: 'admin'
- `keycloak_group` (optional)
    - Default value: keycloak
- `keycloak_home` (optional)
    - Default value: /opt/keycloak
- `keycloak_java_version` (optional)
    - Default value: 8
- `keycloak_user` (optional)
    - Default value: keycloak
- `keycloak_version` (optional)
    - Version of Keycloak to install
    - Default value: see [defaults/main.yml](defaults/main.yml)


### Sample playbook

    - hosts: keycloak-servers
      roles:
        - keycloak
      vars:
        keycloak_admin_password: "{{ vault_keycloak_admin_password }}"
