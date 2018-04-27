# Rails development in Docker

## Aliases
Adding this alias to your shell profile will be very useful

```
alias dweb='docker-compose run --rm web'
```

## Recipe

1. Copy files to your-new-project
   - `Dockerfile`
   - `docker-compose.yml`
   - Gemfile
   - Gemfile.lock
2. Change in `docker-compose.yml` the bundle/image name to be `yournewproject_web`
3. Commit with "I'm going to write Rails in Docker"
4. `docker-compose build`
5. Commit again
   ```
   git add .
   git commit -m "Built my image with rails"
   ```
6. Initialise your new Rails project with
   ```
   dweb rails new .
   ```
   You will be asked if to overwrite `Gemfile.lock` - what do you think? ;-)

7. All further commands use with `dweb ` prefix, i.e. `dweb rails c`
8. Further initial steps which are normal for Rails writing:
   - `dweb bundle` - to install basic gems of the newly created app
9. Serve the app with `docker-compose up`, see it at http://localhost:3000

