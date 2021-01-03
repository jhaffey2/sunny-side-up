# sunny-side-up
Custom Sunrise Alarm with Phillips Hue Bridge &amp; Lights

## Sensors

https://developers.meethue.com/develop/hue-api/5-sensors-api/

```
{
	"19": {
		"state": {
			"flag": false,
			"lastupdated": "none"
		},
		"config": {
			"on": true,
			"reachable": true
		},
		"name": "Joe Custom Alarm",
		"type": "CLIPGenericFlag",
		"modelid": "JoeCustomFlag",
		"manufacturername": "homebridge-hue-joe",
		"swversion": "1.0",
		"uniqueid": "ede07661-476a-42c1-8241-de4e556c8808",
		"recycle": false
	}
}
```

## Schedules

https://developers.meethue.com/develop/hue-api/3-schedules-api/

Record:

```
{
	"3": {
		"name": "Custom Scheduled Sunrise Alarm",
		"description": "Custom Sunrise Alarm",
		"command": {
			"address": "/api/{username}/sensors/{id}/state",
			"body": {
				"flag": true
			},
			"method": "PUT"
		},
		"localtime": "W124/T06:20:00",
		"time": "W124/T14:20:00",
		"created": "2021-01-03T18:13:10",
		"status": "enabled",
		"recycle": false
	}
}
```

## Scenes

https://developers.meethue.com/develop/hue-api/4-scenes/

```
{
	"fkzrMYtIoU78-xY": {
		"name": "First Light 1",
		"type": "LightScene",
		"lights": [
			"1"
		],
		"owner": {username},
		"recycle": false,
		"locked": false,
		"appdata": {},
		"picture": "",
		"lastupdated": "2021-01-03T01:42:10",
		"version": 2,
		"lightstates": {
			"1": {
				"on": true,
				"bri": 1,
				"xy": [
					0.6817,
					0.302
				]
			}
		}
	},
	"cdhg9MqLFNe8xCJ": {
		"name": "First Light 2",
		"type": "LightScene",
		"lights": [
			"1"
		],
		"owner": {username},
		"recycle": false,
		"locked": false,
		"appdata": {},
		"picture": "",
		"lastupdated": "2021-01-03T02:45:55",
		"version": 2,
		"lightstates": {
			"1": {
				"on": true,
				"bri": 13,
				"xy": [
					0.6802,
					0.3097
				],
				"transitiontime": 600
			}
		}
	},
	"AJ1ajjOer5ZwYLF": {
		"name": "First Light 3",
		"type": "LightScene",
		"lights": [
			"1"
		],
		"owner": {username},
		"recycle": false,
		"locked": false,
		"appdata": {},
		"picture": "",
		"lastupdated": "2021-01-03T02:56:34",
		"version": 2,
		"lightstates": {
			"1": {
				"on": true,
				"bri": 15,
				"xy": [
					0.6298,
					0.3578
				],
				"transitiontime": 600
			}
		}
	},
	"7w1TZjLwVCQmF-Y": {
		"name": "First Light 4",
		"type": "LightScene",
		"lights": [
			"1"
		],
		"owner": {username},
		"recycle": false,
		"locked": false,
		"appdata": {},
		"picture": "",
		"lastupdated": "2021-01-03T02:57:40",
		"version": 2,
		"lightstates": {
			"1": {
				"on": true,
				"bri": 15,
				"xy": [
					0.5756,
					0.3953
				],
				"transitiontime": 600
			}
		}
	},
	"zGaOCIPSyVmKZjW": {
		"name": "First Light 5",
		"type": "LightScene",
		"lights": [
			"1"
		],
		"owner": {username},
		"recycle": false,
		"locked": false,
		"appdata": {},
		"picture": "",
		"lastupdated": "2021-01-03T02:58:38",
		"version": 2,
		"lightstates": {
			"1": {
				"on": true,
				"bri": 51,
				"xy": [
					0.5756,
					0.3953
				],
				"transitiontime": 600
			}
		}
	},
	"ytPVLceTwljNqNC": {
		"name": "First Light 6",
		"type": "LightScene",
		"lights": [
			"1"
		],
		"owner": {username},
		"recycle": false,
		"locked": false,
		"appdata": {},
		"picture": "",
		"lastupdated": "2021-01-03T03:00:02",
		"version": 2,
		"lightstates": {
			"1": {
				"on": true,
				"bri": 25,
				"xy": [
					0.5005,
					0.4188
				],
				"transitiontime": 600
			}
		}
	},
	"czcRgwIqKY0nhSa": {
		"name": "First Light End",
		"type": "LightScene",
		"lights": [
			"1"
		],
		"owner": {username},
		"recycle": false,
		"locked": false,
		"appdata": {},
		"picture": "",
		"lastupdated": "2021-01-03T03:28:46",
		"version": 2,
		"lightstates": {
			"1": {
				"on": true,
				"bri": 50,
				"xy": [
					0.5003,
					0.4187
				],
				"transitiontime": 4200
			}
		}
	}
}
```

