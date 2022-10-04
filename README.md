# Ansible Play: cloudflare_add_record

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

MIT

## Author Information

This role was created in 2022 by [Lee Woodhouse](https://www.leewoodhouse.com/)
