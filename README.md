PostgreSQL
========

Installs PostgreSQL and setup db user and databases (if provided).

Installation
--------------

`ansible-galaxy install palkan.postgresql`

Role Variables
--------------

`defaults/main.yml`

| Name                        | Default Value |  Description    |
|-----------------------------|-----|---------------------------|
| postgresql_version          | 9.5 | |
| postgresql_hba              | pg_hba.conf.j2 | |
| postgresql_config           | postgresql.conf.j2 | |
| postgresql_ram_shared       | 512 | To use with default config |
| postgresql_ram_cache        | 256 | To use with default config |
| postgresql_db_user          | - | DB user name (_optional_) |
| postgresql_db_user_flag   | CREATEDB,NOSUPERUSER | DB user privileges (_optional_) |
| postgresql_db_user_pass          | - | DB user pass (plain) (_optional_) |
| postgresql_databases          | - | List of databases to create (_optional_) |

Example Playbook
-------------------------
```yml
  - hosts: servers
    roles:
       - palkan.postgresql
```
