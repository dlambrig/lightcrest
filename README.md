
After downloading to your-dir, set the variables.
  
your-dir/roles/lightcrest/vars/main.yml:

```
---
# vars file for lightcrest-role

# if your-dir is /root :
var_playbook_dir: "/root/roles/lightcrest"

# vars for consul configuration
var_consul_retry_join: '"10.0.40.215", "10.0.40.161" '
var_consul_advertise_addr: '"10.0.40.215"'
var_private_json_key: "http://10.0.40.215:8999"
var_consul_datacenter: '"lax0_vizex"'
```
In your-dir, create a file:
  
``` 
cat > setup.yml << EOF
---
- hosts: lightcrest
  roles:
    - lightcrest
EOF
```
Then run it:
```
ansible-playbook setup.yml 
```
