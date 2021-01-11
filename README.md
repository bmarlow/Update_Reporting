Update_Reporting
=========

The purpose of this role is to provide a framework for both updating systems and providing an audit (report) on the update.  Namely to show what versions the packages originally were and what they are after the update.

Requirements
------------

You need a package manager.  This has been tested with DNF and YUM, however it should work with most other package managers automatically.

Role Variables
--------------

There aren't any variable that need to be set for the role to run.  However for sending the report data to other sources (Database, webservice, CMDB, etc) you will want to use the 'update_report' variable, which is the formatted report stored in a variable.

Dependencies
------------

You will need to have a user that has sudo or update access.  Your system will also require a package manager (as defined in the facts by 'ansible_pkg_mgr').

Example Playbook
----------------


```
---
- name: Run the Update and Report Role
  hosts: all
  tasks:
  - name: "Run the update and report Role"
    include_role: 
      name: Update_Reporting
```

License
-------

BSD

Author Information
------------------

Created by Brandon Marlow.  Brandon enjoys building things and not having to worry about updates.
