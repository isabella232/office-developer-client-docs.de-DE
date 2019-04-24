---
title: Erste Schritte beim Entwickeln von Project Server-Workflows
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Demand Management-Prozesse in Project Server 2013 bieten Workflows, die Ihnen bei der Verwaltung von Projektvorschlägen und Portfolioanalysen helfen. Dieser Abschnitt enthält Artikel mit Informationen zum Erstellen von Workflows für Project Server.
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344471"
---
# <a name="getting-started-developing-project-server-workflows"></a>Erste Schritte beim Entwickeln von Project Server-Workflows

Demand Management-Prozesse in Project Server 2013 bieten Workflows, die Ihnen bei der Verwaltung von Projektvorschlägen und Portfolioanalysen helfen. Dieser Abschnitt enthält Artikel mit Informationen zum Erstellen von Workflows für Project Server.
  
Für Project Server 2013-Workflows wird die SharePoint Server 2013-Workflow Plattform verwendet, die auf Version 4 von Windows Workflow Foundation (WF4) basiert. WF4-basierte Workflows sind deklarativ, was bedeutet, dass das Workflow-Entwurfstool Workflowphasen, Aktionen, Bedingungen und andere Elemente in XAML-Code speichert, der zur Laufzeit interpretiert wird. Sie können entweder SharePoint Designer 2013 oder Visual Studio 2012 verwenden, um deklarative Workflows zu erstellen. Ein Workflow erfordert das Workflow-Manager-Client 1,0-Ausführungsmodul, das sich auf einem lokalen Server für lokale Lösungen oder auf einem Remoteserver für Project Online-Lösungen befinden kann.
  
Sie können SharePoint Designer 2013 verwenden, um relativ einfache deklarative Workflows zu erstellen. Für komplexe Workflows und Workflowvorlagen, die wieder verwendet werden können, können Sie mit Visual Studio 2012 Workflows für Project Web App entwickeln und Debuggen. Weitere Informationen finden Sie unter [Erstellen von Projekt Workflows mit Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).
  
> [!IMPORTANT]
> Verwenden Sie eine Testinstallation von Project Server, keine Produktionsinstallation, um Workflows zu entwickeln und zu testen. Workflows, die für Vorabversionen von Project Server 2013 entwickelt wurden, müssen für die Veröffentlichungsversion getestet werden und müssen möglicherweise erneut erstellt und erneut bereitgestellt werden. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Erstellen eines Project Server-Workflows für das Bedarfs Management](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>Siehe auch



[Massenaktualisierung von benutzerdefinierten Feldern und Erstellen von Projektwebsites aus einem Project Online-Workflow](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[Entwickeln von Workflows in SharePoint Designer 2013 und Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[Neuerungen in Workflows für SharePoint 2013](https://msdn.microsoft.com/library/jj163177.aspx)
  
[Entwickeln von SharePoint 2013-Workflows mit Visual Studio](https://msdn.microsoft.com/library/jj163199.aspx)
  
[Erstellen von Projekt Workflows mit Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation ](https://msdn.microsoft.com/library/dd489441.aspx)
  
[Einführung in Windows Workflow Foundation (WF) in .NET 4](https://msdn.microsoft.com/library/ee342461.aspx)
  
[Tramper es Guide to Demand Management (Whitepaper)](https://msdn.microsoft.com/library/ff973112.aspx)

