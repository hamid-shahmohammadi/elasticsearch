# elasticsearch
## install elasticsearch
```
wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.6.0-amd64.deb
wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.6.0-amd64.deb.sha512
shasum -a 512 -c elasticsearch-7.6.0-amd64.deb.sha512 
sudo dpkg -i elasticsearch-7.6.0-amd64.deb
```

## start and stop service
```
sudo -i service elasticsearch start
sudo -i service elasticsearch stop
```
## test elasticsearch
```
curl -X GET "localhost:9200"
```