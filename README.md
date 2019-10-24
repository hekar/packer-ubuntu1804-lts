# Ubuntu 18.04 LTS Packer libvirt KVM image

Minimal build of [Ubuntu 18.04.3][ubuntu] using [ansible]. Based on [geerlingguy/packer-ubuntu-1804/](https://github.com/geerlingguy/packer-ubuntu-1804/).

Includes: `git`, `wget`, `curl`, `vim` and `aptitude`.

This configuration is fully functional, but meant to be extended. Hence the inclusion of ansible where it is not required.

See [./ansible/main.yml](./ansible/main.yml) for the entry to the [ansible playbook][ansible-playbook].

## Requirements

The following software must be installed on your local machine before building the qemu2 file:

  - [Packer](http://www.packer.io/)
  - [Ansible](http://docs.ansible.com/intro_installation.html)

## Usage

Make sure all the required software (listed above) is installed, then cd to the directory containing this README.md file, and run:

```
packer build ubuntu1804.json
```

After a few minutes, Packer should tell you the box was generated successfully.

Output is stored in `./builds` by default.


## License

MIT license.

ansible: https://github.com/ansible/ansible
ansible-playbook: https://docs.ansible.com/ansible/latest/user_guide/playbooks_intro.html
ubuntu: https://wiki.ubuntu.com/BionicBeaver/ReleaseNotes
