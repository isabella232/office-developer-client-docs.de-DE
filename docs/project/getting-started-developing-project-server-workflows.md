---
title: Erste Schritte beim Entwickeln von Project Server-workflows
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Bei Bedarf, dass Verwaltungsprozesse in Project Server 2013 Workflows enthalten, die Ihnen helfen Verwalten von Projektvorschlägen und Portfolioanalysen. Dieser Abschnitt enthält Artikel, die zeigen, wie Sie zum Erstellen von Workflows für Project Server.
ms.openlocfilehash: 275f61b7992423a5e10a7ba90b8c76433290343e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796163"
---
# <a name="getting-started-developing-project-server-workflows"></a>Erste Schritte beim Entwickeln von Project Server-workflows

Bei Bedarf, dass Verwaltungsprozesse in Project Server 2013 Workflows enthalten, die Ihnen helfen Verwalten von Projektvorschlägen und Portfolioanalysen. Dieser Abschnitt enthält Artikel, die zeigen, wie Sie zum Erstellen von Workflows für Project Server.
  
Project Server 2013-Workflows mithilfe die SharePoint Server 2013-Workflow-Plattform, die auf Windows Workflow Foundation (WF4), Version 4 erstellt wird. WF4 basierenden Workflows sind deklarative, was bedeutet, dass das Workflow-Entwurfstool Workflowstufen, Aktionen, Bedingungen und andere Elemente in XAML-Code speichert, die zur Laufzeit interpretiert wird. SharePoint Designer 2013 oder Visual Studio 2012 können Sie um deklarative Workflows zu erstellen. Ein Workflow muss das Workflow-Manager-Client 1.0-Ausführungsmodul, der auf einem lokalen Server für lokale Lösungen oder auf einem Remoteserver für Project Online Solutions sein kann.
  
SharePoint Designer 2013 können Sie um deklarative Workflows relativ einfach zu erstellen. Für komplexe Workflows und Workflowvorlagen, die wiederverwendet werden können, können Sie Visual Studio 2012 verwenden, entwickeln und Debuggen von Workflows für Project Web App. Weitere Informationen finden Sie unter [Erstellen von Project-Workflows mithilfe von Visual Studio 2012](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).
  
> [!IMPORTANT]
> Verwenden Sie eine Testinstallation von Project Server, eine produktive-Installation, entwickeln und Testen des Workflows. Workflows, die für Vorabversionen von Project Server 2013 entwickelt werden für die endgültige Produktversion getestet werden müssen, und weist möglicherweise neu erstellt und erneut bereitgestellt werden. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Erstellen eines Project Server-Workflows für das Bedarfsmanagement](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>Siehe auch



[Massen-Update für benutzerdefinierte Felder und Erstellen von Projektwebsites in Project Online-workflow](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[Workflowentwicklung in SharePoint Designer 2013 und Visio 2013](http://msdn.microsoft.com/en-us/library/jj163272%28office.15%29.aspx)
  
[Neuerungen in Workflows für SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163177.aspx)
  
[Entwickeln von SharePoint 2013-Workflows mit Visual Studio](http://msdn.microsoft.com/en-us/library/jj163199.aspx)
  
[Erstellen von Project-Workflows mit Visual Studio 2012](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation](http://msdn.microsoft.com/en-us/library/dd489441.aspx)
  
[Einführung in die ein Entwickler zu Windows Workflow Foundation (WF) in .NET 4](http://msdn.microsoft.com/en-us/library/ee342461.aspx)
  
[Implementierung des projektbedarfsmanagements projektbedarfsmanagement (Whitepaper)](http://msdn.microsoft.com/en-us/library/ff973112.aspx)

