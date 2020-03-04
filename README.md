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
## kibana start stop
```
sudo -i service kibana start
sudo -i service kibana stop
```
## put query
```
PUT /{index}/{type}/{id}
{
    "field1":"value1",
    "field2":"value2"
}
PUT /vehicles/car/123
{
  "make":"honda",
  "Color":"black",
  "price":"1901.45"
}
```
## get query retrive document
```
GET /vehicles/car/123
```
## get only data
```
GET /vehicles/car/123/_source
```
## document exist
```
HEAD /vehicles/car/123
```
## post update
```
POST /vehicles/car/123/_update
{
  "doc":{
    "price":"1000.20"
  }
}
```
## Delete document
```
DELETE /vehicles/car/123
```
## get structure
```
GET /vehicles
DELETE /vehicles
```