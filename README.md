# autodevenv
Automation to install tools for a development environment.

This automation currently uses anisible to deploy the SDK's and tooling for a fresh development environment on any machines listed in the `hosts` file.

```bash
ansible-playbook dev_machine.yml -i hosts --ask-pass -K
```
