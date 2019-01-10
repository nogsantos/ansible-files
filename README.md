# Ansible files

Roles files is for ubuntu

## Premisses

- [Docker](https://docs.docker.com/install/)
- [docker-compose](https://docs.docker.com/compose/install/)

## Run

Container up

```bash
$ docker-compose up -d
Creating network "ansible-files_default" with the default driver
Creating ansible ... done
```

View container

```bash
$ docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
c11ba76634d3        nogsantos/ansible   "/bin/bash"         24 seconds ago      Up 23 seconds       80/tcp              ansible
```

Attach to the container

```bash
$ docker attach ansible
```

In container Ansible work dir is `/etc/ansible`

## Generate the keys

### Generate ssh keys

```bash
$ ssh-keygen -t rsa -b 4096 -f [key-name] -C [user]
```

### Connect to host

```bash
$ ssh -i [key-name] [user]@[host-address]
```
