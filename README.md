
# Services

Location: `/etc/systemd/system/`


```
sudo systemctl start airflow-webserver.service
sudo systemctl start airflow-scheduler.service
sudo systemctl start airflow-worker.service
sudo systemctl start airflow-flower.service

```

# Postgres

```
sudo -i -u postgres
sudo service postgresql restart
```

# Queue

```
sudo systemctl start redis 
```

# Process

0. Sync config and dags
1. Stop master services
2. Start redis on remote worker
3. Start remote worker
4. Start airflow services on master
