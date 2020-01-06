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
git clone https://github.com/mesg-foundation/application-erc20-notification.git
```

## Create configuration file

Copy the `.env.example` to `.env`.

This file contains required configurations needed for the application.
You need to replace the `...` by the right value.

## Replace application.yml

You need to replace email at `'__YOUR_EMAIL_HERE__'` by your email.

```yml
  ...
  - type: task
    instance:
      src: https://github.com/mesg-foundation/service-email-sendgrid
      env:
        - SENDGRID_API_KEY=$(env:SENDGRID_API_KEY)
    taskKey: send
    inputs:
      from: 'test@erc20notification.com'
      to: '__YOUR_EMAIL_HERE__'
      subject: 'ERC20 transfer'
      text:
        key: result
  ...
```

## Deploy MESG process

```bash
mesg-cli process:dev application.yml --env PROVIDER_ENDPOINT=$PROVIDER_ENDPOINT --env SENDGRID_API_KEY=$SENDGRID_API_KEY
```
