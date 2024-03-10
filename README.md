# ec2-setup

This repo contains docker compose file that is used to host my projects:

- [DokChat](https://dokchat.dokurno.dev) on port `8080`
- [StockedUp](https://stockedup.dokurno.dev) on port `8081`

This setup was not made to be replicated. This repo servers as documentation for this setup.

## Details

This docker-compose file spins up following containers structure:

![structure](https://i.imgur.com/T9WZsrD.png)


## Deploy guide
1. Clone this repository to any VPS provided. Originally it was designed for [EC2](https://aws.amazon.com/ec2/) but nowadays I run it on [Linode](https://www.linode.com).
1. Navigate to repository folder
   ```
   cd ec2-setup
   ```
1. Create `.stockedup.env` and `.dokchat.env` files that match the examples on both repos. You need to manually create API keys and other resources here.
1. Spin up docker images. This will run all services locally.
   ```
   docker compose up
   ```
1. Install NGINX and move files from `nginx-config` to `/etc/nginx/conf.d`.
1. Restart NGINX:
   ```
   sudo systemctl restart nginx.service
   ```
1. Instal and configure [Certbot](https://certbot.eff.org/instructions) for Let's Encrypt certificates
