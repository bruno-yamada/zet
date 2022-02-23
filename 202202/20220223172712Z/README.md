# Docker on MacOS

Docker-Desktop is no longer free on MacOS

## Alternatives
- minikube
  - worked for a while, but too much custom configuration is needed if you are
    used to how docker-desktop works, because minikube still runs on VMs and
    tools such as `localstack` expect docker to run locally, and are a pain to
    configure when running with minikube
- rancher-desktop
  - best option, most transparent
- podman, kind, k3d
  - haven't tried

## Installing rancher-desktop
> haven't tested on M1 macs

Install rancher-desktop:
```
brew install --cask rancher
```

Install docker and docker-compose if needed:
```
# docker
brew install docker

# docker-compose
mkdir -p ~/.docker/cli-plugins/
curl -SL https://github.com/docker/compose/releases/download/v2.2.3/docker-compose-darwin-x86_64 -o ~/.docker/cli-plugins/docker-compose
chmod +x ~/.docker/cli-plugins/docker-compose
```

When starting services with docker-compose you might see an error:
```
error getting credentials - err: exec: "docker-credential-desktop": executable file not found in $PATH, out: ``
```

if the above happens:
```
brew install docker-credential-helper
```
and In ``~/.docker/config.json` change `credsStore` to `credStore`


> tags: docker; macos; mac;

> uid: 20220223172712Z

> links: 

