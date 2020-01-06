# ERC20 Notification

## Install MESG Engine

Make sure that [MESG Engine](https://github.com/mesg-foundation/engine) is installed and running on your computer.
You can run the following command to install and start the Core:

```bash
 npm install -g @mesg/cli
```

## Download source

Download the source code of the application. You can clone this repository by using the following command:

```bash
git clone https://github.com/
```

## Create configuration file

Copy the `.env.example` to `.env`.

This file contains required configurations needed for the application.
You need to replace the `...` by the right value.

## Deploy MESG process

```bash
mesg-cli process:dev application.yml --env PROVIDER_ENDPOINT=$PROVIDER_ENDPOINT --env SENDGRID_API_KEY=$SENDGRID_API_KEY
```
