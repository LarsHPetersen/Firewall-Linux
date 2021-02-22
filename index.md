# Firewall-Linux

This is a ansible playbook for allowing or blocking ports on a RHEL host.

> If no tags in defined then the playbook defaults to allow

```bash
ansible-playbook Firewall.yml -i hosts -u user -k -e "addport=80/tcp"

ansible-playbook Firewall.yml -i hosts -u user -k -e "addport=80/tcp" --tags add

ansible-playbook Firewall.yml -i hosts -u user -k -e "denyport=3389/tcp" --tags deny
```
> You can also create multiple firewall rules at the same time, by separating then with a comma.

```bash
ansible-playbook Firewall.yml -i hosts -u user -k -e "addport=80/tcp,443/tcp"

ansible-playbook Firewall.yml -i hosts -u user -k -e "addport=80/tcp,443/tcp" --tags add

ansible-playbook Firewall.yml -i hosts -u user -k -e "denyport=3389/tcp,23/tcp" --tags deny
```
