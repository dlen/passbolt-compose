# passbolt docker compose

This is a docker compose that eases passbolt execution.
It is yet an unofficial docker composer repo for passbolt.

It comes with a self signed certificate bundled and some gpg dummy keys.
The repo as it is it has development/testing purposes.

## Usage

* Launch the containers: ```docker-compose up```
* Get container ip address: ```docker inspect --format='{{.Name}} - {{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' passboltcompose_passbolt_1```
* Browse the previous ip address obtained on port 443 https://container_ip

### Non GNU/Linux users

Host environments such as macos require to expose ports on the host and access the continaers through localhost.
Keep this in mind as you would need to add a ```ports:``` section on the passbolt service declared in ```docker-compose.yml```

More info: [limitations](https://docs.docker.com/docker-for-mac/networking/#known-limitations-use-cases-and-workarounds)

