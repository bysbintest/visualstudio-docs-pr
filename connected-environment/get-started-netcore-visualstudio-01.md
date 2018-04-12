---
title: "Create a .NET Core development environment with containers using Kubernetes in the cloud with Visual Studio - Step 1 - Install tools | Microsoft Docs"
author: "johnsta"
ms.author: "johnsta"
ms.date: "04/05/2018"
ms.topic: "get-started-article"
ms.technology: "vsce-kubernetes"
description: "Rapid Kubernetes development with containers and microservices on Azure"
keywords: "Docker, Kubernetes, Azure, AKS, Azure Container Service, containers"
manager: "ghogen"
---
# Get Started on Connected Environment with .NET Core and Visual Studio

In this guide, you will learn how to:

1. Create a Kubernetes-based environment in Azure that is optimized for development.
1. Iteratively develop code in containers using Visual Studio.
1. Independently develop two separate services, and used Kubernetes' DNS service discovery to make a call to another service.
1. Productively develop and test your code in a team environment.

[!INCLUDE[](includes/see-troubleshooting.md)]

## Install the Connected Environment CLI
Connected Environment requires minimal local machine setup. Most of your development environment's configuration gets stored in the cloud, and is shareable with other users.

1. Download and run the [Connected Environment CLI Installer](https://aka.ms/get-vsce-windows). 

## Get Kubernetes Debugging Tools
While you can use the Connected Environment CLI as a standalone tool, rich features like **Kubernetes debugging** are available for .NET Core developers using **VS Code** or **Visual Studio**.

### Visual Studio debugging 
1. Install the latest version of [Visual Studio 2017](https://www.visualstudio.com/vs/)
1. In the Visual Studio installer make sure the following Workload is selected:
    * ASP.NET and web development
1. Install the [Visual Studio extension for Connected Environment](https://aka.ms/get-vsce-visualstudio)

We're now ready to Create an ASP.NET web app with Visual Studio.

> [!div class="nextstepaction"]
> [Create an ASP.NET web app](get-started-netcore-visualstudio-02.md)
