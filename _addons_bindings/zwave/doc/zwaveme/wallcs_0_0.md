---
layout: documentation
title: WALLC-S - ZWave
---

{% include base.html %}

# WALLC-S Wall Controller
This describes the Z-Wave device *WALLC-S*, manufactured by *Z-Wave.Me* with the thing type UID of ```zwaveme_wallcs_00_000```.

The device is in the category of *Wall Switch*, defining Any device attached to the wall that controls a binary status of something, for ex. a light switch.

![WALLC-S product image](https://www.cd-jackson.com/zwave_device_uploads/145/145_default.jpg)


The WALLC-S supports routing. This allows the device to communicate using other routing enabled devices as intermediate routers.  This device is unable to participate in the routing of data from other devices.

The WALLC-S does not permanently listen for messages sent from the controller - it will periodically wake up automatically to check if the controller has messages to send, but will sleep most of the time to conserve battery life. The wakeup period can be configured in the user interface - it is advisable not to make this too short as it will impact battery life - a reasonable compromise is 1 hour. The wakeup period does not impact the devices ability to report events or sensor data. The device can be manually woken with a button press on the device as described below - note that triggering a device to send an event is not the same as a wakeup notification, and this will not allow the controller to communicate with the device.

## Overview

No device information is provided in the database. Consider [updating the database](http://www.cd-jackson.com/index.php/zwave/zwave-device-database/zwave-device-list/devicesummary/145) to improve the documentation.

## Channels

The following table summarises the channels available for the WALLC-S -:

| Channel | Channel Id | Category | Item Type |
|---------|------------|----------|-----------|
| Dimmer | switch_dimmer | DimmableLight | Dimmer | 
| Scene Activation | scene_number |  | Number | 
| Scene Number | scene_number |  | Number | 
| Battery Level | battery-level | Battery | Number |

### Dimmer

The brightness channel allows to control the brightness of a light.
            It is also possible to switch the light on and off.

The ```switch_dimmer``` channel supports the ```Dimmer``` item and is in the ```DimmableLight``` category.

### Scene Activation

Triggers when a scene button is pressed.

The ```scene_number``` channel supports the ```Number``` item.

### Scene Number

Triggers when a scene button is pressed.

The ```scene_number``` channel supports the ```Number``` item.

### Battery Level

Represents the battery level as a percentage (0-100%). Bindings for things supporting battery level in a different format (e.g. 4 levels) should convert to a percentage to provide a consistent battery level reading.

The ```battery-level``` channel supports the ```Number``` item and is in the ```Battery``` category.



## Device Configuration

The following table provides a summary of the 10 configuration parameters available in the WALLC-S.
Detailed information on each parameter can be found in the sections below.

| Param | Name  | Description |
|-------|-------|-------------|
| 1 | Button 1 and 3 pair mode | In separate mode button 1 works with group 1, button 3 with groups 3. Click is On, Hold is dimming Up, Double click is Off, Click-Hold is dimming Down. In pair button 1/3 are Up/Down correspondingly. Click is On/Off, Hold is dimming Up/Down. Single clicks |
| 2 | Button 2 and 4 pair mode | In separate mode button 1 works with group 2, button 4 with groups 3. Click is On, Hold is dimming Up, Double click is Off, Click-Hold is dimming Down. In pair button 2/4 are Up/Down correspondingly. Click is On/Off, Hold is dimming Up/Down. Single clicks |
| 11 | Action on group 1 | In Switch On/Off only mode On command is sent on Dim Up, Off on Dim Down. In Scenes mode the scene ID sent is (10 \* group + ActionID), where ActionID is: 1 = On, 2 = Off, 3 = Dim Up Start, 4 = Dim Down Start, 5 = Dim Up Stop, 6 = Dim Down Stop |
| 12 | Action on group 2 | In Switch On/Off only mode On command is sent on Dim Up, Off on Dim Down. In Scenes mode the scene ID sent is (10 \* group + ActionID), where ActionID is: 1 = On, 2 = Off, 3 = Dim Up Start, 4 = Dim Down Start, 5 = Dim Up Stop, 6 = Dim Down Stop |
| 13 | Action on group 3 | In Switch On/Off only mode On command is sent on Dim Up, Off on Dim Down. In Scenes mode the scene ID sent is (10 \* group + ActionID), where ActionID is: 1 = On, 2 = Off, 3 = Dim Up Start, 4 = Dim Down Start, 5 = Dim Up Stop, 6 = Dim Down Stop |
| 14 | Action on group 4 | In Switch On/Off only mode On command is sent on Dim Up, Off on Dim Down. In Scenes mode the scene ID sent is (10 \* group + ActionID), where ActionID is: 1 = On, 2 = Off, 3 = Dim Up Start, 4 = Dim Down Start, 5 = Dim Up Stop, 6 = Dim Down Stop |
| 21 | Send the following Switch All commands |  |
| 22 | Invert buttons |  |
| 25 | Blocks wakeup even when wakeup interval is set | If the device wakes up and there is no controller nearby, several unsuccessful communication attempts will drain battery. |
| 30 | Send unsolicited Battery Report on Wake Up |  |
|  | Wakeup Interval | Sets the interval at which the device will accept commands from the controller |
|  | Wakeup Node | Sets the node ID of the device to receive the wakeup notifications |

### Parameter 1: Button 1 and 3 pair mode

In separate mode button 1 works with group 1, button 3 with groups 3. Click is On, Hold is dimming Up, Double click is Off, Click-Hold is dimming Down. In pair button 1/3 are Up/Down correspondingly. Click is On/Off, Hold is dimming Up/Down. Single clicks

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Separately |
| 1 | In pair without double clicks |
| 2 | In pair with double clicks |

The manufacturer defined default value is ```1``` (In pair without double clicks).

This parameter has the configuration ID ```config_1_1``` and is of type ```INTEGER```.


### Parameter 2: Button 2 and 4 pair mode

In separate mode button 1 works with group 2, button 4 with groups 3. Click is On, Hold is dimming Up, Double click is Off, Click-Hold is dimming Down. In pair button 2/4 are Up/Down correspondingly. Click is On/Off, Hold is dimming Up/Down. Single clicks

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Separately |
| 1 | In pair without double clicks |
| 2 | In pair with double clicks |

The manufacturer defined default value is ```1``` (In pair without double clicks).

This parameter has the configuration ID ```config_2_1``` and is of type ```INTEGER```.


### Parameter 11: Action on group 1

In Switch On/Off only mode On command is sent on Dim Up, Off on Dim Down. In Scenes mode the scene ID sent is (10 \* group + ActionID), where ActionID is: 1 = On, 2 = Off, 3 = Dim Up Start, 4 = Dim Down Start, 5 = Dim Up Stop, 6 = Dim Down Stop

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Disabled |
| 1 | Switch On/Off and Dim (send Basic Set and Switch Multilevel) |
| 2 | Switch On/Off only (send Basic Set) |
| 3 | Switch all |
| 4 | Send Scenes |
| 5 | Send Preconfigured Scenes |
| 7 | Control Door Lock |
| 8 | Central Scene to Gateway |

The manufacturer defined default value is ```1``` (Switch On/Off and Dim (send Basic Set and Switch Multilevel)).

This parameter has the configuration ID ```config_11_1``` and is of type ```INTEGER```.


### Parameter 12: Action on group 2

In Switch On/Off only mode On command is sent on Dim Up, Off on Dim Down. In Scenes mode the scene ID sent is (10 \* group + ActionID), where ActionID is: 1 = On, 2 = Off, 3 = Dim Up Start, 4 = Dim Down Start, 5 = Dim Up Stop, 6 = Dim Down Stop

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Disabled |
| 1 | Switch On/Off and Dim (send Basic Set and Switch Multilevel) |
| 2 | Switch On/Off only (send Basic Set) |
| 3 | Switch all |
| 4 | Send Scenes |
| 5 | Send Preconfigured Scenes |
| 7 | Control Door Lock |
| 8 | Central Scene to Gateway |

The manufacturer defined default value is ```1``` (Switch On/Off and Dim (send Basic Set and Switch Multilevel)).

This parameter has the configuration ID ```config_12_1``` and is of type ```INTEGER```.


### Parameter 13: Action on group 3

In Switch On/Off only mode On command is sent on Dim Up, Off on Dim Down. In Scenes mode the scene ID sent is (10 \* group + ActionID), where ActionID is: 1 = On, 2 = Off, 3 = Dim Up Start, 4 = Dim Down Start, 5 = Dim Up Stop, 6 = Dim Down Stop

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Disabled |
| 1 | Switch On/Off and Dim (send Basic Set and Switch Multilevel) |
| 2 | Switch On/Off only (send Basic Set) |
| 3 | Switch all |
| 4 | Send Scenes |
| 5 | Send Preconfigured Scenes |
| 7 | Control Door Lock |
| 8 | Central Scene to Gateway |

The manufacturer defined default value is ```1``` (Switch On/Off and Dim (send Basic Set and Switch Multilevel)).

This parameter has the configuration ID ```config_13_1``` and is of type ```INTEGER```.


### Parameter 14: Action on group 4

In Switch On/Off only mode On command is sent on Dim Up, Off on Dim Down. In Scenes mode the scene ID sent is (10 \* group + ActionID), where ActionID is: 1 = On, 2 = Off, 3 = Dim Up Start, 4 = Dim Down Start, 5 = Dim Up Stop, 6 = Dim Down Stop

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Disabled |
| 1 | Switch On/Off and Dim (send Basic Set and Switch Multilevel) |
| 2 | Switch On/Off only (send Basic Set) |
| 3 | Switch all |
| 4 | Send Scenes |
| 5 | Send Preconfigured Scenes |
| 7 | Control Door Lock |
| 8 | Central Scene to Gateway |

The manufacturer defined default value is ```1``` (Switch On/Off and Dim (send Basic Set and Switch Multilevel)).

This parameter has the configuration ID ```config_14_1``` and is of type ```INTEGER```.


### Parameter 21: Send the following Switch All commands



The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 1 | NO (Normal Open) |
| 2 | NC (Normal Close) |
| 255 | Switch all on and off |

The manufacturer defined default value is ```1``` (NO (Normal Open)).

This parameter has the configuration ID ```config_21_1``` and is of type ```INTEGER```.


### Parameter 22: Invert buttons



The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | No |
| 1 | Yes |

The manufacturer defined default value is ```0``` (No).

This parameter has the configuration ID ```config_22_1``` and is of type ```INTEGER```.


### Parameter 25: Blocks wakeup even when wakeup interval is set

If the device wakes up and there is no controller nearby, several unsuccessful communication attempts will drain battery.

The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | Wakeup is blocked |
| 1 | Wakeup is possible |

The manufacturer defined default value is ```0``` (Wakeup is blocked).

This parameter has the configuration ID ```config_25_1``` and is of type ```INTEGER```.


### Parameter 30: Send unsolicited Battery Report on Wake Up



The following option values may be configured -:

| Value  | Description |
|--------|-------------|
| 0 | No |
| 1 | To same node as wake up notification |
| 2 | Broadcast to neighbours |

The manufacturer defined default value is ```0``` (No).

This parameter has the configuration ID ```config_30_1``` and is of type ```INTEGER```.

### Wakeup Interval

The wakeup interval sets the period at which the device will listen for messages from the controller. This is required for battery devices that sleep most of the time in order to conserve battery life. The device will wake up at this interval and send a message to the controller to tell it that it can accept messages - after a few seconds, it will go back to sleep if there is no further communications. 

This setting is defined in *seconds*. It is advisable not to set this interval too short or it could impact battery life. A period of 1 hour (3600 seconds) is suitable in most instances.

Note that this setting does not affect the devices ability to send sensor data, or notification events.

This parameter has the configuration ID ```wakeup_interval``` and is of type ```INTEGER```.

### Wakeup Node

When sleeping devices wake up, they send a notification to a listening device. Normally, this device is the network controller, and normally the controller will set this automatically to its own address.
In the event that the network contains multiple controllers, it may be necessary to configure this to a node that is not the main controller. This is an advanced setting and should not be changed without a full understanding of the impact.

This parameter has the configuration ID ```wakeup_node``` and is of type ```INTEGER```.


## Association Groups

Association groups allow the device to send unsolicited reports to the controller, or other devices in the network. Using association groups can allow you to eliminate polling, providing instant feedback of a device state change without unnecessary network traffic.

The WALLC-S supports 5 association groups.

### Group 1: Lifeline


This group supports 10 nodes.

### Group 2: Group 1


This group supports 10 nodes.

### Group 3: Group 2


This group supports 10 nodes.

### Group 4: Group 3


This group supports 10 nodes.

### Group 5: Group 4


This group supports 10 nodes.

## Technical Information

### Endpoints

#### Endpoint 0

| Command Class | Comment |
|---------------|---------|
| COMMAND_CLASS_NO_OPERATION_V1| |
| COMMAND_CLASS_BASIC_V1| |
| COMMAND_CLASS_SWITCH_MULTILEVEL_V0| Linked to BASIC|
| COMMAND_CLASS_SCENE_ACTIVATION_V0| |
| COMMAND_CLASS_SCENE_CONTROLLER_CONF_V0| |
| COMMAND_CLASS_CENTRAL_SCENE_V0| |
| COMMAND_CLASS_CONFIGURATION_V1| |
| COMMAND_CLASS_MANUFACTURER_SPECIFIC_V1| |
| COMMAND_CLASS_BATTERY_V1| |
| COMMAND_CLASS_WAKE_UP_V2| |
| COMMAND_CLASS_ASSOCIATION_V1| |
| COMMAND_CLASS_VERSION_V1| |
| COMMAND_CLASS_MULTI_CMD_V1| |

### Documentation Links

* [User Manual](https://www.cd-jackson.com/zwave_device_uploads/145/z-wave-me-wall-controller-set-manual.pdf)

---

Did you spot an error in the above definition or want to improve the content?
You can [contribute to the database here](http://www.cd-jackson.com/index.php/zwave/zwave-device-database/zwave-device-list/devicesummary/145).
