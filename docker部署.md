```
version: '3.8'

services:
  9router:
    image: decolua/9router:latest
    container_name: 9router
    restart: unless-stopped
    ports:
      - "20128:20128"
    volumes:
      - ${HOME}/.9router:/app/data
    environment:
      - DATA_DIR=/app/data
      - JWT_SECRET=9router-prod-jwt-2026-06-10-x8FvK2mQp7Nz4LdRc1TwUa6Hy9Sb3JeM
      - INITIAL_PASSWORD=123456
      - HOSTNAME=0.0.0.0
      - REQUIRE_API_KEY=true
```
