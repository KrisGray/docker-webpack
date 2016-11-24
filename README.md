# krisgray/docker-webpack

> Webpack in a container

```sh
$ docker pull krisgray/webpack
```

## Example: Serve dev

_Note: Assumes that default `webpack.config.js` exists at source root._

```sh
$ docker run \
  --rm \
  -i \
  -t \
  -v /path/to/source:/app \
  -p 8080:8080 \
  krisgray/webpack \
  webpack-dev-server --hot --inline --progress --host 0.0.0.0
```

### Example: Build

An example of building the dist.

_Note: Assumes that default `webpack.config.js` exists at source root._

```sh
$ docker run \
  --rm \
  -i \
  -t \
  -v /path/to/source:/app \
  krisgray/webpack \
  webpack
```