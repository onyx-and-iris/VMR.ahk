---
layout: default
title: VMR Class
has_children: true
nav_order: 2
permalink: /VMR-Class 
has_toc: false
---

# VMR Class

---

## `bus` and `strip` Arrays
Array of [`bus`/`strip` objects]({{ site.baseurl }}{% link VMR-Class/bus-strip-object.md %}).

## [`recorder` Object]({{ site.baseurl }}{% link VMR-Class/recorder-object.md %})
Use this object to control voicemeeter's recorder.

## [`vban` Object]({{ site.baseurl }}{% link VMR-Class/vban-object.md %})
Use this object to control VoiceMeeter's VBAN interface

## [`command` Object]({{ site.baseurl }}{% link VMR-Class/command-object.md %})
Use this object to access command methods.

## [`option` Object]({{ site.baseurl }}{% link VMR-Class/option-object.md %})
Use this object to access/modify option parameters.

## [`macroButton` Object]({{ site.baseurl }}{% link VMR-Class/macrobutton-object.md %})
Use this object to access/modify macro buttons statuses.

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
Updates the internal array of input and output devices, that's used for setting bus/strips devices
 