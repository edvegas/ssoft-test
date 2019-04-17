## Pre-requisites:

On your local linux machine:

* Installed [Ansible 2.7](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) and higher

* Installed [Vagrant](https://www.vagrantup.com/downloads.html)

## Usage:

```git clone https://github.com/edvegas/ssoft-test.git```

```cd ssoft-test && vagrant up```

## After VM installation and provisioning

Application is available on you localhost on port 8080:
```http://localhost:8080```

To GET list of users, type:

```http://localhost:8080/api/user```

To POST new user via API, you can use CURL for example:

```curl -d '{"username":"user", "email":"user@host.domain", "password_hash":"123456"}' -H "Content-Type: application/json" -X POST http://localhost:8080/api/user```
