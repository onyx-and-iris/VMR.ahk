---
layout: default
title: bus/strip object
parent: VMR-Object
nav_order: 3
---
# `bus`/`strip` object

Use this object to access or modify bus/strip parameters.
for a list of all parameters, check out [VBVMR docs](http://download.vb-audio.com/Download_CABLE/VoicemeeterRemoteAPI.pdf#page=11)

---

## Set any parameter

```
    voicemeeter.bus[1].gain:= 10.5
    voicemeeter.strip[3].FadeTo:= "(-10.0, 3000)"
```

## Retrieve any parameter
```
    current_gain:= voicemeeter.bus[3].gain
    is_assigned:= voicemeeter.strip[1].B2
    is_muted:= voicemeeter.bus[1].mute
```

## Set a bus/strip's device
```
    ; bus[1].device[driver]:= device_name 
    ; driver can be ["wdm","mme","asio","ks]
    ; device_name can be any substring of the full name

    voicemeeter.strip[2].device["asio"]:= "Microphone (2)" 
```

## Retrieve a bus/strip's device name
```
    device_name:= voicemeeter.bus[2].device
```

## Increment/decrement gain parameter
```
    voicemeeter.bus[3].gain--
    db:= ++voicemeeter.bus[1].gain 
    ; db contains the incremented value
```

## Toggle mute parameter
```
    voicemeeter.bus[1].mute:= 1

    voicemeeter.bus[1].mute:= -1
    is_muted:= voicemeeter.bus[1].mute ;0
    ; OR
    voicemeeter.bus[1].mute--
    is_muted:= voicemeeter.bus[1].mute ;1
```

## Retrieve the gain level of a bus/strip
`level` Array : contains the current level (in dB) for every channel a bus/strip has.

Hardware (physical) strips have 2 channels (left, right), Buses and virtual strips have 8 channels.
```
    level := voicemeeter.bus[1].level[1] 
    max_level := Max(voicemeeter.bus[1].level*)
```