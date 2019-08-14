# nftables-deploy

This role installs `nftables` and copies a folder containing nftables configuration files to `/etc/nftables`.
When reloading the service, the syntax of the nftables config is checked first.
A wrapper for manually doing that is placed at `/usr/local/sbin/nftables-reload`.


## Requirements

This is tested on Debian but should also work on its derivates.
`files/nftables` should exist and contain at least a `nftables.conf` file.


## Role Variables

| Name                    | Required/Default | Description                                                   |
|-------------------------|:----------------:|---------------------------------------------------------------|
| `nftables_deploy_group` | `root`           | Group that should own the nftables files touched by this role |


## Example

```yml
nftables_deploy_group: adm
```

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).


## Author Information

- [Janne Heß](https://github.com/dasJ)
