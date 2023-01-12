
# Installing Mastodon

This is the code for the series I wrote, you can read the full article here https://zaher.dev/blog/mastodon-on-k3s---part-3


```bash
docker run --rm -it -w /app/www --entrypoint rake lscr.io/linuxserver/mastodon secret
docker run --rm -it -w /app/www --entrypoint rake lscr.io/linuxserver/mastodon mastodon:webpush:generate_vapid_key
docker exec -it -w /app/www mastodon bin/tootctl accounts modify <username> --role Owner
```