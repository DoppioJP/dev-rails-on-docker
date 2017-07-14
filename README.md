# Rails development in Docker

## Aliases

```
alias dweb='docker-compose run --rm web'
```

## Recipe

1. Copy files to your-new-project
   - `Dockerfile`
   - `docker-compose.yml`
   - Gemfile
2. Change in `docker-compose.yml` the bundle/image name to be `yournewproject_web`
3. Commit with "I'm going to write Rails in Docker"
4. `docker-compose build`
5. Initialise your new Rails project with
   ```
   rails new your-new-project .
   ```
