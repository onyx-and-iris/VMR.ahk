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

## `__New([p_path])` Constructor
Initilizes the VBVMR class (the actual wrapper) by setting the DLL path and type (64/32) as well as the string encoding which is based on the type of AHK that's running the script (Unicode/ANSI), then loads the correct DLL and its functions addresses.


---

## Methods

## `login()`
Calls voicemeeter's login function and initilizes VMR class properties (objects and arrays).

This method needs to be called first, in order to use the VMR class.
## `getType()`
Returns voicemeeter's type.

`1` : voicemeeter

`2` : voicemeeter Banana

`3` : voicemeeter Potato
## `runVoicemeeter([type])`
Runs the highest version installed , or a specific version if `type` is passed

`type` : 

`1` : voicemeeter

`2` : voicemeeter Banana

`3` : voicemeeter Potato
## `updateDevices()`
Updates the internal array of input and output devices, that's used for setting bus/strips devices
 
---

## `bus` and `strip` Arrays
Array of [`bus`/`strip` objects]({{ site.baseurl }}{% link VMR-Class/bus-strip-object.md %}).

## [`recorder`]({{ site.baseurl }}{% link VMR-Class/recorder-object.md %})
Use this object to control voicemeeter's recorder.

## [`vban`]({{ site.baseurl }}{% link VMR-Class/vban-object.md %})
Use this object to control voicemeeter's VBAN interface

## [`command`]({{ site.baseurl }}{% link VMR-Class/command-object.md %})
Use this object to access command methods.

## [`option`]({{ site.baseurl }}{% link VMR-Class/option-object.md %})
Use this object to access/modify option parameters.

## [`macroButton`]({{ site.baseurl }}{% link VMR-Class/macrobutton-object.md %})
Use this object to access/modify macro buttons statuses.

## Callback functions
Set callback functions for certain events (e.g. to update a user interface)

* `on_update_levels_callback` : called whenever the [`level`]({{ site.baseurl }}{% link VMR-Class/bus-strip-object.md %}#retrieve-the-gain-level-of-a-busstrip) array for bus/strip objects is updated.
* `on_update_parameters_callback` : called whenever voicemeeter's parameters change on the UI or by another app.
* `on_update_macrobuttons_callback` : called whenever a macrobutton's state is changed.


```lua
    ;--> Set a function object
   voicemeeter.on_update_levels_callback:= Func("syncLevels")
```
{: .fs-4 }
* [See ui_example.ahk](https://github.com/SaifAqqad/VMR.ahk/blob/master/examples/ui_example.ahk)
<br>
* [More info on function objects](https://www.autohotkey.com/docs/objects/Func.htm)
{: .fs-3 }
