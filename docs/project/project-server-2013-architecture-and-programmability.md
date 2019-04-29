---
title: Project Server 2013-Architektur und Programmierbarkeit
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- architecture
- platform
- Project
- Project architecture
- Project programmability
- Project Server architecture
- Project Server programmability
keywords:
- Project 2013, Architektur und Programmierbarkeit, Programmierbarkeit, Project Server, Project 2013, Vorteile für EPM, Architecture und Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: In den Artikeln in diesem Abschnitt wird die Gesamtarchitektur der Enterprise Project Management-Lösung (EPM) beschrieben, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413787"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Project Server 2013-Architektur und Programmierbarkeit

In den Artikeln in diesem Abschnitt wird die Gesamtarchitektur der Enterprise Project Management-Lösung (EPM) beschrieben, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
  
Project Server 2013 wurde mit .NET Framework 4 erstellt und ist die dritte Hauptversion von Project Server, um eine echte mehrstufige Architektur bereitzustellen. Für den Cloud-Zugriff implementiert Project Server 2013 ein clientseitiges Objektmodell (CSOM) und einen OData-Dienst für Berichte, die in Webanwendungen, mobilen Anwendungen und Silverlight-Anwendungen verwendet werden können. Für lokale Anwendungen können Clients entweder die CSOM oder die PSI-Dienste (Project Server Interface) verwenden. 
  
## <a name="introduction-to-project-server-architecture"></a>Einführung in die Project Server-Architektur

Die Themen in diesem Abschnitt beschreiben die Gesamtarchitektur der Enterprise Project Management (EPM)-Lösung, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
  
Für den programmgesteuerten Zugriff auf Project Server sollten Sie entweder die CSOM oder die PSI-Dienste mit der Windows Communication Foundation (WCF)-Schnittstelle verwenden. Die ASMX-Webdienst-Schnittstelle der PSI ist in Project Server 2013 veraltet, funktioniert aber immer noch. Das PSI ermöglicht den effizienten Zugriff mithilfe von Datasets und Sie können Handler für serverseitige Ereignisse erstellen. Der CSOM selbst verwendet die PSI für den Zugriff auf die Project Server-Geschäftsobjektebene. Anstelle von vier Project Server-Datenbanken verwendet Project Server 2013 eine einzelne Datenbank in der Datenzugriffsschicht.
  
Project Server 2013 ist in SharePoint Server 2013 integriert. Der Project-Anwendungsdienst kann anderen SharePoint-Websitesammlungen in der Farm zugeordnet werden. Project Server kann mit SharePoint-Aufgabenlisten in der Websitesammlung arbeiten und Berichte dazu und kann auch vollständige Kontrolle darüber erhalten, wo Project Server die Aufgabenlisten als Enterprise-Projekte importiert und verwaltet. Project Server verwendet außerdem Version 4 des Windows Workflow Foundation (WF4) und fügt Workflow Aktivitäten für Bedarfs Verwaltungslösungen hinzu.
  
Eine Erläuterung der vielen neuen Features von Project 2013 für Entwickler und der Features, die veraltet sind, finden Sie unter [Updates für Entwickler in project 2013](updates-for-developers-in-project-2013.md).
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

In der [Architektur von Project Server 2013](project-server-2013-architecture.md) werden die wichtigsten Teile der Project 2013-Plattform beschrieben, einschließlich der Clients und Server. 
  
[Project Server-Programmierbarkeit](project-server-programmability.md) erläutert die wichtigsten Erweiterbarkeitsfeatures von project Server 2013, die Anpassung von Project Web App und das Aktualisieren von Anwendungen, die für frühere Project Server-Versionen erstellt wurden. 
  
[Was die PSI tut und was nicht](what-the-psi-does-and-does-not-do.md) , beschreibt Szenarios, in denen das PSI verwendet werden kann, und listet Dinge auf, die das PSI nicht kann. 
  
[Was das CSOM tut und was nicht](what-the-csom-does-and-does-not-do.md) , beschreibt Szenarios, in denen die CSOM verwendet werden kann, und listet die Dinge auf, die das CSOM nicht ausführen kann. 
  
### <a name="topics-not-covered"></a>Themen werden nicht behandelt

Die Artikel im Abschnitt *Architektur und Programmierbarkeit* dokumentieren nicht die Features der Project-Desktop Clients (project Standard 2013 und project Professional 2013) oder Project Web App. 
  
Visual Basic for Applications (VBA)-Hilfe ist im Visual Basic-Editor in Project Standard und Project Professional verfügbar.
  
## <a name="see-also"></a>Siehe auch
<a name="bk_addresources"> </a>

- [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md)
    
- [Erste Schritte beim Entwickeln von Project Server-Workflows](getting-started-developing-project-server-workflows.md)
    

