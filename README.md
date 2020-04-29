## Lesson 12: Ansible роли, управление настройками нескольких окружений и best practices

- Роли добавлены

## Lesson 10

- Вопрос со слайда 13.2 - Изменился статус changed на 1 .
  это значит что изменения применились, так как предыдущей коммандо "rm -rf ~/reddit"
  мы удалили папку репозитория , поэтому вызов clone.yml плейбука склонировал репозиторий

## Lesson 9

- Created Terraform modules
- Created different stages
- Created bucket

## Lesson 8

- Teerraform configuration added
- Added variables.tf and \*.tfvars.example

## Lesson 6

testapp_IP = 104.155.22.50
testapp_port = 9292

## Lesson5

### Connection credentials

```
bastion_IP = 35.206.179.20
someinternalhost_IP = 10.132.0.3
```

### Homework 5

#### Question

#### Answer:

##### 1. using ssh command

Update `~/.ssh/config` with

```
Host bastion
Hostname bastion-vm-external-ip-adrress
User username-here

Host someinternalhost
ProxyCommand ssh -q bastion nc -q0 internal-someinternalhost-host 22
```

then run: `ssh user@someinternalhost`

##### 2. using gcloud cli:

Connecting to instances as the root user

```
gcloud compute ssh --project project-id-here --zone zone-here root@someinternalhost
```

### Homework \*
