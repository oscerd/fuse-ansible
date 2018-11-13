Role for Fuse 7

An example of Fuse 7 role use:

```yaml
---
- name: role fuse7
  hosts: localhost
  remote_user: user
  
  roles:
    - role: fuse7
      fuse_version: 7.2.0.fuse-720023
      dest_dir: /home/user/
      md5sum: md5:877d191b86d26e13136a1e8f142f4164
      unzip_dest_dir: /home/user/fuse/
      additional_maven_repositories:
        - "http://maven.repo.com/test/test@id=test"
      karaf_clean_all: false
      karaf_clean_cache: false
``` 
