# ansible best practices example
Are you just getting started with ansible? 
then this might be some use to you, I created this using the doc from ansible 1.9.2

Run playbook check: 
Staging: ansible-playbook -u [username] -i staging site.yml --check

Production: ansible-playbook -u [username]  -i production site.yml --check

Ansible project structure explained:
```
|-- README.md                   # This file
|-- site.yml                    # master playbook
|-- production                  # inventory file for production servers
`-- staging                     # inventory file for staging environment
|-- group_vars/                 # here we assign variables to particular groups 
|   `-- group-example               
|-- host_vars/              # if systems need specific variables, put them here
|   `-- hostname-example
|-- filter_plugins/            # if any custom filter plugins, put them here (optional)
|-- library/                   # if any custom modules, put them here (optional)
|-- roles/                     # Here you put the roles you like to use
|   `-- role-example/         # role created with ansible-galaxy init [your empthy role]
|       |-- defaults
|       |   `-- main.yml    # defaults file for role
|       |-- handlers
|       |   `-- main.yml    # handlers file for the role
|       |-- meta
|       |   `-- main.yml    # Here you write information about your role
|       |-- README.md       #  This is the READ.me for the role        
|       |-- tasks
|       |   `-- main.yml    # tasks file for the role
|       `-- vars
|           `-- main.yml    # vars file for role
```


