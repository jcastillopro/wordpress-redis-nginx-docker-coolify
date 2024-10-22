# wordpress-redis-nginx-docker-coolify
docker compose-based stack of wordpress with mariadb, nginx, redis optimised for forking and deploying via coolify
This version does not include a reverse proxy for a standalone deploying to the default VPS. This is because coolify got it's own reverse proxy, so we use it via labels or leave it to be handled by coolify itself.


Inspiration:
https://www.ddmboss.com/posts/wordpress-docker-development-set-up-with-traefik-redis-and-nginx/