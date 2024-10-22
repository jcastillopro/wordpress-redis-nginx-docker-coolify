# wordpress-redis-nginx-docker-coolify
docker compose-based stack of wordpress with mariadb, nginx, redis optimised for forking and deploying via coolify
This version does not include a reverse proxy for a standalone deploying to the default VPS. This is because coolify got it's own reverse proxy, so we use it via labels or leave it to be handled by coolify itself.

TODO:
[] check setup from the article
[] test how is it deployed
[] improve to use with coolify
[] split into two compose files - with and without traefik
[] decide how to move params to env vars


Other stack implementations:
- Stack for common docker compose deploy (coolify-free)
- Stack for common deploy, development-ready with mounting volumes for themes and plugins from repo (or copying)
Ideal goal - to make all of those via single repo.

Inspiration:
https://www.ddmboss.com/posts/wordpress-docker-development-set-up-with-traefik-redis-and-nginx/