# Debug project for the Caddy GRPC plugin

### How it works

Web <--- HTTP 1.1/GRPC-WEB ---> Caddy Proxy <--- HTTP2.0/GRPC ---> Backend

### GRPC definitions

A simple `Greeter` service from the `/protos` folder

### Test Components

- Backend: a precompiled GRPC server, which implements the `Greeter server`
- Web: a prebuilt precompiled implementation of the Web APP, which implements the `Greeter client`
- Caddy-grpc a prebuilt `Caddy` master with the GRPC [plugin](https://github.com/mholt/caddy-grpc-web)
- Caddyfile with a proper definition

### Usage

- Check the Caddyfile. Change the hardcoded IP `192.168.1.93` to the proper value
- docker-compose up
- open the web browser and run `localhost`
- Press `F12` to open a browser console
- Hit the counter button to see the results

### Expected results

Each time clicking a `Count is` button a new message in the Web browser console appears
