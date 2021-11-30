[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ffusionfabric%2Fffdc-sample-retail-webapp%2Fmaster%2Fazuredeploy.json)
[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/fusionfabric/ffdc-sample-retail-webapp)

# FFDC Sample Web App Using FFDC Design System

This repository contains a sample application using [FFDC Design System](https://github.com/fusionfabric/finastra-design-system) for front-end and [FusionFabric.cloud](https://developer.fusionfabric.cloud) for backend service.

<img src="retail-app-demo.gif" width="80%">

## Installation

1. Clone this repository

```
git clone https://github.com/fusionfabric/ffdc-sample-retail-webapp.git
```

2. Register FFDC application

You need to register an application on [FusionFabric.cloud Developer Portal](https://developer.fusionfabric.cloud) and select [Account Information (US) - B2C](https://developer.fusionfabric.cloud/api/b2c-account-v1-fc77362a-c2ee-4b23-b20e-5621249eb7a4/docs#tag/Accounts) API.

3. Setup environment variables

Duplicate `.env.template` file and rename it it `.env`, then add `CLIENT_ID` and `CLIENT_SECRET` of application created at step 2.

4. Run `npm install`

## Build

This application contains two applications, Angular Application and ExpressJs application
> You will need to build both client and server

```
# Server build
npm run build:server

# Client build
npm run build
```
\
Optionnally, you can also run in watch mode.

```
npm run build:server:watch
npm run build -- --watch
```

To build Angular Application for production, use `npm run build -- --prod`

<br>

## Running application

After building applications, now you can run it:

```
npm run start:server
```

or with debug mode

```
npm run start:server:debug
```

Go to http://localhost:3000 and enjoy demo application.

## Credentials

For testing purpose, you can login with one of the following credentials:

| User        | Password |
| :---------- | :------- |
| `ffdcuser1` | `123456` |
| `ffdcuser2` | `123456` |

## Environement variables

| Variable                  | Default value                                                                   |
| :------------------------ | :------------------------------------------------------------------------------ |
| `CLIENT_ID`               |                                                                                 |
| `CLIENT_SECRET`           |                                                                                 |
| `SESSION_SECRET`          |                                                                                 |
| `FFDC_URL`                | `https://api.fusionfabric.cloud`                                                |
| `PORT`                    | `3000`                                                                          |
| `HOST`                    |                                                                                 |
| `AUTHORIZATION_WELLKNOWN` | `${FFDC_URL}/login/v1/sandbox/.well-known/openid-configuration`                 |
| `LOGOUT_URL`              | `https://login.microsoftonline.com/finastra.onmicrosoft.com/oauth2/v2.0/logout` |
| `ROOT_URL`                | `$HOST` or `http://localhost:${PORT}`                                           |

## License

These sample applications are released under the MIT License. See [LICENSE](./LICENSE) for details.
