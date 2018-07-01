# Airflow Services

## Services

Location: `/etc/systemd/system/`


```
sudo systemctl start airflow-webserver.service
sudo systemctl start airflow-scheduler.service
sudo systemctl start airflow-worker.service
sudo systemctl start airflow-flower.service

```

## Postgres

```
sudo -i -u postgres
sudo service postgresql restart
```

## Queue

```
sudo systemctl start redis
```

## Process

0. Sync config and dags
1. Stop master services
2. Start redis on remote worker
3. Start remote worker
4. Start airflow services on master

## Links
[Airflow inside a virtual environment](https://medium.com/@vando/airflow-inside-a-virtual-enviroment-and-integrated-with-systemd-3b6427bd6430)  
[Install and Use PostgreSQL on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04)  
[Install and Configure Redis on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-redis-on-ubuntu-16-04)  
[Use Systemctl to Manage Systemd Services](https://www.digitalocean.com/community/tutorials/how-to-use-systemctl-to-manage-systemd-services-and-units)  
[Journalctl](https://www.digitalocean.com/community/tutorials/how-to-use-journalctl-to-view-and-manipulate-systemd-logs#journal-maintenance)  
[Installing and Configuring Apache Airflow](http://site.clairvoyantsoft.com/installing-and-configuring-apache-airflow/)  
