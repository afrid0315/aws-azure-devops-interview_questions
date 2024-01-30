# Ansible Interview Questions & Answers

#### 1. What are ansible roles and what are its advantages? 
**Answer.** Using ansible roles enhances the readability, scalability, and maintainability of Ansible playbooks, making automation projects more efficient.

#### 2. When i need detailed logs on executing ansible playbook what option i need to use?
**Answer.** To obtain detailed logs when executing an Ansible playbook, you can use the -vvv (or --verbose) option. This increases the verbosity level and provides more detailed output, helping you troubleshoot and understand the execution process:
```
ansible-playbook -vvv your-playbook.yml
```
