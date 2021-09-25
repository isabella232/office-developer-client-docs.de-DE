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
- Project 2013, Architektur und Programmierbarkeit, Programmierbarkeit, Project Server, Project 2013, Vorteile für EPM, Architektur und Project Server
ms.localizationpriority: medium
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: In den Artikeln in diesem Abschnitt wird die allgemeine Architektur der Lösung für die Enterprise Project Verwaltung (EPM) beschrieben, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
ms.openlocfilehash: 975eaefe65599954e13a402083f43da7dc5018c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628990"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Project Server 2013-Architektur und Programmierbarkeit

In den Artikeln in diesem Abschnitt wird die allgemeine Architektur der Lösung für die Enterprise Project Verwaltung (EPM) beschrieben, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
  
Project Server 2013 wurde mit dem .NET Framework 4 erstellt und ist die dritte Hauptversion von Project Server, um eine echte mehrstufige Architektur bereitzustellen. Für den Cloudzugriff implementiert Project Server 2013 ein clientseitiges Objektmodell (CSOM) und einen OData-Dienst für Berichte, die in Webanwendungen, mobilen Anwendungen und Silverlight-Anwendungen verwendet werden können. Für lokale Anwendungen können Clients entweder das CSOM oder die PSI-Dienste (Project Server Interface) verwenden. 
  
## <a name="introduction-to-project-server-architecture"></a>Einführung in Project Serverarchitektur

In den Themen in diesem Abschnitt wird die allgemeine Architektur der Lösung für die Enterprise Project Verwaltung (EPM) beschrieben, die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
  
Für den programmgesteuerten Zugriff auf Project Server sollten Sie entweder das CSOM oder die PSI-Dienste mit der Windows Communication Foundation (WCF)-Schnittstelle verwenden. Die ASMX-Webdienstschnittstelle der PSI ist in Project Server 2013 veraltet, funktioniert aber weiterhin. Die PSI ermöglicht den effizienten Zugriff mithilfe von Datasets, und Sie können Handler für serverseitige Ereignisse erstellen. Das CSOM selbst verwendet die PSI, um auf die Project Server-Geschäftsobjektebene zuzugreifen. Anstelle von vier Project Serverdatenbanken verwendet Project Server 2013 eine einzige Datenbank auf der Datenzugriffsebene.
  
Project Server 2013 ist tief in SharePoint Server 2013 integriert. Der Project-Anwendungsdienst kann anderen SharePoint Websitesammlungen in der Farm zugeordnet werden. Project Server kann mit SharePoint Aufgabenlisten in der Websitesammlung arbeiten und berichte, und er kann auch die vollständige Kontrolle darüber erhalten, wo Project Server die Aufgabenlisten als Enterprise-Projekte importiert und verwaltet. Project Server verwendet auch Version 4 der Windows Workflow Foundation (WF4) und fügt Workflowaktivitäten für Demand Management-Lösungen hinzu.
  
Eine Erläuterung der vielen neuen Features, die Project 2013 für Entwickler bereitstellt, und der features, die veraltet sind, finden Sie [unter Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md).
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Project Server 2013-Architektur](project-server-2013-architecture.md) beschreibt die wichtigsten Teile der Project 2013-Plattform, einschließlich der Clients und Server. 
  
[Project Serverprogrammierbarkeit](project-server-programmability.md) erläutert die wichtigsten Erweiterbarkeitsfeatures von Project Server 2013, die Anpassung von Project Web App und das Aktualisieren von Anwendungen, die für frühere Project Serverversionen erstellt wurden. 
  
[Was die PSI tut und nicht tut,](what-the-psi-does-and-does-not-do.md) beschreibt Szenarien, in denen die PSI verwendet werden kann, und listet Dinge auf, die die PSI nicht ausführen kann. 
  
[Das CSOM beschreibt](what-the-csom-does-and-does-not-do.md) Szenarien, in denen das CSOM verwendet werden kann, und listet Dinge auf, die das CSOM nicht ausführen kann. 
  
### <a name="topics-not-covered"></a>Nicht behandelte Themen

Die Artikel im Abschnitt *"Architektur und Programmierbarkeit"* dokumentieren keine Features der Project Desktopclients (Project Standard 2013 und Project Professional 2013) oder Project Web App. 
  
Visual Basic for Applications (VBA)-Hilfe ist im Visual Basic-Editor in Project Standard und Project Professional verfügbar.
  
## <a name="see-also"></a>Siehe auch
<a name="bk_addresources"> </a>

- [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md)
    
- [Erste Schritte beim Entwickeln von Project Server-Workflows](getting-started-developing-project-server-workflows.md)
    

