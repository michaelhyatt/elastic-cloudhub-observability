## Logstash synchronisation of CloudHub data into Elasticsearch

### get_cloudhub_app_logs.conf
This config authenticates to CloudHub and performs synchronisation of all application logs for a particular environment.

Command to run:
```bash
CH_USER=cloudhubuser CH_PASSWORD=chuserpassword123 CH_ENV=Production bin/logstash -f get_cloudhub_app_logs.conf
```
