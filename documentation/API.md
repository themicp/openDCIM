## API Endpoints v1

All GET endpoints reply with a JSON object that contains at least 2 fields:
* `error`: **false** in case of no error, the error description otherwise
* `errorcode`: The HTTP status code sent from the endpoint

### `GET /api/v1/device`

**Description**: All devices for which the user's rights have access to view

**Returns**: 
```json
{}
```

### `GET /api/v1/device/:deviceid`

**Description**: Get information for the device with the specified id

**Returns**: 
```json
{}
```

### `GET /api/v1/device/bydatacenter/:datacenterid`

**Description**: All devices for which the user's rights have access to view, filtered by the datacenter id

**Returns**: 
```json
{}
```

### `GET /api/v1/device/byproject/:projectid`

**Description**: All devices for which the user's rights have access to view, filtered by the project id

**Returns**: 
```json
{}
```

### `GET /api/v1/device/:deviceid/getpicture`

**Description**: Get the HTML representation of a device

**Optional arguments**:
* `rear`: If set, it will return the rear picture of the device

**Returns**: 
```json
{}
```

### `GET /api/v1/device/:deviceid/getsensorreadings`

**Description**: Get readings from the device's sensors

**Returns**: 
```json
{}
```

### `GET /deviceport/:deviceid`

**Description**: Get all ports for specified device

**Returns**: 
```json
{}
```

### `GET /api/v1/deviceport/:deviceid/patchcandidates`

**Description**: All devices that this device can connect to

**Optional arguments**:
* `portnumber` (int): id of the port on the device you're connecting from. required when listports is true
* `connectto` (int): deviceid you want to connect to
* `listports` (true): will kick back ports that can be connected to instead of devices
* `patchpanels` (true): limit the result to just patch panel devices
* `limiter` (cabinet/row/zone/datacenter): limit the results by these containers
**Returns**: 
```json
{}
```

### `GET /api/v1/devicestatus`

**Description**: Get all the available device statuses

**Returns**: 
```json
{}
```

### `GET /api/v1/devicestatus/:statusid`

**Description**: Get information about a specific status code

**Returns**: 
```json
{}
```

### `GET /api/v1/devicetemplate`

**Description**: Get all available device templates

**Returns**: 
```json
{}
```

### `GET /api/v1/devicetemplate/:templateid`

**Description**: Get information about a specific template

**Returns**: 
```json
{}
```

### `GET /api/v1/devicetemplate/:templateid/dataport`

**Description**: Get data ports defined for device template with templateid

**Returns**: 
```json
{}
```

### `GET /api/v1/devicetemplate/:templateid/dataport/:portnumber`

**Description**: Get single data port defined for device template with templateid and portnumber

**Returns**: 
```json
{}
```

### `GET /api/v1/devicetemplate/:templateid/powerport`

**Description**: Get power ports defined for device template with templateid

**Returns**: 
```json
{}
```

### `GET /api/v1/devicetemplate/:templateid/slot`

**Description**: Get slots defined for device template with templateid

**Returns**: 
```json
{}
```

### `GET /api/v1/manufacturer`

**Description**: Get all manufacturers

**Returns**: 
```json
{}
```

### `GET /api/v1/zone`

**Description**: Get all zones for which the user's rights have access to view

**Returns**: 
```json
{}
```

### `GET /api/v1/zone/:zoneid`

**Description**: Get zone with zoneid

**Returns**: 
```json
{}
```

### `GET /api/v1/cabrow`

**Description**: Get all cabinet rows for which the user's rights have access to view

**Returns**: 
```json
{}
```

### `GET /api/v1/cabrow/:cabrowid/devices`

**Description**: Get all devices in the cabinet row

**Returns**: 
```json
{}
```

### `GET /api/v1/people`

**Description**: List of all users

**Returns**: 
```json
{}
```

### `GET /api/v1/department`

**Description**: List of all departments

**Returns**: 
```json
{}
```

### `GET /api/v1/datacenter`

**Description**: List of all data centers

**Returns**: 
```json
{}
```

### `GET /api/v1/datacenter/:id`

**Description**: Details of a specified datacenter

**Returns**: 
```json
{}
```

### `GET /api/v1/cabinet`

**Description**: List of all cabinets

**Returns**: 
```json
{}
```

### `GET /api/v1/cabinet/:cabinetid`

**Description**: Get all information on a specific cabinet

**Returns**: 
```json
{}
```

### `GET /api/v1/cabinet/:cabinetid/getpictures`

**Description**: Get HTML representation of a cabinet

**Returns**: 
```json
{}
```

### `GET /api/v1/cabinet/byproject/:projectid`

**Description**: List of all cabinets filtered by the project id

**Returns**: 
```json
{}
```

### `GET /api/v1/cabinet/bydc/:datacenterid`

**Description**:  Get all cabinet information belonging in a datacenter

**Returns**: 
```json
{}
```

### `GET /api/v1/cabinet/:cabinetid/sensors`

**Description**:  Get readings from various sensors of specific cabinet

**Returns**: 
```json
{}
```

### `GET /api/v1/cabinet/bydept/:deptid`

**Description**:  Get all cabinet information for cabinets in a specific department

**Returns**: 
```json
{}
```

### `GET /api/v1/disposition`

**Description**:  Get all disposition methods

**Returns**: 
```json
{}
```

### `GET /api/v1/disposition/:dispositionid`

**Description**:  Get information on specific disposition method, along with all devices disposed via this method

**Returns**: 
```json
{}
```

### `GET /api/v1/project`

**Description**:  List all projects

**Returns**: 
```json
{}
```


### `GET /api/v1/project/bycabinet/:cabinetid`

**Description**:  Get all project metadata for projects the cabinetid is a member of

**Returns**: 
```json
{}
```

### `GET /api/v1/project/bydevice/:deviceid`

**Description**:  Get all project metadata for projects the deviceid is a member of

**Returns**: 
```json
{}
```

### `GET /api/v1/powerport/:deviceid`

**Description**:  Get all power ports for a device or a specific port

**Returns**: 
```json
{}
```

### `GET /api/v1/colorcode`

**Description**:  List of all color codes

**Returns**: 
```json
{}
```

### `GET /api/v1/colorcode/:colorid`

**Description**:  Get information on a specific color code

**Returns**: 
```json
{}
```

### `GET /api/v1/colorcode/:colorid/timesused`

**Description**:  Get the number of objects using a specific color code

**Returns**: 
```json
{}
```
