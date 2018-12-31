# FLKA Mail Setup

The whole setup is currently on two different VMs, each running `docker` and `docker-compose`

## mail.fablab-karlsruhe.de

Mailu based

```shell
cd mail
docker-compose up -d
```

## lists.fablab-karlsruhe.de

Mailman 3 based

```shell
cd lists
docker-compose up -d
docker-compose exec mailman-web python manage.py createsuperuser
```

### TODO

* configure the LE certs for postfix
