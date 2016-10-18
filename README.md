Role Name
=========

Import mysql databases from sql files

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

Use the same variables as geerlingguy.mysql plus a variable for the sql file path.

```yaml
# Boonyah.mysql-import
mysql_sql_path: /tmp
mysql_databases:
  - name: database_name
    sqlfile: "{{ mysql_sql_path }}/database_name.sql"
  - name: database_name2
    sqlfile: "{{ mysql_sql_path }}/database_name2.sql"
mysql_users:
  - name: database_user 
    password: database_password
```

Dependencies
------------

I use the same variable names as geerlingguy.mysql

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
