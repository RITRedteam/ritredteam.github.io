---
layout: default
title: Deployment
parent: Br4vo6ix
grand_parent: Cross Platform
nav_order: 1
---

## Deployment

You're going to need two `.env` files, one for the server and one for the frontend.

```shell
# .env (need to source this file)
export PWN_URL=http(s)://<url for pwnboard>/generic

# frontend/.env
REACT_APP_GRAPHQL_URL=http://<Br4vo6x host fqdn/ip>:8080/query
```
