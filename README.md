# cloudflare-ddns-compose

## Run on local machine for tests

### Create an environment file for local test with your correct values
~~~
# ./cloudflare/configs/environment/local.env
# EMAIL=me@example.org
API_KEY=<CF API TOKEN>
ZONE=example.org
# Record to be changed could be a subdomain as well
# SUBDOMAIN=subdomain
~~~

### Then run the service
~~~
docker-compose -f docker-compose.base.yml -f docker-compose.local.yml -p cloudflare-dyndns up -d
~~~



## Run on your production machine

### Create an environment file for local, with your correct CF values
~~~
# ./cloudflare/configs/environment/local.env
# EMAIL=me@example.org
API_KEY=<CF API TOKEN>
ZONE=example.org
# Record to be changed could be a subdomain as well
# SUBDOMAIN=subdomain
~~~

### Then run the service
~~~
docker-compose -f docker-compose.base.yml -f docker-compose.production.yml -p cloudflare-dyndns up -d
~~~