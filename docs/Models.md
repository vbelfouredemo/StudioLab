# Models

Create stand alone `json` files for the following models:


### User
**Description**: *Users associated with a CloudHome account. Administrative priviledges are indicated to show which users can configure device management and which users can only interact with configured devices.*
 
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
      "type": "string"
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
**Description**: *Users can belong to multiple accounts on CloudHome's federated services. In other words users have a unique id that can interact or manage devices on more than one account or location.*

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
      "type": "integer"
    },
    "deviceCount": {
      "type": "integer"
    }
  },
  "required": [
    "accountID"
  ]
}
```

### Location
**Description**: *Device geolocation at most recent update. Users can optionally choose to turn off geolocation, however key features such as mapping will not be available.*

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
      "description": "decimal degrees"
    },
    "long": {
      "type": "number",
      "description": "decimal degrees"
    },
    "geoTracking": {
      "type": "boolean",
      "description": "real time tracking enabled?"
    }
  },
  "required": [
    "geoTracking"
  ]
}
```