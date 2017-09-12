# DroneCore Paradigms/Usage

This topic provides general/overview information about how DroneCore is used, designed and some limitations. 


## Object Management

[DroneCore](../api_reference/classdronecore_1_1_drone_core.md) is the main library class. API consumers use it to discover and manage vehicles ([Device](../api_reference/classdronecore_1_1_device.md) objects), which in turn provide access to all other drone information and control objects.

DroneCore applications must create a `DroneCore` object and destroy it during application shut down. The object can be created as an automatic variable that is cleaned up when it goes out of scope, or you can dynamically create/destroy the object using `new`/`delete`.

All other objects are returned/owned by the API and will automatically be destroyed along with `DroneCore`.


## Error Handling

DroneCore APIs do not raise exceptions! Instead, methods that can fail return success or an error reason as `enum` values.

> **Tip** The error code usually reflects acknowledgment from the vehicle that it will perform the requested action (or not). The operation itself may not yet have completed (e.g. taking off).

The various classes also all provide methods getting human readable strings from their associated enum (e.g. [DroneCore::connection_result_str()](h../api_reference/classdronecore_1_1_drone_core.md#classdronecore_1_1_drone_core_1a84c40dcefcafe888c38a5ed8dd93b0af), [Telemetry::result_str()](../api_reference/classdronecore_1_1_telemetry.md#classdronecore_1_1_telemetry_1a05c6355b7f8743250b2a7a611ea5fb4a)). You can see how these are used in the example code.

## API Limitations/Behaviour
### Supported Vehicles

DroneCore has been designed to manage *aircraft* (VTOL, copter, fixed wing) that use the PX4 autopilot. 

The APIs include methods that do not make sense for other vehicle types - including "takeoff" and "land". While ground vehicles may work, they are not supported and are untested.


### Telemetry/Information

DroneCore `Telemetry` information may not precisely reflect the state of the connected vehicle.

DroneCore gets and stores vehicle state information from received MAVLink messages. The API is likely to more accurately reflect the device state if DroneCore is queried just after receiving an update rather than just before getting the next one.

The main implication is that developers need to use a channel and and update rate that allows them to perform the desired control algorithm - there is no point trying to use computer vision over an unreliable high-latency link. The rate at which update messages should be sent can be specified by using API (but will be limited by the bandwidth of the channel). 

`Info` information is static for a particular vehicle, so should remain accurate.


### Actions/Offboard

Actions methods (and any other "vehicle instructions") return when the vehicle has confirmed that the message was received and will be acted on (or not). The methods do not wait for the commanded action to complete.

So, for example, the [Action::land()](../api_reference/classdronecore_1_1_action.md#classdronecore_1_1_action_1ad1a50dd7bff99d3099916576efbf8cf6) method returns as soon as the vehicle confirms it will land, but will land at some later point. 

The implication is that developers will need to separately monitor the completion of the requested actions, if this is important to the application.


### Missions

The `Mission` and `MissionItem` APIs provide a the most useful *subset* of MAVLink mission commands as a developer-friendly API. 

Not every mission command behaviour supported by the protocol and PX4 will be supported by DroneCore. For example, at time of writing the API does not allow you to specify commands that jump back to previous commands.

### Connection Status

Connection state information may be up to 3 seconds out of date (callbacks are notified 3 seconds after the last heartbeat message).