## Rules

https://developers.meethue.com/develop/hue-api/6-rules-api/

```
{
	"2": {
		"name": "Sunrise1-1.start",
		"owner": {username},
		"created": "2021-01-03T17:39:46",
		"lasttriggered": "none",
		"timestriggered": 0,
		"status": "enabled",
		"recycle": false,
		"conditions": [{
				"address": "/sensors/{id}/state/flag",
				"operator": "eq",
				"value": "true"
			},
			{
				"address": "/sensors/{id}/state/flag",
				"operator": "ddx",
				"value": "PT00:00:01"
			}
		],
		"actions": [{
			"address": "/groups/{id}/action",
			"method": "PUT",
			"body": {
				"scene": "fkzrMYtIoU78-xY"
			}
		}]
	},
	"1": {
		"name": "Sunrise1-2.start",
		"owner": {username},
		"created": "2021-01-03T17:46:22",
		"lasttriggered": "none",
		"timestriggered": 0,
		"status": "enabled",
		"recycle": false,
		"conditions": [{
				"address": "/sensors/{id}/state/flag",
				"operator": "eq",
				"value": "true"
			},
			{
				"address": "/sensors/{id}/state/flag",
				"operator": "ddx",
				"value": "PT00:01:00"
			}
		],
		"actions": [{
			"address": "/groups/{id}/action",
			"method": "PUT",
			"body": {
				"scene": "cdhg9MqLFNe8xCJ"
			}
		}]
	},
	"4": {
		"name": "Sunrise1-3.start",
		"owner": {username},
		"created": "2021-01-03T17:46:44",
		"lasttriggered": "none",
		"timestriggered": 0,
		"status": "enabled",
		"recycle": false,
		"conditions": [{
				"address": "/sensors/{id}/state/flag",
				"operator": "eq",
				"value": "true"
			},
			{
				"address": "/sensors/{id}/state/flag",
				"operator": "ddx",
				"value": "PT00:02:00"
			}
		],
		"actions": [{
			"address": "/groups/{id}/action",
			"method": "PUT",
			"body": {
				"scene": "AJ1ajjOer5ZwYLF"
			}
		}]
	},
	"5": {
		"name": "Sunrise1-4.start",
		"owner": {username},
		"created": "2021-01-03T17:47:54",
		"lasttriggered": "none",
		"timestriggered": 0,
		"status": "enabled",
		"recycle": false,
		"conditions": [{
				"address": "/sensors/{id}/state/flag",
				"operator": "eq",
				"value": "true"
			},
			{
				"address": "/sensors/{id}/state/flag",
				"operator": "ddx",
				"value": "PT00:03:00"
			}
		],
		"actions": [{
			"address": "/groups/{id}/action",
			"method": "PUT",
			"body": {
				"scene": "7w1TZjLwVCQmF-Y"
			}
		}]
	},
	"6": {
		"name": "Sunrise1-5.start",
		"owner": {username},
		"created": "2021-01-03T17:48:19",
		"lasttriggered": "none",
		"timestriggered": 0,
		"status": "enabled",
		"recycle": false,
		"conditions": [{
				"address": "/sensors/{id}/state/flag",
				"operator": "eq",
				"value": "true"
			},
			{
				"address": "/sensors/{id}/state/flag",
				"operator": "ddx",
				"value": "PT00:04:00"
			}
		],
		"actions": [{
			"address": "/groups/{id}/action",
			"method": "PUT",
			"body": {
				"scene": "zGaOCIPSyVmKZjW"
			}
		}]
	},
	"7": {
		"name": "Sunrise1-6.start",
		"owner": {username},
		"created": "2021-01-03T17:48:49",
		"lasttriggered": "none",
		"timestriggered": 0,
		"status": "enabled",
		"recycle": false,
		"conditions": [{
				"address": "/sensors/{id}/state/flag",
				"operator": "eq",
				"value": "true"
			},
			{
				"address": "/sensors/{id}/state/flag",
				"operator": "ddx",
				"value": "PT00:05:00"
			}
		],
		"actions": [{
			"address": "/groups/{id}/action",
			"method": "PUT",
			"body": {
				"scene": "ytPVLceTwljNqNC"
			}
		}]
	},
	"8": {
		"name": "Sunrise1-7.start",
		"owner": {username},
		"created": "2021-01-03T17:49:55",
		"lasttriggered": "none",
		"timestriggered": 0,
		"status": "enabled",
		"recycle": false,
		"conditions": [{
				"address": "/sensors/{id}/state/flag",
				"operator": "eq",
				"value": "true"
			},
			{
				"address": "/sensors/{id}/state/flag",
				"operator": "ddx",
				"value": "PT00:06:00"
			}
		],
		"actions": [{
				"address": "/groups/{id}/action",
				"method": "PUT",
				"body": {
					"scene": "czcRgwIqKY0nhSa"
				}
			},
			{
				"address": "/sensors/{id}/state",
				"method": "PUT",
				"body": {
					"flag": false
				}
			}
		]
	}
}
```
