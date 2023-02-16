# .env file

rename .env.template to .env or copy the contents to a .env file

---

# default values for this image

the default port for this image is 80
go to http://localhost:8080/login for login
or to http://localhost:{PG_ADMIN_PORT}/login for login

for login you just need PGADMIN_DEFAULT_PASSWORD and PGADMIN_DEFAULT_EMAIL
for connection you need:

- host: DB_NAME (is the name of the container of the postgres image) in this case not is localhost
- maintenance database: postgres
- port: in this case is image default port "5432"
- username: in this case is "postgres"
- password: in this case is "your-db-password"

example:

- host: your-db-name
- port: 5432
- maintenance database: postgres
- username: postgres
- password: your-db-password

---

# .env.template values

change the values of .env.template as you see fit

---

# docker.compose values

you can change the values of the volume name, the image tag and the container name.

---
