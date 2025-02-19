### Systemd syslog in Opensearch

```json
{
    "_index": "otlp-logs",
    "_id": "59tEF5UB9hHr9R1SnTBi",
    "_version": 1,
    "_score": null,
    "_source": {
      "traceId": "",
      "spanId": "",
      "droppedAttributesCount": 0,
      "serviceName": null,
      "schemaUrl": "https://opentelemetry.io/schemas/1.6.1",
      
      "flags": 0,
      "severityNumber": 9,
      "severityText": "info",
      
      "time": "2025-02-18T04:15:18Z",
      "observedTime": "2025-02-18T04:15:18.312545735Z",
      
      "body": "<30>Feb 18 04:15:18 ip-10-0-0-173 systemd[1]: Starting System Logging Service...",
      // dataprepper processor - grok
      "priority": "30",
      "syslog_timestamp": "Feb 18 04:15:18",
      "hostname": "ip-10-0-0-173",
      "program": "systemd",
      "pid": "1",
      "message": "Starting System Logging Service...",
      
      // otelcol processor - resource.attributes
      "resource.attributes.site@id": 1,
      "resource.attributes.site@name": "Amir Punya Outlet",
      "resource.attributes.state": "Hulu Langat",
      "resource.attributes.region": "Selangor",
      "resource.attributes.position": "POINT (-110.8752204 32.1891602)",
      "resource.attributes.district": "Bandar Baru Bangi",

      // otelcol processor - resourcedetection.system
      "resource.attributes.os@type": "linux",
      "resource.attributes.os@description": "Linux 58da95d16983 6.8.0-1021-aws #23~22.04.1-Ubuntu SMP Tue Dec 10 16:50:46 UTC 2024 x86_64",
      "resource.attributes.host@name": "58da95d16983",
      "resource.attributes.host@arch": "amd64",
      "resource.attributes.host@mac": "[\"02-42-AC-1A-00-02\"]",
      "resource.attributes.host@ip": "[\"172.26.0.2\"]",
      "resource.attributes.host@cpu@vendor@id": "GenuineIntel",
      "resource.attributes.host@cpu@stepping": "7",
      "resource.attributes.host@cpu@cache@l2@size": 36608,
      "resource.attributes.host@cpu@family": "6",
      "resource.attributes.host@cpu@model@id": "85",
      "resource.attributes.host@cpu@model@name": "Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz",
      
      // otelcol processor - attributes
      "log.attributes.environment": "staging",

      // otelcol receiver - syslog
      "log.attributes.priority": 30,
      "log.attributes.facility": 3,
      "log.attributes.message": "Starting System Logging Service...",
      "log.attributes.appname": "systemd",
      "log.attributes.hostname": "ip-10-0-0-173",
      "log.attributes.proc_id": "1",
      "log.attributes.net@host@name": "58da95d16983",
      "log.attributes.net@peer@ip": "54.255.39.222",
      "log.attributes.net@transport": "IP.TCP",
      "log.attributes.net@host@port": "514",
      "log.attributes.net@host@ip": "172.26.0.2",
      "log.attributes.net@peer@name": "ec2-54-255-39-222.ap-southeast-1.compute.amazonaws.com",
      "log.attributes.net@peer@port": "45778"
    },
    "fields": {
      "time": [
        "2025-02-18T04:15:18.000Z"
      ],
      "observedTime": [
        "2025-02-18T04:15:18.312Z"
      ]
    },
    "highlight": {
      "log.attributes.appname.keyword": [
        "@opensearch-dashboards-highlighted-field@systemd@/opensearch-dashboards-highlighted-field@"
      ]
    },
    "sort": [
      1739852118312
    ]
  }
```