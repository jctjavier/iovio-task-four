# iovio-task-four
##### status: *complete*

## Description:
* Run and configure demo instance
* Write a data point into influxdb 

## Additional Information:
* Used postman to write data point into the influxdb

## InfluxDB Information:
* InfluxDB: http://localhost:9999
* org: iovio
* bucket: tech
* precision: s (seconds)
* db: mydb

## Requirements
* mydb database has already been created in influxdb
* Authentication token is available

## Steps to write datapoint
1. Download postman collection
2. Ensure influx db is running and configured as described in "InfluxDB Information" (Please see above)
3. Load postman collection into Postman
4. Input authentication token in header key = 'Authorization'
5. Input data as a line in request body where data type is 'raw'. Example: 
```
cpu_load_short,direction=in,host=server01,region=us-west value=2.0 1422568543702900257
```
6. Run request
7. Response should return 200
