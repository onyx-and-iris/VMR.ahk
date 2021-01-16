---
layout: default
title: Getting started
nav_order: 1
permalink: /
---
###  Getting started
To use `VMR.ahk` in your script, follow these steps:
1.  Include it using `#Include VMR.ahk` or copy it to a [library folder](https://www.autohotkey.com/docs/Functions.htm#lib) and use `#Include <VMR>`

2.  create an object of the VMR class:
    ```
        voicemeeter:= new VMR()
    ```
    you can optionally pass the path for voicemeeter's folder:
    ```
        voicemeeter:= new VMR("C:\path\to\voicemeeter\")
    ```
3.  call the `login()` method:
    ```
        voicemeeter.login()
    ```
4. The `VMR` object will have two arrays, [`bus`]() and [`strip`](), as well as [other objects](), that will allow you to control voicemeeter in AHK.
    ```
        voicemeeter.bus[1].mute:= true
        voicemeeter.strip[4].gain++
    ```
##### This documentation is for VMR.ahk, If you need help with the Voicemeeter API check out [their documentation](http://download.vb-audio.com/Download_CABLE/VoicemeeterRemoteAPI.pdf)