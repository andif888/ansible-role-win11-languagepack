ansible-role-win11-languagepack
=========

Add language packs to a Windows 11.   


Role Variables
--------------
The default values for the variables are set in `defaults/main.yml`:

```yaml
language_experience_pack_download_dir: 'C:\temp'
language_experience_pack_isos:
  - url: 'https://software-download.microsoft.com/download/sg/22000.1.210604-1628.co_release_amd64fre_CLIENT_LOF_PACKAGES_OEM.iso'
    dest: '{{ language_experience_pack_download_dir }}\langpack.iso'

language_experience_packs:
  - de-de

language_experience_pack_isos_remove_when_finished: true
```

Example Playbook
----------------


```yaml
- hosts: win11
  vars:
    language_experience_pack_download_dir: 'D:\temp'
    language_experience_packs:
      - de-de
      - nl-nl

  roles:
    - { role: ansible-role-win11-languagepack }
```
