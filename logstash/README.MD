## Logstash synchronisation of CloudHub data into Elasticsearch

### get_cloudhub_app_logs.conf
This config authenticates to CloudHub and performs synchronisation of all application logs for a particular environment.
![Kibana1](../images/kibana1.png)
![Kibana2](../images/kibana2.png)

#### Command to run:
```sh
cd elastic-cloudhub-observability

ES_USER=elastic \
ES_HOST=https://eshost:9200 \
ES_PASS=espass \
CH_USER=cloudhubuser \
CH_PASSWORD=cloudhubpassword \
CH_ENV=Production \
NUM_LOG_LINES=300 \
logstash --path.settings $PWD/logstash/config
```
