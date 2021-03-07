[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/H2H43P9OI)

# Ansible role: linuxgsm

Download LinuxGSM to a common location on Linux systems and optionally install
all the dependency packages required to use it.

More information about LinuxGSM can be found at [GameServerManagers/LinuxGSM](https://github.com/GameServerManagers/LinuxGSM).

## Example Playbook

To get started using the role:

    - hosts: servers
      roles:
         - stonesoupkitchen.linuxgsm

Some users may use alternative Ansible roles to manage some of the same
dependent packages that this role does. To disable the installation of
these packages:

    - hosts: servers
      roles:
         - stonesoupkitchen.linuxgsm
      vars:
        linuxgsm_install_dependencies: no

To change the install path of the LinuxGSM executable:

    - hosts: servers
      roles:
         - stonesoupkitchen.linuxgsm
      vars:
        linuxgsm_install_dir: '/path/to/install/dir'

## Role Variables

### Defaults

| Variable                        | Description                                     | Default         |
|---------------------------------|-------------------------------------------------|-----------------|
| `linuxgsm_install_dir`          | Default installation directory for LinuxGSM.    | `/opt/linuxgsm` |
| `linxugsm_install_dependencies` | Install prerequisites for LinuxGSM.             | yes             |

### Vars

| Variable                | Description                           | Value                                    |
|-------------------------|---------------------------------------|------------------------------------------|
| `linuxgsm_install_path` | Full path to the LinuxGSM executable. | `{{ linuxgsm_install_dir }}/linuxgsm.sh` |

## License

See [LICENSE](LICENSE).

