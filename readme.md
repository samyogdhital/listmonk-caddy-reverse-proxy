# Listmonk Installation Guide with Caddy reverse proxy and SSL certificate

This guide will help you nstall Listmonk with proper SSL certification on your domain using Docker.

## Prerequisites

- An EC2 instance or any cloud instance
- Git installed on your instance
- Docker installed on your instance

## Steps

1. **Create a Listmonk Folder and Navigate Into It**

   Open your terminal and run the following commands to create a new directory named 'listmonk' and navigate into it:

   ```bash
   mkdir listmonk && cd listmonk
   ```

   Do not use sudo to create directory

2. **Clone the Repository Inside the Listmonk Folder**

   Run the following command to clone the repository into the 'listmonk' directory:

   ```bash
   git clone git@github.com:samyogdhital/listmonk-caddy-reverse-proxy.git .
   ```

3. **Follow Listmonk manual installation on production**

   Head over to this repo and follow the usal installation https://listmonk.app/docs/installation/#manual-docker-install_1

4. **Make changes to Caddyfile inside ./caddy/Caddyfile**

   Provide your email and the domain where you will be hosting your listmonk instance. (It can be subdomain as well)

## Conclusion

Now for the final step run all the containers in detached mode and you should be good to go.

```bash
docker compose up -d
```

You should now have Listmonk running on your EC2 instance with Lets encrypt SSL certificate.
