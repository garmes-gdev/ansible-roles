# Ansible roles 
-  lvm 
-  java 
-  kafka 
-  zookeeper 

Copyright (c) 2017-2018, Mohammed Amine GARMES.

## Usage

### Requeriments
-  Ansible 2.4 or higher.

### Steps

#### 1. Ctreate the hosts file.

#### 2. Run Ansible playbook. Check _Tags section_ to see other playbook run options.

```
ansible-playbook kafka.yml -i hosts/hosts_file [options]
```


## Playbook tags

Use tags to run a part of the playbook:

```
ansible-playbook kafka.yml -i hosts --tags kafka 
ansible-playbook kafka.yml -i hosts --tags "zookeeper,kafka" 
ansible-playbook kafka.yml -i hosts --tags "lvm,java,zookeeper,kafka" 
```

* **lvm :** create un mount lvm.
* **java / java_installation:** Install and configure jdk.
* **zk_prepare:** Setup user/group _zookeeper_ into zookeeper nodes.
* **zk_install:** Get _zookeeper_ package if needed and install it.
* **zk_config:** Set _zookeeper_ configuration needed and start zookeeper service.
* **zookeeper:** zk_prepare + zk_install + zk_config.
* **kafka_prepare:** Setup user/group _kafka_ into kafka nodes.
* **kafka_install:** Get _kafka_ package if needed and install it.
* **kafka_config:** Set _kafka_ configuration needed and start kafka service.
* **kafka:** kafka_prepare + kafka_install + kafka_config.

## Group variables

#### LVM variables
#### JAVA variables
#### ZOOKEEPER variables
#### KAFKA variables


### Authors and license

`lvm` `java` `kafka` `zookeeper` roles were written by:
- Mohammed Amine GARMES | [e-mail](mailto:aminegarmes@yahoo.fr) | [GitHub](https://github.com/garmes-gdev)

License: [GPLv3](https://tldrlegal.com/license/gnu-general-public-license-v3-%28gpl-3%29)

## Support

File bug reports, feature requests and questions using
[GitHub Issues]


***
_coming soon_


