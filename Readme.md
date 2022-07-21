# Setup homeassistant and homekit

## install homekit

pre-requirements: install docker

docker compose, `docker-compose.yml`:

```
version: '3'
services:
  homeassistant:
    container_name: homeassistant
    image: "homeassistant/home-assistant:2022.7"
    volumes:
      - /PATH_TO_YOUR_CONFIG:/config
      - /etc/localtime:/etc/localtime:ro
    restart: unless-stopped
    privileged: true
    network_mode: host
```

sudo docker-compose up -d

## install hacs

https://hacs.xyz/docs/setup/download

## install xiaomi miio auto


小米设备添加到homekit： https://bbs.iobroker.cn/t/topic/13486
https://github.com/PiotrMachowski/Xiaomi-cloud-tokens-extractor
https://www.home-assistant.io/integrations/xiaomi_miio/#retrieving-the-access-token
