# Ansible templating issue minimal reproduction

This is the minimal reproduction of a regression that happened between ansible 2.1.2 and 2.2.

# Steps to reproduce

1. Install ansible 2.1.2
2. `ansible-playbook playbook.yml`
3. It works
4. Install ansible 2.2
5. `ansible-playbook playbook.yml`
6. We get the error below:

```
TASK [debug] *******************************************************************
An exception occurred during task execution. To see the full traceback, use -vvv. The error was: TemplateNotFound: bar.txt
fatal: [localhost]: FAILED! => {"failed": true, "msg": "Unexpected failure during module execution.", "stdout": ""}
```
