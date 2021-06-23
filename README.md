# express-chrome-ssr

# Server side rendering with puppeteer / headless chrome

This repo is meant to be an example of implementing nodejs, expressjs, and puppeteer for server side rendering using headless chrome.

To boost performance, the same chrome instance is reused on sequential loads.

### Packages used

Open source projects:

-   [Express] - Serving the requests
-   [Puppeteer] - Headless Chrome Node.js API
-   [PM2] - Node.js Production Process Manager with a built-in Load Balancer

### Installation

[Node.js 8+](https://nodejs.org/) is required to run.

```sh
$ npm install https://github.com/isharadilshan/reactjs-prerender.git
or
$ yarn add https://github.com/isharadilshan/reactjs-prerender.git
```

Install the dependencies and devDependencies and start the server.

```sh
$ git clone https://github.com/isharadilshan/reactjs-prerender.git
$ cd express-chrome-ssr
$ npm install (or yarn install)
$ npm run dev (or yarn dev)
```

For production environments...

```sh
$ git clone https://github.com/isharadilshan/reactjs-prerender.git
$ cd express-chrome-ssr
$ npm install (or yarn install)
$ npm run start_production_server (or yarn start_production_server)
```

### Usage

Specifying a port is optional, the default one is 3000

```sh
$ yarn start_production_server --port=3000
```

-   Start the server (locally or on production)
-   Visit /ssr and add your url in the url param

The script has two url's (you can replace localhost with your domain if running it on server or virtual box)

-   `http://localhost:3000/test` - To make sure the server is running
-   `http://localhost:3000/ssr?url=THE_URL_TO_RENDER` - Will return server side rendered html of the url

### Development

Go to the project folder and run:

```sh
$ npm run dev (or yarn dev)
```

A server will be spawned accesible on [localhost:3000](http://localhost:3000) with live reload when changes are done.

#### Building for source

For production release:

```sh
$ npm run build (or yarn build)
```

To start the pm2 server:

```sh
$ npm run start_production_server (or yarn start_production_server)
```

To kill the pm2 server:

```sh
$ npm run kill_production_server (or yarn kill_production_server)
```
