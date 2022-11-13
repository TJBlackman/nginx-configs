# Nginx Configs

A project the allows you to quickly copy/paste Nginx config files with good default settings: This project was bootstrapped from Digital Ocean's [Nginx Config Generator](https://www.digitalocean.com/community/tools/nginx).

## How to use

For every domain you want to support:

- Create a file in `/sites-available/` using the domain you with to support:
  - Example: `/sites-available/mysite.com` or `/sites-available/admin.mysite.com`
- Copy all the config from `/sites-available/DOMAIN.config` into your new file.
- Find a replace `__DOMAIN.COM__` with the domain you with to support.
- To active the site, create an empty file with the same name in the `/sites-enabled/` directory:
  - Example: `/sites-available/mysite.com` with config and `/sites-enabled/mysite.com` as an empty file
- Restart your nginx server.

## Copy Checklist

Modifications to the `/sites-available/DOMAIN.conf` you should double check:

- [ ] Ctrl+f for `__DOMAIN.COM__` to make sure you replace them all
- [ ] Confirm root directory, on line 5
- [ ] Confirm Reverse Proxy settings on line 24
- [ ] Ctrl+f for `__APPLICATION__:__PORT__` to replace with your reverse proxy application URL
- [ ] Remove `DOMAIN.CONF` from `/sites-enabled` directory before going live.
#   n g i n x - c o n f i g s  
 #   n g i n x - c o n f i g s  
 