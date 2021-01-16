---
layout: default
title: VMR Object
has_children: true
nav_order: 2
permalink: /VMR-Object
---

# VMR Object

---

## `bus` and `strip` Arrays
Array of [`bus`/`strip` objects]({{ site.baseurl }}{% link VMR-Object/bus-strip-object.md %}).

## [`command` Object]()
Use this object to access command methods.

## [`recorder` Object]()
Use this object to control voicemeeter's recorder.

## [`option` Object]()
Use this object to access/modify option parameters.

## [`macroButton` Object]()
Use this object to access/modify macro buttons statuses.

## [`vban` Object]()
Use this object to control VoiceMeeter's VBAN interface

## `command` Object
Use this object to access [command methods]()

---

## Methods

## `login()`
loads VoiceMeeter's Library and calls VM's login function.

This method needs to be called at startup
## `getType()`
Returns Voicemeeter's type.

`1` : Voicemeeter

`2` : Voicemeeter Banana

`3` : Voicemeeter Potato
## `runVoicemeeter([type])`
Runs the highest version installed , or a specific version if `type` is specified

`type` : 

`1` : Voicemeeter

`2` : Voicemeeter Banana

`3` : Voicemeeter Potato
## `updateDevices()`
Updates the internal array of input and output devices, that is used for setting bus/strips devices
 