# Ansible Playbook: cloudflare_add_record
![GitHub last commit](https://img.shields.io/github/last-commit/lpwoodhouse/playbook_cloudflare_add_record)
![GitHub repo file count](https://img.shields.io/github/directory-file-count/lpwoodhouse/playbook_cloudflare_add_record)
![GitHub top language](https://img.shields.io/github/languages/top/lpwoodhouse/playbook_cloudflare_add_record)

## Purpose

This play is for adding a DNS A record using the cloudflare api and then updating it with a cloudflare dynamic DNS update script.

## Requirements

community.general

## Role Variables

Available variables are listed below, along with default values (see ```defaults/main.yml```)
```shell
# add_record role
auth_email: user@example.com
auth_key: <auth_key>
sub_domain: <sub_domain>
root_domain: example.com
# ddns_update role
auth_email: user@example.com
auth_key: <auth_key>
zone_id: <zone_id>
script_path: ~/cloudflare-ddns-updater/
sub_domain: <sub_domain>
root_domain: example.com

```
## Dependencies

None

## Example Playbook
```yaml
    - hosts: all
      vars:
        add_record: true
      roles:
        - add_record
        - ddns_update
```

## License

[![GitHub](https://img.shields.io/github/license/lpwoodhouse/playbook_cloudflare_add_record)](LICENSE)

## Author Information

This role was created in 2022 by [Lee Woodhouse](https://www.leewoodhouse.com/)
