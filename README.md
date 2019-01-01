# FLKA Mail Setup

The whole setup is currently on two different VMs, each running `docker` and `docker-compose`

## mail.fablab-karlsruhe.de

Mailu based

```shell
cd mail
docker-compose up -d

# create superuser root@example.net
docker-compose run --rm admin python manage.py admin root example.net password
```

## lists.fablab-karlsruhe.de

Mailman 3 based

```shell
cd lists
docker-compose up -d

# create superuser
docker-compose exec mailman-web python manage.py createsuperuser
# manage more super users under /admin
```

### TODO

* configure the LE certs for postfix
