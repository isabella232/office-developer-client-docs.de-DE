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
- Project 2013, Architektur und Programmierbarkeit, Programmierbarkeit, Project Server,Project 2013, Vorteile für EPM, Architecture und Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: In den Artikeln in diesem Abschnitt wird die Gesamtarchitektur der Enterprise Project Management (EPM)-Lösung beschrieben, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413787"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Project Server 2013-Architektur und Programmierbarkeit

In den Artikeln in diesem Abschnitt wird die Gesamtarchitektur der Enterprise Project Management (EPM)-Lösung beschrieben, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
  
Project Server 2013 wurde mit .NET Framework 4 erstellt und ist die dritte Hauptversion von Project Server, die eine echte mehrstufige Architektur bietet. Für den Cloudzugriff implementiert Project Server 2013 ein clientseitiges Objektmodell (CSOM) und einen OData-Dienst für die Berichterstellung, der in Webanwendungen, mobilen Anwendungen und Silverlight-Anwendungen verwendet werden kann. Für lokale Anwendungen können Clients entweder das CSOM oder die Project Server Interface (PSI) verwenden. 
  
## <a name="introduction-to-project-server-architecture"></a>Einführung in Project Serverarchitektur

In den Themen in diesem Abschnitt wird die Gesamtarchitektur der Enterprise Project Management (EPM)-Lösung beschrieben, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
  
Für den programmgesteuerten Zugriff auf Project Server sollten Sie entweder das CSOM oder die PSI-Dienste mit der Windows Communication Foundation (WCF)-Schnittstelle verwenden. Die ASMX-Webdienstschnittstelle der PSI ist in Project Server 2013 veraltet, funktioniert aber weiterhin. Die PSI ermöglicht einen effizienten Zugriff mithilfe von Datasets, und Sie können Handler für serverseitige Ereignisse erstellen. Das CSOM selbst verwendet die PSI, um auf die Project Server-Geschäftsobjektebene zu zugreifen. Statt vier Project Serverdatenbanken verwendet Project Server 2013 eine einzelne Datenbank in der Datenzugriffsebene.
  
Project Server 2013 integriert sich tief in SharePoint Server 2013. Der Project-Anwendungsdienst kann anderen websitesammlungen SharePoint in der Farm zugeordnet werden. Project Server kann mit SharePoint Aufgabenlisten in der Websitesammlung arbeiten und diese melden und auch voll steuern, wo Project Server die Aufgabenlisten als Unternehmensprojekte importiert und verwaltet. Project Server verwendet auch Version 4 des Windows Workflow Foundation (WF4) und fügt Workflowaktivitäten für Lösungen zur Bedarfsverwaltung hinzu.
  
Eine Diskussion über die vielen neuen Features, die Project 2013 für Entwickler bietet, und der veralteten Features finden Sie unter [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Project Server 2013-Architektur](project-server-2013-architecture.md) beschreibt die wichtigsten Teile der Project 2013-Plattform, einschließlich der Clients und Server. 
  
[Project Server-Programmierbarkeit](project-server-programmability.md) behandelt die wichtigsten Erweiterbarkeitsfeatures von Project Server 2013, die Anpassung von Project Web App und das Upgrade von Anwendungen, die für frühere Project Server-Versionen erstellt wurden. 
  
[Was die PSI tut und](what-the-psi-does-and-does-not-do.md) nicht, beschreibt Szenarien, in denen die PSI verwendet werden kann, und listet Dinge auf, die die PSI nicht tun kann. 
  
[Was das CSOM](what-the-csom-does-and-does-not-do.md) tut und nicht, beschreibt Szenarien, in denen das CSOM verwendet werden kann, und listet Dinge auf, die das CSOM nicht tun kann. 
  
### <a name="topics-not-covered"></a>Themen, die nicht behandelt werden

Die Artikel im Abschnitt *Architektur* und Programmierbarkeit dokumentieren keine Features der Project-Desktopclients (Project Standard 2013 und Project Professional 2013) oder Project Web App. 
  
Visual Basic for Applications (VBA)-Hilfe ist im editor Visual Basic innerhalb von Project Standard und Project Professional.
  
## <a name="see-also"></a>Siehe auch
<a name="bk_addresources"> </a>

- [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md)
    
- [Erste Schritte beim Entwickeln von Project Server-Workflows](getting-started-developing-project-server-workflows.md)
    

