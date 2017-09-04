# dronecore::Mission Class Reference
`#include: mission.h`

----


The [Mission](classdronecore_1_1_mission.md) class enables waypoint missions. 


## Public Types


Type | Description
--- | ---
enum [Result](#classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cda) {<ul><li style="list-style-type: none;"><a href="#classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaad0749aaba8b833466dfcbb0428e4f89c">SUCCESS=0</a>, <a href="#classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaabb1ca97ec761fc37101737ba0aa2e7c5">ERROR</a>, <a href="#classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaab6968a2ae2835d0d36126e1d12e5d1a1">TOO_MANY_MISSION_ITEMS</a>, <a href="#classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaa802706a9238e2928077f97736854bad4">BUSY</a>, <a href="#classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaa070a0fb40f6c308ab544b227660aadff">TIMEOUT</a>, <a href="#classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaaf295a0c3e37c94f078e1c5476479132d">INVALID_ARGUMENT</a>, <a href="#classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaa696b031073e74bf2cb98e5ef201d4aa3">UNKNOWN</a><p>}</p></li> | Possible results returned for mission requests.
std::function< void([Result](classdronecore_1_1_mission.md#classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cda))> [result_callback_t](#classdronecore_1_1_mission_1a239f8d5853785d6ccf90c8c48b5ccf06) | Callback type for async mission calls.
std::function< void(int current, int total)> [progress_callback_t](#classdronecore_1_1_mission_1aeda7795cd898008afc05b779f99b704b) | Callback type to receive mission progress.

## Public Member Functions


Type | Name | Description
---: | --- | ---
| [Mission](#classdronecore_1_1_mission_1ae37622b5640ab3a5042b33c540b31db8) (MissionImpl *impl) | Constructor (internal use only).
| [~Mission](#classdronecore_1_1_mission_1a395b8c121630aa8a5dd3d48f95290659) () | Destructor (internal use only).
| [Mission](#classdronecore_1_1_mission_1a4947f79b7dd71e66bca64e5bbb0b3377) (const Mission &)=delete | Copy constructor (object is not copyable).
void | [send_mission_async](#classdronecore_1_1_mission_1ad06a0751e303eb5c1f1ba37d3b9ede47) (const std::vector< std::shared_ptr< MissionItem >> &mission_items, result_callback_t callback) | Sends a vector of mission items to the device (asynchronous).
void | [start_mission_async](#classdronecore_1_1_mission_1a9e032c6b2bc35cf6e7e19e07747fb0d3) (result_callback_t callback) | Starts the mission (asynchronous).
void | [pause_mission_async](#classdronecore_1_1_mission_1a65f729cf954586507ecd8dc07a510dd1) (result_callback_t callback) | Pauses the mission (asynchronous).
void | [set_current_mission_item_async](#classdronecore_1_1_mission_1af8d06941d424d57bcc2b55f8f9a2ea27) (int current, result_callback_t callback) | Sets the mission item index to go to (asynchronous).
bool | [mission_finished](#classdronecore_1_1_mission_1a63f73773d319ddac49f4c67f075368c6) () const | Checks if mission has been finished (synchronous).
int | [current_mission_item](#classdronecore_1_1_mission_1af757c3f1332f0c3bb6b592b94cb24384) () const | Returns the current mission item index (synchronous).
int | [total_mission_items](#classdronecore_1_1_mission_1a1edf6f07441c3f67053c875157af6342) () const | Returns the total number of mission items (synchronous).
void | [subscribe_progress](#classdronecore_1_1_mission_1a3290fc79eb22f899528328adfca48a61) (progress_callback_t callback) | Subscribes to mission progress (asynchronous).
const [Mission](classdronecore_1_1_mission.md) & | [operator=](#classdronecore_1_1_mission_1ae946abaf32a30cb0b803a145f095217d) (const Mission &)=delete | Equality operator (object is not copyable).
## Static Public Member Functions


Type | Name | Description
---: | --- | ---
const char * | [result_str](#classdronecore_1_1_mission_1ac2abe4b9f52e32900f84e5bf47d38fe2) (Result result) | Gets a human-readable English string for an [Mission::Result](classdronecore_1_1_mission.md#classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cda).


## Constructor & Destructor Documentation


### Mission() {#classdronecore_1_1_mission_1ae37622b5640ab3a5042b33c540b31db8}
```cpp
dronecore::Mission::Mission(MissionImpl *impl)
```


Constructor (internal use only).


**Parameters**

* [MissionImpl](classdronecore_1_1_mission_impl.md) * **impl** - 

<!-- inbodydescription:  --> 
<!-- return_type:  -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: yes -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### ~Mission() {#classdronecore_1_1_mission_1a395b8c121630aa8a5dd3d48f95290659}
```cpp
dronecore::Mission::~Mission()
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


### Mission() {#classdronecore_1_1_mission_1a4947f79b7dd71e66bca64e5bbb0b3377}
```cpp
dronecore::Mission::Mission(const Mission &)=delete
```


Copy constructor (object is not copyable).


**Parameters**

* const [Mission](classdronecore_1_1_mission.md) & **** - 

<!-- inbodydescription:  --> 
<!-- return_type:  -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->

## Member Typdef Documentation


### typedef result_callback_t {#classdronecore_1_1_mission_1a239f8d5853785d6ccf90c8c48b5ccf06}

```cpp
typedef std::function<void(Result)> dronecore::Mission::result_callback_t
```


Callback type for async mission calls.


### typedef progress_callback_t {#classdronecore_1_1_mission_1aeda7795cd898008afc05b779f99b704b}

```cpp
typedef std::function<void(int current, int total)> dronecore::Mission::progress_callback_t
```


Callback type to receive mission progress.

The mission is finished if current == total.

**Parameters**

* **current** - current mission item index (0 based)
* **total** - total number of mission items

## Member Enumeration Documentation


### enum Result {#classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cda}


Possible results returned for mission requests.


 Value | Description
--- | ---
<span id="classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaad0749aaba8b833466dfcbb0428e4f89c"></span> `SUCCESS` | Request succeeded. 
<span id="classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaabb1ca97ec761fc37101737ba0aa2e7c5"></span> `ERROR` | Error. 
<span id="classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaab6968a2ae2835d0d36126e1d12e5d1a1"></span> `TOO_MANY_MISSION_ITEMS` | Too many [MissionItem](classdronecore_1_1_mission_item.md) objects in the mission. 
<span id="classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaa802706a9238e2928077f97736854bad4"></span> `BUSY` | Vehicle busy. 
<span id="classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaa070a0fb40f6c308ab544b227660aadff"></span> `TIMEOUT` | Request timed out. 
<span id="classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaaf295a0c3e37c94f078e1c5476479132d"></span> `INVALID_ARGUMENT` | Invalid argument. 
<span id="classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cdaa696b031073e74bf2cb98e5ef201d4aa3"></span> `UNKNOWN` | Unknown error. 

<!-- inbodydescription:  --> 
<!-- prot: public -->
<!-- static: no -->

## Member Function Documentation


### send_mission_async() {#classdronecore_1_1_mission_1ad06a0751e303eb5c1f1ba37d3b9ede47}
```cpp
void dronecore::Mission::send_mission_async(const std::vector< std::shared_ptr< MissionItem >> &mission_items, result_callback_t callback)
```


Sends a vector of mission items to the device (asynchronous).

The mission items are uploaded to a drone. Once uploaded the mission can be started and executed even if a connection is lost.

**Parameters**

* const std::vector< std::shared_ptr< [MissionItem](classdronecore_1_1_mission_item.md) >> & **mission_items** - reference to vector of mission items.
* [result_callback_t](classdronecore_1_1_mission.md#classdronecore_1_1_mission_1a239f8d5853785d6ccf90c8c48b5ccf06) **callback** - callback to receive result of this request

<!-- inbodydescription:  --> 
<!-- return_type: void -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### start_mission_async() {#classdronecore_1_1_mission_1a9e032c6b2bc35cf6e7e19e07747fb0d3}
```cpp
void dronecore::Mission::start_mission_async(result_callback_t callback)
```


Starts the mission (asynchronous).

Note that the mission must be uplaoded to the vehicle using [send_mission_async()](classdronecore_1_1_mission.md#classdronecore_1_1_mission_1ad06a0751e303eb5c1f1ba37d3b9ede47) before this method is called.

**Parameters**

* [result_callback_t](classdronecore_1_1_mission.md#classdronecore_1_1_mission_1a239f8d5853785d6ccf90c8c48b5ccf06) **callback** - callback to receive result of this request

<!-- inbodydescription:  --> 
<!-- return_type: void -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### pause_mission_async() {#classdronecore_1_1_mission_1a65f729cf954586507ecd8dc07a510dd1}
```cpp
void dronecore::Mission::pause_mission_async(result_callback_t callback)
```


Pauses the mission (asynchronous).

Pausing the mission puts the vehicle into HOLD mode (See [https://docs.px4.io/en/flight_modes/hold.html](https://docs.px4.io/en/flight_modes/hold.html)). A multicopter should just hover at the spot while a fixedwing vehicle should loiter around the location where it paused.

**Parameters**

* [result_callback_t](classdronecore_1_1_mission.md#classdronecore_1_1_mission_1a239f8d5853785d6ccf90c8c48b5ccf06) **callback** - callback to receive result of this request

<!-- inbodydescription:  --> 
<!-- return_type: void -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### set_current_mission_item_async() {#classdronecore_1_1_mission_1af8d06941d424d57bcc2b55f8f9a2ea27}
```cpp
void dronecore::Mission::set_current_mission_item_async(int current, result_callback_t callback)
```


Sets the mission item index to go to (asynchronous).

By setting the current index to 0, the mission is restarted from the beginning. If it is set to a specific index of a mission item, the mission will be set to this item.


Note that this is not necessarily true for general missions using mavlink if loop counters are used.

**Parameters**

* int **current** - index for mission index to go to next (0 based)
* [result_callback_t](classdronecore_1_1_mission.md#classdronecore_1_1_mission_1a239f8d5853785d6ccf90c8c48b5ccf06) **callback** - callback to receive result of this request.

<!-- inbodydescription:  --> 
<!-- return_type: void -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### mission_finished() {#classdronecore_1_1_mission_1a63f73773d319ddac49f4c67f075368c6}
```cpp
bool dronecore::Mission::mission_finished() const
```


Checks if mission has been finished (synchronous).


**Returns**

&emsp;bool - true if mission is finished and the last mission item has been reached.

<!-- inbodydescription:  --> 
<!-- return_type: bool -->
<!-- return_type_comment: true if mission is finished and the last mission item has been reached. -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: yes -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### current_mission_item() {#classdronecore_1_1_mission_1af757c3f1332f0c3bb6b592b94cb24384}
```cpp
int dronecore::Mission::current_mission_item() const
```


Returns the current mission item index (synchronous).

If the mission is finished, the current mission item will be the total number of mission items (so the last mission item index + 1).

**Returns**

&emsp;int - current mission item index (0 based).

<!-- inbodydescription:  --> 
<!-- return_type: int -->
<!-- return_type_comment: current mission item index (0 based). -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: yes -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### total_mission_items() {#classdronecore_1_1_mission_1a1edf6f07441c3f67053c875157af6342}
```cpp
int dronecore::Mission::total_mission_items() const
```


Returns the total number of mission items (synchronous).


**Returns**

&emsp;int - total number of mission items

<!-- inbodydescription:  --> 
<!-- return_type: int -->
<!-- return_type_comment: total number of mission items -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: yes -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### subscribe_progress() {#classdronecore_1_1_mission_1a3290fc79eb22f899528328adfca48a61}
```cpp
void dronecore::Mission::subscribe_progress(progress_callback_t callback)
```


Subscribes to mission progress (asynchronous).


**Parameters**

* [progress_callback_t](classdronecore_1_1_mission.md#classdronecore_1_1_mission_1aeda7795cd898008afc05b779f99b704b) **callback** - callback to receive mission progress

<!-- inbodydescription:  --> 
<!-- return_type: void -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### operator=() {#classdronecore_1_1_mission_1ae946abaf32a30cb0b803a145f095217d}
```cpp
const Mission& dronecore::Mission::operator=(const Mission &)=delete
```


Equality operator (object is not copyable).


**Parameters**

* const [Mission](classdronecore_1_1_mission.md) & **** - 

**Returns**

&emsp;const [Mission](classdronecore_1_1_mission.md) & - 

<!-- inbodydescription:  --> 
<!-- return_type: const [Mission](classdronecore_1_1_mission.md) & -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: no -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->


### result_str() {#classdronecore_1_1_mission_1ac2abe4b9f52e32900f84e5bf47d38fe2}
```cpp
static const char * dronecore::Mission::result_str(Result result)
```


Gets a human-readable English string for an [Mission::Result](classdronecore_1_1_mission.md#classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cda).


**Parameters**

* [Result](classdronecore_1_1_mission.md#classdronecore_1_1_mission_1a529b17f5b63508494ca22fc247598cda) **result** - 

**Returns**

&emsp;const char * - 

<!-- inbodydescription:  --> 
<!-- return_type: const char * -->
<!-- return_type_comment:  -->
<!-- prot: public -->
<!-- static: yes -->
<!-- const: no -->
<!-- explicit: no -->
<!-- virt: non-virtual -->
<!-- inline: no -->