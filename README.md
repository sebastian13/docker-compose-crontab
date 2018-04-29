# Container-Crontab

[Rancher's container-crontab](https://github.com/rancher/container-crontab) acts as a crontab for other containers. I'm just providing the missing **docker-compose.yml** here.

### Start the cron-container

```shell
docker-compose up -d
```

### Define a schedule

By adding the label `cron.schedule` to a docker-compose.yml file while starting the container, the crontab will start the respective container in the defined schedules or intervals.

```yaml
labels:
  cron.schedule: "0 0 1 * * MON"
```