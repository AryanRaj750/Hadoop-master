Hadoop-Master
=========

Configure rhel8 system as NameNode/master

Requirements
------------

>- **[Hadoop software](https://archive.apache.org/dist/hadoop/core/hadoop-1.2.1/hadoop-1.2.1-1.x86_64.rpm "click to download hadoop")**

>- **[jdk 1.8](https://download.oracle.com/otn/java/jdk/8u171-b11/512cd62ec5174c3487ac17c61aaa89e8/jdk-8u171-linux-x64.rpm "click to download jdk 1.8")**

>- You may need to download **gcc library/compiler** for java because hadoop is designed on java language. y
>- After download both file **jdk-8u171-linux-x64.rpm** and **hadoop-1.2.1-1.x86_64.rpm** *copy in files* directory of the role.

---

Role Variables
--------------
- **port_no :**
By defualt porn_no is 9000. If have to change then can change
but master port number and slave port number shoud be same otherwise slave could not connect. Be careful...
- **master_path :** By default master_path is '**/mn'**. If want to give a specific directory then you have to update this variable value.
- **pkg_path :** This variable i used for path of package where *jdk-8u171-linux-x64.rpm* and *hadoop-1.2.1-1.x86_64.rpm* files are present or want to copy. So, further task (e.g installation) could be proceed.

Dependencies
------------



Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: master
      roles:
         - hadoop-master

Inventory File
------------------
    [master]
    IPaddress ansible_user=root ansible_ssh_pass=xyz123 ansible_connection=ssh

Author Information
------------------

Name:- **Aryan Raj**

Email:- **Ar9131000@gmail.com**
