# config-repository

## Api de récupération d'une ressource

```bash
/{application}/{profile}[/{label}]
/{application}-{profile}.yml
/{label}/{application}-{profile}.yml
/{application}-{profile}.properties
/{label}/{application}-{profile}.properties
```

Avec :

- application : nom application, exemple ms-service
- profile : le profile choisi. Correspond typiquement à l'environnement, exemple : staging, uat, prod


```bash
export SPRING_PROFILES_ACTIVE=prod
```

```bash
$ java -jar -Dspring.profiles.active=prod demo-0.0.1-SNAPSHOT.jar
```

- label : version de la ressource. Par défault sur Git c'est master.

