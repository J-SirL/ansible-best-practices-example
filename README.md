# ansible best practices example
Are you just getting started with ansible? 
then this might be some use to you, I created this using the doc from ansible 1.9.2

Run playbook check: 
Staging: ansible-playbook -u [username] -i staging site.yml --check

Production: ansible-playbook -u [username]  -i production site.yml --check

Ansible project structure explained:
```
|-- README.md
|-- site.yml
|-- production                  # inventory file for production servers
`-- staging                     # inventory file for staging environment
|-- group_vars/                 # here we assign variables to particular groups 
|   `-- group-example               
|-- host_vars/              # if systems need specific variables, put them here
|   `-- hostname-example
|-- filter_plugins/            # if any custom filter plugins, put them here (optional)
|-- library/                   # if any custom modules, put them here (optional)
|-- roles/
|   `-- role-example/
|       |-- defaults
|       |   `-- main.yml
|       |-- handlers
|       |   `-- main.yml
|       |-- meta
|       |   `-- main.yml
|       |-- README.md
|       |-- tasks
|       |   `-- main.yml
|       `-- vars
|           `-- main.yml
```


