Role for Fuse 7

An example of Fuse 7 role use:

```yaml
---
- name: role fuse7
  hosts: localhost
  remote_user: user
  
  roles:
    - role: fuse7
      fuse_version: fuse-karaf-7.3.0
      path_dir: /home/user/
      unzip_dest_dir: /home/user/fuse/
      additional_maven_repositories:
        - "http://maven.repo.com/test/test@id=test"
      karaf_clean_all: false
      karaf_clean_cache: false
      enable_admin: true
      additional_users:
        - "admin_test = admin_test,_g_:admingroup"
      start_fuse: true
``` 

## Role options

| Name                                 | Description                                                                                                               |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| fuse_version                         | The name of the fuse zip distribution                                                                                     |
| path_dir                             | The location of the fuse zip distribution                                                                                 |
| unzip_dest_dir                       | The location of the dire where to unzip the fuse zip distribution                                                         |
| additional_maven_repositories        | List of additional maven repositories to use                                                                              |
| karaf_clean_all                      | Setting of the karaf.clean.all option                                                                                     |
| karaf_clean_cache                    | Setting of the karaf.clean.cache option                                                                                   |
| enable_admin                         | If the admin role must be enabled or not                                                                                  |
| additional_users                     | A list of additional users in the form `admin_test = admin_test,_g_:admingroup`                                           |
| start_fuse                           | Start Fuse at the end of the ansible playbook                                                                             |
| log_level                            | Log level of the root logger                                                                                              |
