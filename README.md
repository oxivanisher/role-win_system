win_system
==========

Configure Windows system things, mostly concerning privacy and telemetry:
* Disable automatic install of suggested apps
* Disable user activity upload to Microsoft
* Disable Microsoft self ads ("Suggest ways to get the most out of Windows and finish setting up this device")
* Disable "Windows Welcome Experience"

Requirements
------------

This role is built to be used with Ansible oder SSH on Windows.

Role Variables
--------------

| Name                             | Comment                        | Default value |
|----------------------------------|--------------------------------|---------------|
| win_system_users                 | List of users to be configured | `[Default]`   |
| win_system_also_for_ansible_user | Also configure `ansible_user`  | `true`        |

Example Playbook
----------------
```yaml
- name: Configure the Windows Start menu
  hosts: windows
  roles:
    - role: oxivanisher.windows_desktop.win_system
```
License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.windows_desktop](https://galaxy.ansible.com/ui/repo/published/oxivanisher/windows_desktop/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-windows_desktop).
