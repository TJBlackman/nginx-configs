# Nginx Configs

A project the allows you to quickly copy/paste Nginx config files with good default settings: This project was bootstrapped from Digital Ocean's [Nginx Config Generator](https://www.digitalocean.com/community/tools/nginx).

## How to use

For every domain you want to support:

- Create a file in `./conf.d/` using the domain you with to support:
  - Example: `./conf.d/mysite.com.conf` or `./conf.d/admin.mysite.com.conf`
- Copy all the config from `./conf.d/DOMAIN.conf` into your new file.
- Find and replace `__DOMAIN.COM__` with the domain you with to support.
- To active the site, create an empty file with the same name in the `/sites-enabled/`
- Restart your nginx server.

## Copy Checklist

Modifications to the `./conf.d/DOMAIN.conf` you should double check:

- [ ] Ctrl+f for `__DOMAIN.COM__` to make sure you replace them all
- [ ] Confirm root directory location, on line 5
- [ ] Confirm Reverse Proxy settings on line 24
  - [ ] Do you need a prefix, like `/api` or not?
- [ ] Ctrl+f for `__APPLICATION__:__PORT__` to replace with your reverse proxy application URL
- [ ] Confirm SSL certification locations on lines 8 and 41.
- [ ] Confirm Let's Encrypt Acme Challenge location on line 54
