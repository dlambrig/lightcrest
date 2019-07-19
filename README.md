
Invoke the role by creating a yml file:
```
---
- hosts: lightcrest
  roles:
    - lightcrest
```
Then run it:
```
ansible-playbook setup.yml 
```
