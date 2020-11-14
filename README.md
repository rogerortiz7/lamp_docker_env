# Simple LAMP ENV with Docker

## Provisioned:
- Debian
- MySql: 8
- PHP: 7.3 with Apache, PDO, myslqi, ZLIB, phpunint as global, composer as global
# SetUp

- Move the files to your project directory
- Run docker-composer up -d
- Set up you PHP app in /www and Enjoy ;)

## How it Works?
Docker compose bind your /www directory (you can change the name as you want) with the public Apache's public directory in container

## Entry in container
- WorkSpace: Just execute docker-compose exec web bash
- MySql: Just execute docker-compose exec db bash

## Extra

If you want add more addons just add it in /php/Dockerfile

