---
title: Erste Schritte beim Entwickeln von Project Server-Workflows
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Demand Management-Prozesse in Project Server 2013 umfassen Workflows, mit denen Sie Projektvorschläge und Portfolioanalysen verwalten können. Dieser Abschnitt enthält Artikel mit Informationen zum Erstellen von Workflows für Project Server.
ms.openlocfilehash: 7183969ec11cff06b3c3e16a7c0bd69ab89a3628
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613198"
---
# <a name="getting-started-developing-project-server-workflows"></a>Erste Schritte beim Entwickeln von Project Server-Workflows

Demand Management-Prozesse in Project Server 2013 umfassen Workflows, mit denen Sie Projektvorschläge und Portfolioanalysen verwalten können. Dieser Abschnitt enthält Artikel mit Informationen zum Erstellen von Workflows für Project Server.
  
Project Server 2013-Workflows verwenden die SharePoint Server 2013-Workflowplattform, die auf Version 4 von Windows Workflow Foundation (WF4) basiert. WF4-basierte Workflows sind deklarativ, was bedeutet, dass das Workflowentwurfstool Workflowphasen, Aktionen, Bedingungen und andere Elemente in XAML-Code speichert, der zur Laufzeit interpretiert wird. Sie können entweder SharePoint Designer 2013 oder Visual Studio 2012 verwenden, um deklarative Workflows zu erstellen. Ein Workflow erfordert das Workflow-Manager Client 1.0-Ausführungsmodul, das sich auf einem lokalen Server für lokale Lösungen oder auf einem Remoteserver für Project Online Lösungen befinden kann.
  
Sie können SharePoint Designer 2013 verwenden, um relativ einfache deklarative Workflows zu erstellen. Für komplexe Workflows und Workflowvorlagen, die wiederverwendet werden können, können Sie Visual Studio 2012 verwenden, um Workflows für Project Web App zu entwickeln und zu debuggen. Weitere Informationen finden Sie unter [Creating Project Workflows using Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).
  
> [!IMPORTANT]
> Verwenden Sie eine Testinstallation von Project Server und keine Produktionsinstallation, um Workflows zu entwickeln und zu testen. Workflows, die für Vorabversionen von Project Server 2013 entwickelt wurden, müssen auf die Releaseversion getestet werden und müssen möglicherweise erneut erstellt und erneut bereitgestellt werden. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Erstellen eines Project Serverworkflows für das Bedarfsmanagement](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>Siehe auch



[Massenaktualisierung benutzerdefinierter Felder und Erstellen von Projektwebsites aus einem Project Online-Workflow](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[Entwickeln von Workflows in SharePoint Designer 2013 und Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[Neuerungen in Workflows für SharePoint 2013](https://msdn.microsoft.com/library/jj163177.aspx)
  
[Entwickeln von SharePoint 2013-Workflows mit Visual Studio](https://msdn.microsoft.com/library/jj163199.aspx)
  
[Erstellen von Project Workflows mit Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation ](https://msdn.microsoft.com/library/dd489441.aspx)
  
[Einführung eines Entwicklers in Windows Workflow Foundation (WF) in .NET 4](https://msdn.microsoft.com/library/ee342461.aspx)
  
[Leitfaden für Hitchhiker zum Bedarfsmanagement (Whitepaper)](https://msdn.microsoft.com/library/ff973112.aspx)

