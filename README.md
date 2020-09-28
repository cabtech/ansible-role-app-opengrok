----
# ansible-role-app-opengrok

## Purpose Installs and configures [Opengrok](https://oracle.github.io/opengrok/) 

## Requied variables
| Name | Type | Comment |
| ---- | ---- | ------- |
| opengrok_github_token | string | needed if specifying private repos ||

## Default variables
| Name | Type | Value | Comment |
| ---- | ---- | ----- | ------- |
| opengrok_addr | string | localhost ||
| opengrok_download_url | string | 'https://github.com/oracle/opengrok/releases/download' ||
| opengrok_group | string | tomcat8 | Unix group |
| opengrok_internet_timeout | integer | 30 ||
| opengrok_owner | string | tomcat8 | Unix user |
| opengrok_opt_dir | string | /opt/opengrok | where the binaries live |
| opengrok_pkg_dependencies | list(string) | git, libjansson4, tomcat8 ||
| opengrok_port | integer | 8080 | what Tomcat listens on |
| opengrok_private_repos | list(string) | [] | e.g. `ansible/ansible` |
| opengrok_public_repos | list(string) | [] | e.g. `yourTeam/specialCode` |
| opengrok_snap_dependencies | list(string) | universal-ctags | there is no pkg for this |
| opengrok_staging_dir | string | /var/downloads | Unix path for the download of Opengrok |
| opengrok_sub_dirs | list(dict(keys(group, mode, owner, path))) | see `defaults/main.yml` ||
| opengrok_svc_enabled | Boolean | true ||
| opengrok_svc_name | string | tomcat8 ||
| opengrok_svc_state | string | started ||
| opengrok_var_dir | string | /var/opengrok | Unix path |
| opengrok_version | string | 1.4.5 ||

## Supported Distros
Ubuntu 16+

****
