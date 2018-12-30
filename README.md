# FLKA Mail Setup

The whole setup is currently on two different VMs, each running `docker` and `docker-compose`

## mail.fablab-karlsruhe.de

Mailu based

```shell
cd mail
docker-compose up
```

## lists.fablab-karlsruhe.de

Mailman 3 based

```shell
cd lists
docker-compose up
docker-compose exec mailman-web python manage.py createsuperuser
```
