# Architecture
![architecture](../../imgs/architecture.png)
![architecture_2](../../imgs/architecture_2.png)

## Commands
- Clean Up
```sh
k delete -f .
```
- Atualizar
```sh
k apply -f .
```

### Dumb Way
Abaixo foi quando eu não sabia que poderia referenciar o path atual com `.`

- Clean Up
```sh
k delete pod postgres
k delete pod redis
k delete pod result-app
k delete pod voting-app
k delete pod worker
k delete svc svc-postgres
k delete svc svc-redis
k delete svc svc-voting-app
k delete svc svc-result-app
```
- Atualizar
```sh
k apply -f postgres.yaml
k apply -f redis.yaml
k apply -f result-app.yaml
k apply -f voting-app.yaml
k apply -f worker.yaml
k apply -f svc-postgres.yaml
k apply -f svc-redis.yaml
k apply -f svc-voting-app.yaml
k apply -f svc-result-app.yaml
```