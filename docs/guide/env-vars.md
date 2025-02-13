# Environment variables

This is the list of the actually supported env vars:

- `NETWORK_KEY`: Zwave Network key
- `HTTPS`: Enable https
- `SESSION_SECRET`: Used as secret for session. If not provided the default one is used
- `USE_SECURE_COOKIE`: Set the cookie [secure](https://github.com/expressjs/session#cookiesecure) option.
- `PORT`: The port to listen to for incoming requests. Default is `8091`
- `HOST`: The host address to bind to. Default is `0.0.0.0`
- `STORE_DIR`: The absolute path to the directory where all files will be stored. Default is `<path to your z2m dir>/store`
- `ZWAVEJS_EXTERNAL_CONFIG`: Mostly needed for docker users, it's the path to the folder used by zwave-js to [store config database](https://zwave-js.github.io/node-zwave-js/#/usage/external-config?id=specifying-an-external-config-db-location), by default on docker image it is `/usr/src/app/store/.config-db`. For users that are using a custom `STORE_DIR` this must be changed too
- `MQTT_NAME`: The name used as client name when connecting to the mqtt server. Overrides `mqtt.name` in `settings.json`

This env vars can be used when running webpack dev server with HMR (most users will not need them):

- `SERVER_PORT`: The port the server is running. Default is `8091`
- `SERVER_SSL`: Set to 'true' if server is using HTTPS / WSS scheme
- `SERVER_HOST`: The host address the server is binded to. Default is `0.0.0.0`
- `SERVER_URL`: Complete URL to server. If not set a combination of `SERVER_SSL`, `SERVER_HOST` and `SERVER_PORT` will be used.
