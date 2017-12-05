# ansible-role-zfs

Installs and enables the ZFSForLinux kernel module driver for RHEL/Ubuntu

## Requirements

None

## Role Variables

| Variable Name             | Defaults | Description                                                        |
|---------------------------|----------|--------------------------------------------------------------------|
| zfs_source_el_enabled     | 0        | state of the zfs-source repository on Enterprise Linux             |
| zfs_dkms_el_enabled       | 0        | state of the auto-building zfs-dkms repository on Enterprise Linux |
| zfs_kmod_el_enabled       | 1        | state of the pre-built zfs-kmod repository on Enterprise Linux     |

## Dependencies

None

## Example Playbook

```
    - hosts: servers
      roles:
        - role: gabethecabbage.zfs-kmod
```

For dkms built zfs kernel modules on Enterprise Linux

```
    - hosts: servers
      roles:
        - role: gabethecabbage.zfs-kmod
          zfs-kmod-el-enabled: 0
          zfs-dkms-el-enabled: 1
```
