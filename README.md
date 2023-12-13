# k3s-remove
Ansible playbook to remove k3s kubernetes

Please also check out the companion Playbook to [deploy k3s kubernetes](https://github.com/luisj1983/k3s-deploy).

## Description
This Playbook will remove [k3s](https://k3s.io/) using the built-in k3s scripts and then it ensure that the application and its pre-requisites have been removed.
Please pay attention to what will be removed and customize it for your needs; the goal of this playbook is to provide a quick way to tear down a k3s `lab/testing` environment, providing a clean-slate to re-deploy onto. <br>
<br>
**If you want to use this in Production then please customise the app removal step.**

This Playbook has been tested on Ubuntu 20.xx and ought to also work on Debian equivalents.<br>
It is not expected to work with non-Debian distributions as it currently depends on the [ansible.builtin.apt](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/apt_module.html) module.

## Usage

```bash
ansible-playbook -K main.yml
```



# To-do
- [ ] Make app removal step OS agnostic.
