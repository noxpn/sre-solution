
Solution for: https://github.com/muxx/sre-hello-world

OS: CentOS7

ansible: [core 2.12.5]

### run:
ansible-playbook --ask-vault-pass -i hosts sre-full-task.yml

**vault pass**: 12345678

#### nuances
bug on ansible 2.10 : yum ansible ~~loop~~ interpreter puke (need to move 2->3->2)

The ipaddr filter requires python's netaddr be installed on the ansible controller

("sudo apt install --no-install-recommends python3-netaddr" or "pip3 install netaddr" )