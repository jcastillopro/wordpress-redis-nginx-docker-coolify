# wordpress-redis-nginx-docker-coolify
docker compose-based stack of wordpress with mariadb, nginx, redis optimised for forking and deploying via coolify
This version does not include a reverse proxy for a standalone deploying to the default VPS. This is because coolify got it's own reverse proxy, so we use it via labels or leave it to be handled by coolify itself.

TODO: create 2nd separate compose file, for prod we should copy wp files and mount persistant storage, for dev we can mount src folder and hot reload updates 

Inspiration:
https://www.ddmboss.com/posts/wordpress-docker-development-set-up-with-traefik-redis-and-nginx/