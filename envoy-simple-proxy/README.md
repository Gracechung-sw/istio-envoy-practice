## Backend apps

1. localhost:1111
2. localhost:2222
3. localhost:3333
4. localhost:4444

## Installation

### Install Envoy on Mac OSX¶

You can install Envoy on Mac OSX using the official brew repositories.

```
brew update
brew install envoy
```

### Install Envoy using Docker¶

You can run Envoy using the official Docker images.

The following commands will pull and show the Envoy version of current images.

```
docker pull envoyproxy/envoy-dev:416c6f5a1d85ceb5ed9cc173533eb36b2e2dcac0
docker run --rm envoyproxy/envoy-dev:416c6f5a1d85ceb5ed9cc173533eb36b2e2dcac0 --version
```

## Configuration

Q. According to Envoy docs, there are 3 types of configuration.

- Configuration:Static
- Configuration:Dynamic from filesystem
- Configuration:Dynamic from control plane
  What's the difference of these?

### 1. Layer 7 Proxying

Listen a port and once listening to a port, Let's create a filter and then start basically mapping to the 4 Backends.  
Related file is `http.yaml`

After start Envoy with below command, go localhost:8080 then you can see https://www.envoyproxy.io:443.

## Let's start Envoy

```bash
envoy --config-path [specify which file you want to load]

ex. envoy --config-path http.yaml
```
