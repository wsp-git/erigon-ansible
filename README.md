# Ansible roles for Erigon deployment

This is a group of roles for provisioning ethereum node in testnet Ropsten

## Installation

Clone the repo
```python
git clone https://github.com/wsp-git/erigon-ansible.git
cd erigon-ansible/
```
Prepare your private key
and to provision the node run:

```bash
ansible-playbook -i <server_ip>, playbook.yml --user <name> --private-key <path_to_keyfile>
```

## Nomad Job
After all ansible tasks finished you can
check for successfull nomad job deployment at: 
```python
http://<server_ip>:4646/ui/jobs
```
All ledger data will be safely stored at mountpoint
```bash
/ethdata
```
