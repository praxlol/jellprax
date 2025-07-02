# Basic Jellyfin media stack

```ruby
git clone https://github.com/praxlol/jellprax
```

Create the networks before launching the compose files
```ruby
docker network create --driver bridge starr
docker network create --driver bridge qbit
```


Remember to define the .env file when running both docker composes. use the `--env-file {relative/file/path}` before `up`. This allows you to use one .env file for multiple docker-compose.yml files.

Use: 
```ruby
docker compose --env-file ../.env up -d
```
from within the docker-compose dir

Annoyingly, you have to include the /env for compose down use:
```ruby
docker compose --env-file ../.env down
```

##Updating

###Updating Images
  All images
```ruby
docker-compose pull
```
  Single Image
```ruby
docker-compose pull qbittorent
```

###Updating Containers
  All containers
```ruby
docker-compose up -d
```
  Single container
```ruby
docker-compose up -d qbittorrent
```

Dont forget to prune old images
```ruby
docker image prune
```
