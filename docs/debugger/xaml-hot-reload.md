---
title: "Write and debug XAML using XAML hot reload"
description: "XAML hot reload, or XAML edit and continue, allows you to make changes to your XAML code while running apps"
ms.custom: ""
ms.date: "02/28/2019"
ms.topic: "conceptual"
helpviewer_keywords:
  - "xaml edit and continue"
  - "xaml hot reload"
author: "mikejo5000"
ms.author: "mikejo"
manager: jillfra
ms.workload: 
  - "multiple"
---
# Write and debug running XAML code with XAML hot reload in Visual Studio

Visual Studio XAML hot reload helps you build your WPF or UWP app UI by letting you make changes to XAML code while your app is running. This feature enables you to incrementally build and test XAML code with the benefit of the running app's data context, authentication state, and other real-world complexity that’s hard to simulate during design-time.

XAML hot reload is especially helpful in these scenarios:

* Fixing UI problems found in your XAML code after the app was started in debug mode.

* Building a new UI component for an app that is under development, while taking advantage of your app’s runtime context.

|Supported Application Types|Operating System and Tools|
|-|-|-|
|Windows Presentation Foundation (WPF) |.NET Framework 4.6+</br>Windows 7 and above |
|Universal Windows apps (UWP)|Windows 10 and above, with the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk) 14393+ |

> [!NOTE]
> Visual Studio XAML hot reload is currently only supported when running your application in Visual Studio with the debugger attached (**F5** or **Start debugging**). You can't enable this experience by using *Attach to process*.

## Known limitations

The following are known limitations of XAML hot reload. To work around any limitation that you run into, just stop the debugger, and then complete the operation.

|Limitation|WPF|UWP|Notes|
|-|-|-|-|
|Wiring events to controls while the app is running|Not Supported|Not supported|See error: *Ensure Event Failed*|
|Creating resource objects in a resource dictionary such as those in your app's Page/Window or *App.xaml*|Not Supported|Supported|Example: adding a ```SolidColorBrush``` into a resource dictionary for use as a ```StaticResource```.</br>Note: Static resources, style converters, and other elements written into a resource dictionary can be applied/used while using XAML hot reload. Only the creation of the resource is not supported.</br> Changing the resource dictionary ```Source``` property.| 
|Adding new controls, classes, windows, or other files to your project while the app is running|Not Supported|Not Supported|None|
|Managing NuGet packages (adding/removing/updating packages)|Not Supported|Not Supported|None|
|Changing data binding that uses the {x:Bind} markup extension|N/A|Supported in Visual Studio 2019 and later versions|Not supported in Visual Studio 2018 or previous versions|

## Error messages

You may come across the following errors while using XAML hot reload.

|Error message|Description|
|-|-|-|
|Ensure Event Failed|Error indicates you are attempting to wire an event to one of your controls, which isn’t supported while your application is running.|
|XAML Edit and Continue did not find any elements to update.|Error occurs when you are editing XAML that hot reload cannot update in your app.</br> This error can sometimes be fixed by using your running app to navigate to a view where the XAML is used.</br> Sometimes, this error means that the specific change can't be applied until you restart the debugging session. |
|This change is not supported during a debugging session.|Error indicates that the change you are attempting is not supported by XAML hot reload. Stop the debugging session, make the change, and then restart the debugging session.|