
## Requirements

- [Docker](https://docs.docker.com/install/)
- [Docker Documentation](https://docs.docker.com/)

## Installation

1. Clone this rep.

2. Run `docker-compose build`

3. Run `docker-compose up -d`

If you get `Error starting userland proxy: listen tcp 0.0.0.0:3308: bind: address already in use` change db->ports from 3308 to an unbound port at docker-compose.yml (line 16).

4. The 3 containers are deployed: 

```
Creating kuznetsovadocker_db_1    ... done
Creating kuznetsovadocker_php_1   ... done
Creating kuznetsovadocker_nginx_1 ... done
```

5. Run command `docker exec -it  kuznetsovadocker_php_1 bash`

6. Run command `sh init.sh`

Press `yes` when prompted

7. Go to localhost:80/converter or 127.0.0.1:80/converter to use converter. 
127.0.0.1:80/admin to work with currencies.

