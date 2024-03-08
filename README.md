# ec2-setup

This repo contains docker compose file that is used to host my projects:

- [DokChat](https://dokchat.dokurno.dev) on port `8080`
- [StockedUp](https://stockedup.dokurno.dev) on port `8081`

This repo is primarily for managing my personal deployment.

## Deploy guide
1. Clone this repository to EC2
1. Navigate to repo folder
1. Create `.stockedup.env` and `.dokchat.env` files that match the examples on both repos
1. Run
   ```
   docker compose up
   ```

## Details

This docker-compose file spins up following containers structure:

![structure](https://i.imgur.com/T9WZsrD.png)

