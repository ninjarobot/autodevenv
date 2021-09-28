# autodevenv
Automation to install tools for a development environment.

This automation currently uses anisible to deploy the SDK's and tooling for a fresh development environment on any machines listed in the `hosts` file.

Create a virtualenv for ansible in the venvs/ansible directory, activate it, and install ansible:
```bash
python3 -m venv venvs/ansible
source venvs/ansible/bin/activate
pip install ansible
```

```bash
ansible-playbook dev_machine.yml -i hosts --ask-pass -K
```
Or if you want to install the .NET 6 RC1:
```bash
ansible-playbook dev_machine.yml -i hosts --ask-pass -K -e dotnet=preview
```
