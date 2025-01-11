to access and controol influx db from its originated dashboard you can use this url:


ip(srvr):port(influx)
ip:8086

structure of the influx db line protocol:

<measurement>,<tag_key>=<tag_value> <field_key>=<field_value> <timestamp>

sample of data filing via pythoon:

```python
from influxdb_client import InfluxDBClient, Point, WritePrecision
from influxdb_client.client.write_api import SYNCHRONOUS

client = InfluxDBClient(url="http://localhost:8086", token="your-token", org="your-org")
write_api = client.write_api(write_options=SYNCHRONOUS)

point = Point("system_metrics") \
    .tag("host", "server1") \
    .tag("region", "us-west") \
    .field("cpu_usage", 75.4) \
    .field("memory_usage", 2048) \
    .time(datetime.utcnow(), WritePrecision.NS)

write_api.write(bucket="your-bucket", record=point)
```
