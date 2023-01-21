# basestar provisions

everything i need to get my basestar fully operational

![battlestar galactica exchanging munitions with a couple of cylon basestars](https://media.tenor.com/0Uuw4iOYNoQAAAAC/battlestar-galactica-galactica.gif)

## requirements

- [ansible](https://www.ansible.com/) - for configuring everything *just so*
- [ansible docker community collection](https://galaxy.ansible.com/community/docker) and...
- [docker SDK for python](https://docker-py.readthedocs.io/en/stable/) - for deploying apps
- [vagrant](https://www.vagrantup.com/) - for testing against a local box

## usage

create your inventory file

```bash
$ echo 'example.com ansible_user=username' > inventory
```

run the playbook

```bash
$ ansible-playbook playbook.yaml -i inventory --ask-become-pass
```
 
## local usage

set required env vars

```bash
$ cp .env.example .env
$ vim .env
```

bootstrap database

> **note**: this script doesn't exist yet. sorry! check casper's source.

```base
$ ../casper7/scripts/makedb casper.db
```

spin up & provision the vagrant box

```bash
$ vagrant up
```
