# Keycloak Smart Auth



## Docker build

The Dockerfile has 3 steps:

1. Clone the [OpenMSR keycloak smart auth repo](https://github.com/openmrs/openmrs-contrib-keycloak-smart-auth)
2. Build the EAR
3. Deploy the EAR in keycloak

To Build and publish:
```bash
docker build . -t trifork/keycloak-smart-auth:{version}

docker push trifork/keycloak-smart-auth:{version}
```

Images can be found on [Docker Hub](https://hub.docker.com/r/trifork/keycloak-smart-auth)

## Docker compose setup

The docker compose setup uses a postgres db and imports a preconfigured realm on first startup.

The configuration is inspired by [this guide](https://wiki.openmrs.org/display/projects/Using+Keycloak+for+SMART-on-FHIR+Support)

To run

```bash
docker-compose up -d
```
