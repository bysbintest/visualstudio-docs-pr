---
title: "Create a Windows Forms app with Visual Basic"
description: "Learn how to create a Windows Forms app in Visual Studio with Visual Basic, step-by-step."
ms.date: 03/23/2019
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
ms.devlang: vb
author: TerryGLee
ms.author: tglee
manager: jillfra
dev_langs:
  - vb
ms.workload:
  - "multiple"
---
# Create a Windows Forms app in Visual Studio with Visual Basic

In this short introduction to the Visual Studio integrated development environment (IDE), you'll create a simple Visual Basic application that has a Windows-based user interface (UI).

::: moniker range="vs-2017"

If you haven't already installed Visual Studio, go to the [Visual Studio downloads](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) page to install it for free.

::: moniker-end

::: moniker range="vs-2019"

If you haven't already installed Visual Studio, go to the [Visual Studio downloads](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) page to install it for free.

> [!NOTE]
> Some of the screenshots in this tutorial use the dark theme. If you aren't using the dark theme but would like to, see the [Personalize the Visual Studio IDE and Editor](../ide/quickstart-personalize-the-ide.md) page to learn how.

::: moniker-end

## Create a project

First, you'll create a Visual Basic application project. The project type comes with all the template files you'll need, before you've even added anything.

::: moniker range="vs-2017"

1. Open Visual Studio 2017.

2. From the top menu bar, choose **File** > **New** > **Project**.

3. In the **New Project** dialog box in the left pane, expand **Visual Basic**, and then choose **Windows Desktop**. In the middle pane, choose **Windows Forms App (.NET Framework)**. Then name the file `HelloWorld`.

     If you don't see the **Windows Forms App (.NET Framework)** project template, cancel out of the **New Project** dialog box and from the top menu bar, choose **Tools** > **Get Tools and Features**. The Visual Studio Installer launches. Choose the **.NET desktop development** workload, then choose **Modify**.

     ![.NET Core workload in the Visual Studio Installer](../ide/media/install-dot-net-desktop-env.png)

::: moniker-end

::: moniker range="vs-2019"

1. Open Visual Studio 2019.

1. On the start window, choose **Create a new project**.

   ![View the 'Create a new project' window](../get-started/media/vs-2019/create-new-project-dark-theme.png)

1. On the **Create a new project** window, enter or type *Windows Forms* in the search box. Next, choose **Visual Basic** from the Language list, and then choose **Windows** from the Platform list. 

   After you apply the language and platform filters, choose the **Windows Forms App (.NET Framework)** template, and then choose **Next**.

   ![Choose the Visual Basic template for the Windows Forms App (.NET Framework)](../get-started/visual-basic/media/vs-2019/vb-create-new-project-search-winforms-filtered.png)

   > [!NOTE]
   > If you do not see the **Windows Forms App (.NET Framework)** template, you can install it from the **Create a new project** window. In the **Not finding what you're looking for?** message, choose the **Install more tools and features** link.
   >
   > ![The 'Install more tools and features' link from the 'Not finding what you're looking for' message in the 'Create new project' window](../get-started/media/vs-2019/not-finding-what-looking-for.png) 
   > 
   > Next, in the Visual Studio Installer, choose the Choose the **.NET desktop development** workload.
   > 
   > ![.NET Core workload in the Visual Studio Installer](../ide/media/install-dot-net-desktop-env.png)
   >
   > After that, choose the **Modify** button in the Visual Studio Installer. You might be prompted to save your work; if so, do so. Next, choose **Continue** to install the workload. Then, return to step 2 in this "[Create a project](#create-a-project)" procedure.

1. In the **Configure your new project** window, type or enter *HelloWorld* in the **Project name** box. Then, choose **Create**.

   ![in the 'Configure your new project' window, name your project 'HelloWorld'](../get-started/visual-basic/media/vs-2019/vb-name-your-winform-project-helloworld.png)

   Visual Studio opens your new project.

::: moniker-end

## Create the application

After you select your Visual Basic project template and name your file, Visual Studio opens a form for you. A form is a Windows user interface. We'll create a "Hello World" application by adding controls to the form, and then we'll run the application.

### Add a button to the form

1. Click **Toolbox** to open the Toolbox fly-out window.

     ![Click the Toolbox to open the Toolbox window](../ide/media/vb-toolbox-toolwindow.png)

     (If you don't see the **Toolbox** fly-out option, you can open by pressing **Ctrl**+**Alt**+**X**.)

2. Click the **Pin** icon to dock the **Toolbox** window.

     ![Click the Pin icon to pin the Toolbox window to the IDE](../ide/media/vb-pin-the-toolbox-window.png)

3. Click the **Button** control and then drag it onto the form.

     ![Add a button to the form](../ide/media/vb-add-a-button-to-form1.png)

4. In the **Appearance** section (or the **Fonts** section) of the **Properties** window, type `Click this`, and then press **Enter**.

     ![Add text to the button on the form](../ide/media/vb-button-control-text.png)

     (If you don't see the **Properties** window, you can open it from the menu bar. To do so, click **View** > **Properties Window**. Or, press **F4**.)

5. In the **Design** section of the **Properties** window, change the name from **Button1** to `btnClickThis`, and then press **Enter**.

     ![Add a function to the button on the form](../ide/media/vb-button-control-function.png)

### Add a label to the form

Now that we've added a button control to create an action, let's add a label control to send text to.

1. Select the **Label** control from the **Toolbox** window, and then drag it onto the form and drop it beneath the **Click this** button.

2. In the **Design** section of the **Properties** window, change the name from **Label1** to `lblHelloWorld`, and then press **Enter**.

### Add code to the form

1. In the **Form1.vb &#91;Design&#93;** window, double-click the **Click this** button to open the **Form1.vb** window.

      (Alternatively, you can expand **Form1.vb** in **Solution Explorer**, and then click **Form1**.)

2. In the **Form1.vb** window, between the **Private Sub** line and the **End Sub** line (or between the **Public Class Form1** line and the **End Class** line), type the following code.

     ![Add code to the form](../ide/media/vb-add-code-to-the-form.png)

## Run the application

1. Click the **Start** button to run the application.

     ![Click Start to debug and run the app](../ide/media/vb-click-start-hello-world.png)

   Several things will happen. In the Visual Studio IDE, the **Diagnostics Tools** window will open, and an **Output** window will open, too. But outside of the IDE, a **Form1** dialog box appears. It will include your **Click this** button and text that says **Label1**.

2. Click the **Click this** button in the **Form1** dialog box. Notice that the **Label1** text changes to **Hello World!**.

    ![A Form1 dialog box that includes Label1 text ](../ide/media/vb-form1-dialog-hello-world.png)

Congratulations on completing this quickstart! We hope you learned a little bit about Visual Basic and the Visual Studio IDE. If you'd like to delve deeper, please continue with a tutorial in the **Tutorials** section of the table of contents.

## See also

* [Quickstart: Create a console app in Visual Studio with Visual Basic](quickstart-visual-basic-console.md)
* [Learn more about Visual Basic IntelliSense](visual-basic-specific-intellisense.md)
