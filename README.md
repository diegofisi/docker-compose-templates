# docker-compose-templates

This repository is a basic docker compose templates.

---

## How to use

copy docker-compose.yml and .env.template to your project and rename .env.template to .env
you can replace the name volume, image tag and container name in docker-compose.yml

for example:

```
version: '3.9'
services:
  pgAdmin:
    ...
    volumes:
      - pg-admin:/var/lib/pgadmin
    ...

volumes:
  pg-admin:
    name: pg-admin
    external: false
```

you can do it this:

```
version: '3.9'
services:
  pgAdmin:
    ...
    volumes:
      - ./pg-admin:/var/lib/pgadmin
    ...
```

this is a binding volume, the data will be saved in the folder pg-admin in the project.

---