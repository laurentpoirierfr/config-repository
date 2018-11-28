# config-repository

## Exemle d'accès ressources


Mode Api :


```bash
http://localhost:8888/ms-admin/default
http://localhost:8888/ms-admin/default/master
```

```bash
http://localhost:8888/ms-service/prod
http://localhost:8888/ms-service/prod/master
http://localhost:8888/ms-service/prod/release-1.0.0
```



Mode flat :

```bash
http://localhost:8888/ima/default/master/tomcat-users.xml
http://localhost:8888/ima/default/master/ms-logger/tomcat-users.xml
```

> Peut importe le nom de l'application, ici ima, cela permet d'accéder directement à une ressource.





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

Référence :

- [https://cloud.spring.io/spring-cloud-config/multi/multi__spring_cloud_config_server.html](https://cloud.spring.io/spring-cloud-config/multi/multi__spring_cloud_config_server.html)