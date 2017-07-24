# Nginx Configuration

My nginx configuration.

### Usage

1. Replace the `${HOST_IP}` in the `service_*.conf` with the host ip
2. Run with the following command:

	docker run \
		--name ansel-nginx \
		-p 80:80 \
		-d \
		--restart always \
		-v ${NGINX_CONF_DIR}:/etc/nginx/conf.d \
		nginx

### Proxy Setting

| Server Name | Proxy Pass Port |
| --- | --- |
| ghost.ansellin.club (default) | 2368 |
| jupyter.ansellin.club | 8888 |
