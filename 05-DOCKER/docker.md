# Docker

## Diagnóstico

```powershell
docker --version
docker info
docker ps
docker ps -a
docker images
```

## Build e execução

```powershell
docker build -t nome-imagem .
docker run --name nome-container nome-imagem
docker run -d -p 8000:8000 --name nome-container nome-imagem
```

## Logs

```powershell
docker logs nome-container
docker logs -f nome-container
```

## Parar e remover

```powershell
docker stop nome-container
docker start nome-container
docker restart nome-container
docker rm nome-container
docker rmi nome-imagem
```

## Docker Compose

```powershell
docker compose up -d
docker compose down
docker compose logs -f
docker compose build --no-cache
```

## Limpeza

```powershell
docker system df
docker system prune
```

Use volumes para banco e arquivos persistentes. Container sem volume é memória de peixe com interface de rede.
