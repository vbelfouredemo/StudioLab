# Models

Create stand alone `json` files for the following models:


### User
 
```json json_schema
{
  "title": "User",
  "type": "object",
  "x-tags": [
    "IOT"
  ],
  "description": "Users associated with a CloudHome account. Administrative priviledges are indicated to show which users can configure device management and which users can only interact with configured devices.",
  "properties": {
    "userID": {
      "type": "string"
    },
    "userName": {
      "type": "string"
    },
    "email": {
      "type": "string",
      "format": "email"
    }
  },
  "required": [
    "userID",
    "userName",
    "email"
  ]
}
```

### Account

```json json_schema
{
  "title": "Account",
  "type": "object",
  "description": "Users can belong to multiple accounts on CloudHome's federated services. In other words users have a unique id that can interact or manage devices on more than one account or location.",
  "x-tags": [
    "IOT"
  ],
  "properties": {
    "accountID": {
      "type": "string"
    },
    "accountName": {
      "type": "string"
    },
    "userCount": {
      "type": "integer",
      "format": "int64",
      "minimum": 1
    },
    "deviceCount": {
      "type": "integer",
      "format": "int64",
      "minimum": 1
    }
  },
  "required": [
    "accountID"
  ]
}
```

### Location

```json json_schema
{
  "title": "Location",
  "type": "object",
  "description": "Device geolocation at most recent update. Users can optionally choose to turn off geolocation, however key features such as mapping will not be available.",
  "x-tags": [
    "IOT",
    "devices"
  ],
  "properties": {
    "lat": {
      "type": "number",
      "format": "float",
      "minimum": 4,
      "maximum": 7,
      "description": "decimal degrees"
    },
    "long": {
      "type": "number",
      "format": "float",
      "minimum": 4,
      "maximum": 7,
      "description": "decimal degrees"
    },
    "geoTracking": {
      "type": "boolean",
      "description": "real time tracking enabled?\n"
    }
  },
  "required": [
    "geoTracking"
  ]
}
```