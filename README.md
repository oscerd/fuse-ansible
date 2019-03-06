Role for Fuse 7

An example of Fuse 7 role use:

```yaml
---
- name: role fuse7
  hosts: localhost
  remote_user: user
  
  roles:
    - role: fuse7
      fuse_version: fuse-karaf-7.2.0.fuse-720023
      path_dir: /home/user/
      unzip_dest_dir: /home/user/fuse/
      additional_maven_repositories:
        - "http://maven.repo.com/test/test@id=test"
      karaf_clean_all: false
      karaf_clean_cache: false
      enable_admin: false
      start_fuse: false
``` 
