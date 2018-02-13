---
title: "How to: Enable and Disable Full Solution Analysis for Managed Code | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "full solution analysis"
author: "gewarren"
ms.author: "gewarren"
manager: ghogen
ms.technology: vs-ide-code-analysis
ms.workload: 
  - "dotnet"
---
# How to: Enable and disable full solution analysis for managed code

*Full solution analysis* is a Visual Studio feature that enables you to see code analysis issues only in open Visual C# or Visual Basic files in your solution, or also in code files that are closed. By default, full solution analysis is enabled for Visual Basic and disabled for Visual C#.

While being able to see all issues in all files is useful, it can be distracting. It can also slow Visual Studio down if your solution is very large or has a lot of files. To limit the number of issues shown and improve Visual Studio performance, you can disable full solution analysis. You can easily reenable this feature if necessary.

## To toggle full solution analysis

1. To open the **Options** dialog box, on the menu bar in Visual Studio choose **Tools** > **Options**.

1. In the **Options** dialog box, choose **Text Editor** > **C#** or **Basic** > **Advanced**.

1. Select the **Enable full solution analysis** check box to enable full solution analysis, or clear the box to disable it. Choose the **OK** button when you're done.

    ![Enable full solution analysis check box.](../code-quality/media/fsa_toolsoptions.png "FSA_ToolsOptions")

## Results of enabling and disabling full solution analysis

In the following screenshot, you can see the results when full solution analysis is enabled. All errors and code analysis issues in *all* of the files in the solution appear, regardless of whether the files are open or not.

![Full solution analysis enabled.](../code-quality/media/fsa_enabled.png "FSA_Enabled")

The following screenshot shows the results from the same solution after disabling full solution analysis. Only errors and code analysis issues in open solution files appear in the Error List.

![Full solution analysis disabled.](../code-quality/media/fsa_disabled.png "FSA_Disabled")

## Automatically disabling full solution analysis

If Visual Studio detects that 200MB or less of system memory is available to it, it automatically disables full solution analysis (as well as some other features) if it's enabled. If this occurs, an alert appears informing you of this. A button lets you re-enable full solution analysis if desired.

![Alert text suspending full solution analysis](../code-quality/media/fsa_alert.png "FSA_Alert")