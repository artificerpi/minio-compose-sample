# minio-compose-sample

## Prequiresites
- [Docker](https://www.docker.com/)
- [docker-compose](https://docs.docker.com/compose/)

### Customize your configuration
- Edit [docker-compose.yml](./docker-compose.yml) file to scale the minio nodes.
- Edit [nginx-minio.conf](./nginx-minio.conf) file to setting nginx proxy.

## Setting up
### Docker
- Installation
https://docs.docker.com/install/#time-based-release-schedule

Usually, users install docker-ce on their ubuntu distro, then following this link
https://docs.docker.com/install/linux/docker-ce/ubuntu/

### docker-compose
- Installation
https://docs.docker.com/compose/install/#install-compose

### Deployment
Enter the directory of this project, then use following commands to handle deployment.
- start or update
``` bash
docker-compose up -d
```
- stop
``` bash
docker-compose stop
```

- remove
``` bash
docker-compose rm
```

Go to http://your-host-ip:9000 to visit the minio web page.
Default username is `minio` and password is `artificerpi`, and you can change and redeploy to make it take effect.