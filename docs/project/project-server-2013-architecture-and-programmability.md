---
title: Architektur von Project Server 2013 und Programmierbarkeit
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
- Project 2013, Architektur und Programmierbarkeit, Programmierbarkeit, Project Server, Project 2013, Vorteile für EPM-Architektur und Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Die Artikel in diesem Abschnitt beschreiben die allgemeine Architektur der Lösung Enterprise Project Management (EPM), die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
ms.openlocfilehash: 6b5ab94968dbb996a370e0e5abb89813f5e41ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796308"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Architektur von Project Server 2013 und Programmierbarkeit

Die Artikel in diesem Abschnitt beschreiben die allgemeine Architektur der Lösung Enterprise Project Management (EPM), die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
  
Projektserver 2013 ist integriert mit .NET Framework 4 und der dritte Hauptversion von Project Server eine true mehrstufige Architektur zur Verfügung. Für den Zugriff der Cloud implementiert Project Server 2013 ein Client-seitigen Objektmodell (CSOM) und einen OData-Dienst für die berichterstellung, der verwendet werden können in Webanwendungen, mobile Anwendungen und Silverlight-Anwendungen. Für die Anwendung lokal können Clients die CSOM oder die Dienste für Project Server Interface (PSI) verwenden. 
  
## <a name="introduction-to-project-server-architecture"></a>Einführung in Project Server-Architektur

Die Themen in diesem Abschnitt beschreiben die allgemeine Architektur der Lösung Enterprise Project Management (EPM), die Project Professional 2013, Project Server 2013, Project Web App und SharePoint Server 2013 kombiniert.
  
Für den programmgesteuerten Zugriff auf Project Server sollten Sie die CSOM oder der PSI-Dienste mit der Windows Communication Foundation (WCF)-Schnittstelle verwenden. Die ASMX Webdienstschnittstelle für die PSI ist in Project Server 2013 veraltet, aber noch funktioniert. Die PSI ermöglicht den effizienten Zugriff durch Verwenden von Datasets und Handler für serverseitige Ereignisse erstellen. Das CSOM selbst verwendet die PSI, um die Project Server-geschäftsobjektschicht zuzugreifen. Anstelle von vier Project Server-Datenbanken verwendet Project Server 2013 eine einzelne Datenbank, in der Datenzugriffsschicht.
  
Projektserver 2013 integriert tief mit SharePoint Server 2013. Project-Anwendungsdienst können andere SharePoint-Websitesammlungen in der Farm zugeordnet werden. Projektserver kann effektives und Berichten über SharePoint-Aufgabenlisten in der Websitesammlung und kann auch Vollzugriff erhalten, auf dem Project Server importiert und verwaltet werden, dass die Aufgabenlisten als Enterprise-Projekte. Projektserver auch verwendet Version 4 von Windows Workflow Foundation (WF4) und fügt Workflowaktivitäten für Demand Management-Lösungen.
  
Eine Erläuterung der viele neue Features, die Project 2013 für Entwickler zur Verfügung stehen und der Features, die veraltet sind, finden Sie unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md).
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Architektur von Project Server 2013](project-server-2013-architecture.md) beschreibt die Hauptteile der Project 2013-Plattform, einschließlich der Clients und Servern. 
  
[Project Server-Programmierbarkeit](project-server-programmability.md) erläutert die Erweiterbarkeit der wichtigsten Features von Project Server 2013 Anpassung von Project Web App und Aktualisieren von Anwendungen, die für frühere Versionen von Project Server integriert sind. 
  
[Was die PSI enthält und nicht zu](what-the-psi-does-and-does-not-do.md) beschreibt Szenarios die PSI verwendet werden kann, und enthält Features, mit denen die PSI nicht ausführen kann. 
  
[Was das CSOM ist und nicht zu](what-the-csom-does-and-does-not-do.md) beschreibt Szenarios das CSOM verwendet werden kann, und enthält Features, mit denen das CSOM nicht ausführen kann. 
  
### <a name="topics-not-covered"></a>Themen nicht behandelt.

Die Artikel im Abschnitt *Architektur und Programmierbarkeit* Features des Project-Desktopclients (Project Standard 2013 und Project Professional 2013) oder Project Web App nicht dokumentiert. 
  
Visual Basic für Applikationen (VBA) Hilfe ist in den Visual Basic-Editor in Project Standard und Project Professional verfügbar.
  
## <a name="see-also"></a>Siehe auch
<a name="bk_addresources"> </a>

- [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md)
    
- [Erste Schritte beim Entwickeln von Project Server-Workflows](getting-started-developing-project-server-workflows.md)
    

