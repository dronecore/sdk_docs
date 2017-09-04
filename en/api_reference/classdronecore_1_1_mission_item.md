# dronecore::MissionItem Class Reference
`#include: mission_item.h`

----


A mission is a vector of [MissionItem](classdronecore_1_1_mission_item.md)s. 


Each [MissionItem](classdronecore_1_1_mission_item.md) can contain a position and/or actions. [Mission](classdronecore_1_1_mission.md) items are just building blocks to assemble a mission, which can be sent to (or received from) a device. They cannot be used independently. 


## Public Types


Type | Description
--- | ---
enum [CameraAction](#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887a) {<ul><li style="list-style-type: none;"><a href="#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aa4130de26d3895fa5de9f46ddd558315c">TAKE_PHOTO</a>, <a href="#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aa27eb71e5403792ee9072932ec93c113c">START_PHOTO_INTERVAL</a>, <a href="#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aa7554aaea445f14cf06a0757ff8204b0a">STOP_PHOTO_INTERVAL</a>, <a href="#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aa2830bdcebb2b8bb17e19bef72a7255bc">START_VIDEO</a>, <a href="#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aac7dbedd5fead832bc23d7caaf4cfb8cf">STOP_VIDEO</a>, <a href="#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aab50339a10e1de285ac99d4c3990b8693">NONE</a><p>}</p></li> | Possible camera actions at a mission item.

## Public Member Functions


Type | Name | Description
---: | --- | ---
| [MissionItem](#classdronecore_1_1_mission_item_1aca4d7fd82ae0f623cd162730140a5a68) () | Constructor (internal use only).
| [~MissionItem](#classdronecore_1_1_mission_item_1abfcfaeb576e969d6da33a4d16013dd9f) () | Destructor (internal use only).
| [MissionItem](#classdronecore_1_1_mission_item_1ac6e6d75b38193db07eaa05b21fc229e2) (const MissionItem &)=delete | Copy constructor (object is not copyable).
void | [set_position](#classdronecore_1_1_mission_item_1ab5897670c8830fc3514036d6ee99b582) (double latitude_deg, double longitude_deg) | Set the position of a mission item.
void | [set_relative_altitude](#classdronecore_1_1_mission_item_1afef21f3028edad2ba2a0e966404fa33a) (float altitude_m) | Set the relative altitude of a mission item.
void | [set_fly_through](#classdronecore_1_1_mission_item_1a63d73896635dc0af136a521cd35bf352) (bool fly_through) | Set the fly-through property of a mission item.
void | [set_speed](#classdronecore_1_1_mission_item_1a37e43f748da4136c659419a4a2d84b0e) (float speed_m_s) | Set the speed to use after a mission item.
void | [set_gimbal_pitch_and_yaw](#classdronecore_1_1_mission_item_1a10adfcff1e99ae937654786b767e5558) (float pitch_deg, float yaw_deg) | Set the pitch and yaw angle of a gimbal at that mission item.
void | [set_camera_action](#classdronecore_1_1_mission_item_1a8d0d8a5519783aaa272befd73e851896) (CameraAction action) | Set the camera action for a mission item.
void | [set_camera_photo_interval](#classdronecore_1_1_mission_item_1a4ffe698b47c659aa8857725e94ad1f7c) (double interval_s) | Set the camera photo interval.
double | [get_latitude_deg](#classdronecore_1_1_mission_item_1abab46b936c93875f94069bc8a641aa29) () const | Get the latitude of a mission item.
double | [get_longitude_deg](#classdronecore_1_1_mission_item_1a290be3e40aa144ce5434274b631fe721) () const | Get the longitude of a mission item.
float | [get_relative_altitude_m](#classdronecore_1_1_mission_item_1aee64aee39efe672b85dd3e3425b6622b) () const | Get the relative altitude of a mission item.
bool | [get_fly_through](#classdronecore_1_1_mission_item_1a2ce89316fd776cab889339e5174619fc) () const | Get the fly-through property of a mission item.
float | [get_speed_m_s](#classdronecore_1_1_mission_item_1ae21003aa71d28f0a850408331ce318dc) () const | Get the speed to be used after this mission item.
[CameraAction](classdronecore_1_1_mission_item.md#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887a) | [get_camera_action](#classdronecore_1_1_mission_item_1a528773d14ee320ea6d65566b4cba1da4) () const | Get the camera action set for this mission item.
double | [get_camera_photo_interval_s](#classdronecore_1_1_mission_item_1afc11acac29356a4d3412dac99359b04a) () const | Get the camera photo interval that was set for this mission item.
const [MissionItem](classdronecore_1_1_mission_item.md) & | [operator=](#classdronecore_1_1_mission_item_1a8582ad72a3a8c20c87e8224ab10970c0) (const MissionItem &)=delete | Equality operator (object is not copyable).


## Constructor & Destructor Documentation


### MissionItem() {#classdronecore_1_1_mission_item_1aca4d7fd82ae0f623cd162730140a5a68}
```cpp
dronecore::MissionItem::MissionItem()
```


Constructor (internal use only).


<!-- inbodydescription:  --> 
<!-- return_type:  -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### ~MissionItem() {#classdronecore_1_1_mission_item_1abfcfaeb576e969d6da33a4d16013dd9f}
```cpp
dronecore::MissionItem::~MissionItem()
```


Destructor (internal use only).


<!-- inbodydescription:  --> 
<!-- return_type:  -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### MissionItem() {#classdronecore_1_1_mission_item_1ac6e6d75b38193db07eaa05b21fc229e2}
```cpp
dronecore::MissionItem::MissionItem(const MissionItem &)=delete
```


Copy constructor (object is not copyable).


**Parameters**

* const [MissionItem](classdronecore_1_1_mission_item.md) & **** - 

<!-- inbodydescription:  --> 
<!-- return_type:  -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


## Member Enumeration Documentation


### enum CameraAction {#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887a}


Possible camera actions at a mission item.


 Value | Description
--- | ---
<span id="classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aa4130de26d3895fa5de9f46ddd558315c"></span> `TAKE_PHOTO` | Take single photo. 
<span id="classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aa27eb71e5403792ee9072932ec93c113c"></span> `START_PHOTO_INTERVAL` | Start capturing photos at regular intervals - see [set_camera_photo_interval()](classdronecore_1_1_mission_item.md#classdronecore_1_1_mission_item_1a4ffe698b47c659aa8857725e94ad1f7c). 
<span id="classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aa7554aaea445f14cf06a0757ff8204b0a"></span> `STOP_PHOTO_INTERVAL` | Stop capturing photos at regular intervals. 
<span id="classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aa2830bdcebb2b8bb17e19bef72a7255bc"></span> `START_VIDEO` | Start capturing video. 
<span id="classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aac7dbedd5fead832bc23d7caaf4cfb8cf"></span> `STOP_VIDEO` | Stop capturing video. 
<span id="classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aab50339a10e1de285ac99d4c3990b8693"></span> `NONE` | No action. 

<!-- inbodydescription:  --> 
<!-- prot: public -->
<!-- static: no -->

## Member Function Documentation


### set_position() {#classdronecore_1_1_mission_item_1ab5897670c8830fc3514036d6ee99b582}
```cpp
void dronecore::MissionItem::set_position(double latitude_deg, double longitude_deg)
```


Set the position of a mission item.


**Parameters**

* double **latitude_deg** - Latitude of the waypoint in degrees.
* double **longitude_deg** - Longitude of the waypoint in degrees.

<!-- inbodydescription:  --> 
<!-- return_type: void -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### set_relative_altitude() {#classdronecore_1_1_mission_item_1afef21f3028edad2ba2a0e966404fa33a}
```cpp
void dronecore::MissionItem::set_relative_altitude(float altitude_m)
```


Set the relative altitude of a mission item.


**Parameters**

* float **altitude_m** - Altitude relative to takeoff position in metres.

<!-- inbodydescription:  --> 
<!-- return_type: void -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### set_fly_through() {#classdronecore_1_1_mission_item_1a63d73896635dc0af136a521cd35bf352}
```cpp
void dronecore::MissionItem::set_fly_through(bool fly_through)
```


Set the fly-through property of a mission item.


**Parameters**

* bool **fly_through** - If true the drone will fly through the waypoint without stopping. If false the drone will come to a stop at the waypoint before continuing.

<!-- inbodydescription:  --> 
<!-- return_type: void -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### set_speed() {#classdronecore_1_1_mission_item_1a37e43f748da4136c659419a4a2d84b0e}
```cpp
void dronecore::MissionItem::set_speed(float speed_m_s)
```


Set the speed to use after a mission item.


**Parameters**

* float **speed_m_s** - Speed to use after this mission item in metres/second.

<!-- inbodydescription:  --> 
<!-- return_type: void -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### set_gimbal_pitch_and_yaw() {#classdronecore_1_1_mission_item_1a10adfcff1e99ae937654786b767e5558}
```cpp
void dronecore::MissionItem::set_gimbal_pitch_and_yaw(float pitch_deg, float yaw_deg)
```


Set the pitch and yaw angle of a gimbal at that mission item.


**Parameters**

* float **pitch_deg** - The new pitch angle of the gimbal in degrees (0: horizontal, positive up, -90: vertical downward facing).
* float **yaw_deg** - The new yaw angle of the gimbal in degrees (0: forward, positive clock-wise, 90: to the right).

<!-- inbodydescription:  --> 
<!-- return_type: void -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### set_camera_action() {#classdronecore_1_1_mission_item_1a8d0d8a5519783aaa272befd73e851896}
```cpp
void dronecore::MissionItem::set_camera_action(CameraAction action)
```


Set the camera action for a mission item.


**Parameters**

* [CameraAction](classdronecore_1_1_mission_item.md#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887a) **action** - The camera action.

<!-- inbodydescription:  --> 
<!-- return_type: void -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### set_camera_photo_interval() {#classdronecore_1_1_mission_item_1a4ffe698b47c659aa8857725e94ad1f7c}
```cpp
void dronecore::MissionItem::set_camera_photo_interval(double interval_s)
```


Set the camera photo interval.

This only has an effect if used together with [CameraAction::START_PHOTO_INTERVAL](classdronecore_1_1_mission_item.md#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aa27eb71e5403792ee9072932ec93c113c).

**Parameters**

* double **interval_s** - Interval between photo captures in seconds.

<!-- inbodydescription:  --> 
<!-- return_type: void -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### get_latitude_deg() {#classdronecore_1_1_mission_item_1abab46b936c93875f94069bc8a641aa29}
```cpp
double dronecore::MissionItem::get_latitude_deg() const
```


Get the latitude of a mission item.


**Returns**

&emsp;double - Latitude in degrees.

<!-- inbodydescription:  --> 
<!-- return_type: double -->
<!-- return_type_comment: Latitude in degrees. -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: yes -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### get_longitude_deg() {#classdronecore_1_1_mission_item_1a290be3e40aa144ce5434274b631fe721}
```cpp
double dronecore::MissionItem::get_longitude_deg() const
```


Get the longitude of a mission item.


**Returns**

&emsp;double - Longitude in degrees.

<!-- inbodydescription:  --> 
<!-- return_type: double -->
<!-- return_type_comment: Longitude in degrees. -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: yes -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### get_relative_altitude_m() {#classdronecore_1_1_mission_item_1aee64aee39efe672b85dd3e3425b6622b}
```cpp
float dronecore::MissionItem::get_relative_altitude_m() const
```


Get the relative altitude of a mission item.


**Returns**

&emsp;float - The altitude relative to the takeoff position in metres.

<!-- inbodydescription:  --> 
<!-- return_type: float -->
<!-- return_type_comment: The altitude relative to the takeoff position in metres. -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: yes -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### get_fly_through() {#classdronecore_1_1_mission_item_1a2ce89316fd776cab889339e5174619fc}
```cpp
bool dronecore::MissionItem::get_fly_through() const
```


Get the fly-through property of a mission item.


**Returns**

&emsp;bool - true if the drone will fly through the waypoint without stopping. false if the drone will come to a stop at the waypoint before continuing.

<!-- inbodydescription:  --> 
<!-- return_type: bool -->
<!-- return_type_comment: true if the drone will fly through the waypoint without stopping. false if the drone will come to a stop at the waypoint before continuing. -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: yes -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### get_speed_m_s() {#classdronecore_1_1_mission_item_1ae21003aa71d28f0a850408331ce318dc}
```cpp
float dronecore::MissionItem::get_speed_m_s() const
```


Get the speed to be used after this mission item.


**Returns**

&emsp;float - Speed in metres/second.

<!-- inbodydescription:  --> 
<!-- return_type: float -->
<!-- return_type_comment: Speed in metres/second. -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: yes -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### get_camera_action() {#classdronecore_1_1_mission_item_1a528773d14ee320ea6d65566b4cba1da4}
```cpp
MissionItem::CameraAction dronecore::MissionItem::get_camera_action() const
```


Get the camera action set for this mission item.


**Returns**

&emsp;[CameraAction](classdronecore_1_1_mission_item.md#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887a) - Camera action enum value.

<!-- inbodydescription:  --> 
<!-- return_type: [CameraAction](classdronecore_1_1_mission_item.md#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887a) -->
<!-- return_type_comment: Camera action enum value. -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: yes -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### get_camera_photo_interval_s() {#classdronecore_1_1_mission_item_1afc11acac29356a4d3412dac99359b04a}
```cpp
double dronecore::MissionItem::get_camera_photo_interval_s() const
```


Get the camera photo interval that was set for this mission item.

This only has an effect if used together with [CameraAction::START_PHOTO_INTERVAL](classdronecore_1_1_mission_item.md#classdronecore_1_1_mission_item_1a0cdd25121e5ed6930080ac022857887aa27eb71e5403792ee9072932ec93c113c).

**Returns**

&emsp;double - Camera photo interval in seconds.

<!-- inbodydescription:  --> 
<!-- return_type: double -->
<!-- return_type_comment: Camera photo interval in seconds. -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: yes -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### operator=() {#classdronecore_1_1_mission_item_1a8582ad72a3a8c20c87e8224ab10970c0}
```cpp
const MissionItem& dronecore::MissionItem::operator=(const MissionItem &)=delete
```


Equality operator (object is not copyable).


**Parameters**

* const [MissionItem](classdronecore_1_1_mission_item.md) & **** - 

**Returns**

&emsp;const [MissionItem](classdronecore_1_1_mission_item.md) & - 

<!-- inbodydescription:  --> 
<!-- return_type: const [MissionItem](classdronecore_1_1_mission_item.md) & -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->