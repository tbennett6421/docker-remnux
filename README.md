# docker-remnux

A compilation of the docker commands wrapped into docker-compose for ease-of-use

## Creds
This uses the default creds of the following
```
username: remnux
password: malware
```

it is recommended you change the password or implement ssh key authentication

## Run

```bash
# run the solution detached
docker-compose -f docker-compose.yml up -d
# connecting to the container via ssh
ssh remnux@127.0.0.1 -p 1022
# Connecting to the container over X11-forwarding (SSH)
ssh remnux@127.0.0.1 -p 1022 -Y
```

## Testing X11 access
If you'd like to test your X11 to ensure it its woking you can do the following.
```bash
## Connect to the container
ssh remnux@127.0.0.1 -p 1022 -Y
sudo apt-get update
sudo apt-get install x11-apps
xclock
```

A listing of all available version tags can be found on the [Docker Hub](https://hub.docker.com/r/remnux/remnux-distro/tags) page.

## Refs

* [https://remnux.org/](https://remnux.org/)
* [https://hub.docker.com/r/remnux/remnux-distro/](https://hub.docker.com/r/remnux/remnux-distro/)
