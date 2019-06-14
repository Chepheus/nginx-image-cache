# Nginx Image Cache

### To run nginx:
> docker-compose up -d

### To testing:
> docker build -t yokogawa/siege ./siege/

#### Cached variant
> docker run --network custom_network --rm -t yokogawa/siege -r300 -c255 --file=url_cache.txt http://nginx/

##### Result
![Cached images](/images/cache.png)

#### No Cached variant
> docker run --network custom_network --rm -t yokogawa/siege -r300 -c255 --file=url_no_cache.txt http://nginx/

##### Result
![No Cached images](/images/no_cache.png)