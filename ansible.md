# Ansible Interview Questions & Answers

#### 1. What are ansible roles and what are its advantages? 
**Answer.** Using ansible roles enhances the readability, scalability, and maintainability of Ansible playbooks, making automation projects more efficient.

#### 2. When i need detailed logs on executing ansible playbook what option i need to use?
**Answer.** To obtain detailed logs when executing an Ansible playbook, you can use the -vvv (or --verbose) option. This increases the verbosity level and provides more detailed output, helping you troubleshoot and understand the execution process:
```
ansible-playbook -vvv your-playbook.yml
```

#### 3. Why, like, what's the benefit of using Ansible?
**Answer.** Ansible simplifies IT automation, making it easier to deploy, manage, and scale infrastructure and applications. It offers efficiency, consistency, and flexibility in configuration management, application deployment, orchestration, and task automation.

#### 4. What's one thing that makes Ansible different from any other tool for example, Chef, Puppet or anything like that?
**Answer.** Ansible stands out for its agentless architecture, simplicity, and ease of use. Unlike other configuration management tools like Chef or Puppet, Ansible does not require agents to be installed on managed hosts, leading to reduced overhead and faster deployment.

#### 5. Is Ansible agent or agentless?
**Answer.** Ansible is agentless, meaning it does not require any software to be installed on the managed hosts. Instead, it communicates with remote hosts using SSH (Secure Shell) protocol for Linux-based systems and WinRM (Windows Remote Management) protocol for Windows systems.

#### 6. What does it use to communicate with the host?
**Answer.** Ansible communicates with the hosts using SSH protocol for Linux-based systems and WinRM protocol for Windows systems. It securely connects to remote hosts over the network to execute tasks defined in playbooks.

#### 7. How does Ansible interact with the servers?
**Answer.** Ansible interacts with servers through playbooks, which are YAML-formatted files containing instructions to configure, deploy, and manage systems. Playbooks define tasks, roles, and variables that specify desired configurations and actions to be performed on the servers.

#### 8. What have you automated so far in terms of that, like what have you configured on the host using Ansible playbook?
**Answer.** Using Ansible playbook, various tasks can be automated such as server provisioning, package installation, configuration management, application deployment, service orchestration, and system monitoring. Specific examples may include setting up web servers, configuring databases, deploying applications, and managing network devices.

#### 9. if u have 100 servers we need to check their versions and if the updated version not available in that particular server we need to send mail to particular person - how can we achieve this?
**Answer.** 
```
---
- name: Check software versions
  hosts: servers
  tasks:
    - name: Get current version
      shell: command_to_get_version
      register: current_version

    - name: Compare with latest version
      set_fact:
        outdated: "{{ current_version.stdout.strip() != latest_version }}"

    - name: Send email if outdated
      when: outdated
      mail:
        to: admin@example.com
        subject: "Outdated version detected on {{ inventory_hostname }}"
        body: "The current version is {{ current_version.stdout.strip() }}, which is outdated."
```
By using this yaml we can achieve..
