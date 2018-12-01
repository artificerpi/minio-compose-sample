# minio-compose-sample

## Prequiresites
- [Docker](https://www.docker.com/)

## Setting up
### Docker
- Installation
https://docs.docker.com/install/#time-based-release-schedule

Usually, users install docker-ce on their ubuntu distro, then following this link
https://docs.docker.com/install/linux/docker-ce/ubuntu/

### Deployment
Enter the directory of this project, then use following commands to handle deployment.
- start or update
``` bash
docker stack deploy -c docker-compose.yml minio
```

Go to http://your-host-ip:9000 to visit the minio web page.
Default username is `minio-artificerpi` and password is `minio-passw0rd`, and you can change and redeploy to make it take effect.
