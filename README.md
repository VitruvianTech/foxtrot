# Foxtrot™

## Tactical Project Management

Foxtrot™ is a project management philosophy based on (good parts of) Agile principles, and Atlassian JIRA Software.

This Docker setup includes the official Atlassian JIRA Software Docker image with Postgres, along with add-ons, workflows, and configuration necessary to support the VitruvianTech® Foxtrot™ methodology.

## Quick Launch

By default, Foxtrot™ runs on port `8080` on your server.

`[DOMAIN=foxtrot.example.com] [PORT=8080] docker-compose up [-d]`

## SSL

Foxtrot™ uses Let's Encrypt and Nginx to setup a secure SSL (HTTPS) reverse web proxy.

```
DOMAIN=foxtrot.example.com EMAIL=email@example.com SCHEME=https SECURE=true [PROXY_PORT=443] \
    docker-compose -f docker-compose.yml -f docker-compose.http.yml up [-d]
```

---

© 2019 VitruvianTech
