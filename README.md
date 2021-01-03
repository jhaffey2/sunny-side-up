# sunny-side-up
Custom Sunrise Alarm with Phillips Hue Bridge &amp; Lights

## Sensors

https://developers.meethue.com/develop/hue-api/5-sensors-api/

```
{
	"16": {
		"state": {
			"flag": false,
			"lastupdated": "2021-01-03T03:29:32"
		},
		"config": {
			"on": true,
			"reachable": true
		},
		"name": "Sunrise Custom Alarm",
		"type": "CLIPGenericFlag",
		"modelid": "PHA_CTRL_START",
		"manufacturername": "Philips",
		"swversion": "1.0",
		"uniqueid": "uO7pMuNmt9UG",
		"recycle": true
	}
}
```

## Schedules

https://developers.meethue.com/develop/hue-api/3-schedules-api/

Record:

```
{
	"1": {
		"name": "Sunrise Custom Alarm",
		"description": "My programmed sunrise alarm",
		"command": {
			"address": "/api/{username}/sensors/{id}/state",
			"body": {
				"flag": true
			},
			"method": "PUT"
		},
		"localtime": "W124/T06:20:00",
		"time": "W124/T14:20:00",
		"created": "2021-01-02T18:10:12",
		"status": "enabled",
		"recycle": true
	}
}
```

## Scenes

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
