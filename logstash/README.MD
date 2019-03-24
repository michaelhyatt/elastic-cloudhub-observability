## Logstash synchronisation of CloudHub data into Elasticsearch

### get_cloudhub_app_logs.conf
This config authenticates to CloudHub and performs synchronisation of all application logs for a particular environment.

Command to run:
```sh
ES_USER=elastic \
ES_HOST=https://eshost:9200 \
ES_PASS=espass \
CH_USER=cloudhubuser \
CH_PASSWORD=cloudhubpassword \
CH_ENV=Production \
bin/logstash -f ../elastic-cloudhub-observability/logstash/get_cloudhub_app_logs.conf -r -w 1
```
