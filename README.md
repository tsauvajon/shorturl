# ShortURL

[![codecov](https://codecov.io/gh/tsauvajon/shorturl/branch/master/graph/badge.svg?token=EbP2Znh1m3)](https://codecov.io/gh/tsauvajon/shorturl)

Hello! I'm a service designed to shorten URLs.  
I'm composed of an API server, an in-memory database and a front-end interface.

![Demo](/demo.gif)

## Example usage

### Start the API

```sh
cargo run
```

### Use the API

```sh
$ curl -X POST 127.0.0.1:50002/tsauvajon -d "https://linkedin.com/in/tsauvajon"
/tsauvajon now redirects to https://linkedin.com/in/tsauvajon

$ curl 127.0.0.1:50002/tsauvajon                                               
redirecting to https://linkedin.com/in/tsauvajon...
```

### Build the front-end

The front-end is designed to be served by the API, so make sure to have it
started and running.

```sh
$ cd front/
$ make build
$ sudo cp -r dist /etc/shorturl/dist
$ echo http://127.0.0.1:50002/
```
