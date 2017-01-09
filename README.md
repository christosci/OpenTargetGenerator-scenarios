# OpenTargetGenerator-scenarios
Scenarios for OpenTargetGenerator

## Format
The root element `<scenario>` must include a `magvar` attribute indicating the magnetic variation. For example `magvar="-11.2"` represents a magnetic variation of 11.2 degrees east.

Below you will find the description of attributes for the subelements of (`<navaids>`, `<runways>`, and `<aircraft>`). Each element can contain an unlimited amount of subelements (`<wp/>`, `<rwy/>`, and `<ac/>` respectively).

#### `<navaids>`

| Attribute     | Optional      | Description                                    |
| ------------- |:-------------:|:-----------------------------------------------|
| name          | No            | Name of waypoint, must be typed all uppercase. |
| lat & lon     | No            | Latitude and longitude in decimal format.      |
| alt           | Yes           | Crossing altitude for the waypoint.            |

#### `<runways>`

| Attribute     | Description                                                             |
| ------------- |:------------------------------------------------------------------------|
| id            | Runway identifier; letters must be typed uppercase.                     |
| lat & lon     | Latitude and longitude of the touchdown zone in decimal format.         |
| crs           | Final approach course (magnetic) in degrees (0-360), no decimal numbers.|
| elev          | Touchdown zone elevation in feet.                                       |

#### `<aircraft>`

| Attribute     | Description                                                                |
| ------------- |:---------------------------------------------------------------------------|
| callsign      | Aircraft callsign; letters must be typed uppercase.                        |
| sq            | Squawk code; digits 0-7 only and unique for each aircraft.                 |
| lat & lon     | Latitude and longitude of the starting point in decimal format.            |
| alt           | Starting altitude.                                                         |
| spd           | Starting speed.                                                            |
| type          | Aircraft type.                                                             |
| route         | Can only include waypoints already defined in navaids, separated by spaces.|
