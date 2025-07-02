# Basic Jellyfin media stack

Remember to define the .env file when running both docker composes. use the `--env-file {relative/file/path}` before `up`. This allows you to use one .env file for multiple docker-compose.yml files.

Use: 
```ruby
docker compose --env-file ../.env up
```
from within the docker-compose dir
