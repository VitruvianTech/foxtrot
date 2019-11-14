# FoxZero™ JIRA

This Docker setup includes the official Atlassian JIRA Software Docker image with Postgres, along with workflow, add-on, board, and user group configuration necessary to support the FoxZero™ FAST™ product lifecycle management (PLM) methodology.

## Quick Launch

By default, FoxZero™ JIRA runs on port `8080` on your server.

`[DOMAIN=jira.example.com] [PORT=8080] docker-compose up [-d]`

When setting up the instance, choose Import, and type `foxzero.zip` in the input field.

## SSL

FoxZero™ JIRA uses Let's Encrypt and Nginx to setup a secure SSL (HTTPS) reverse web proxy.

```
DOMAIN=jira.example.com EMAIL=email@example.com SCHEME=https SECURE=true [PROXY_PORT=443] \
    docker-compose -f docker-compose.yml -f docker-compose.http.yml up [-d]
```

---

© 2019 FoxZero Media (a VitruvianTech® brand)
