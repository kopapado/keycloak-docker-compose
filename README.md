# Keycloak Docker Compose

## Start containers (detached)
``` 
docker-compose up -d
```

## Stop containers
```
docker-compose stop
```

## Check Keycloak logs
```
docker logs -f keycloak-docker-compose-keycloak-1
```

## Export realms and copy them to the local system
```
docker exec -it keycloak-docker-compose-keycloak-1 /opt/keycloak/bin/kc.sh export --dir /tmp/export
docker cp keycloak-docker-compose-keycloak-1:/tmp/export .
```