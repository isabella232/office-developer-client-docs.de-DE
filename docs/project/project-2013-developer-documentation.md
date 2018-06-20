---
title: Project 2013-Entwicklerdokumentation
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
f1_keywords:
- Project
- Project 2013
- Project 2013 SDK
- Project programmability
- Project SDK
- SDK
- SDK Project
keywords:
- Übersicht über Project 2013, Project 2013-SDK-SDK
localization_priority: Normal
ms.assetid: f66adbf1-5cb5-4dd0-be08-45e1c88c010c
description: Hier finden Sie Dokumentation, Codebeispiele, Artikel mit Anleitungen und Programmierreferenzen zum Entwickeln von apps für den Office Store oder privaten app-Katalog und zum Anpassen und Integrieren von Project Server und Project-Clients mit einer Vielzahl von anderen Desktop- und business Anwendungen für Enterprise Projektmanagement.
ms.openlocfilehash: 490b5bd2fcbe2f92653b6ebc84d36e5c28cdc8c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796303"
---
# <a name="project-2013-developer-documentation"></a>Project 2013-Entwicklerdokumentation

Hier finden Sie Dokumentation, Codebeispiele, Artikel mit Anleitungen und Programmierreferenzen zum Entwickeln von apps für den Office Store oder privaten app-Katalog und zum Anpassen und Integrieren von Project Server und Project-Clients mit einer Vielzahl von anderen Desktop- und business Anwendungen für Enterprise Projektmanagement.
  
Willkommen Sie bei der Microsoft Project 2013 Software Development Kit (SDK). Das SDK enthält Dokumentation, Codebeispiele, Artikel mit Anleitungen und Programmierreferenzen zum Entwickeln von apps für einen öffentlichen oder privaten app-Katalog und zum Anpassen und Integrieren von Project Server und den Project-Clients mit einer Vielzahl von anderen Desktop und Geschäftsanwendungen für Enterprise Projektmanagement.
  
> [!NOTE]
> Projektserver 2013 basiert auf der Plattform für SharePoint Server 2013 und Project 2013 enthält einen Großteil der gleichen Infrastruktur als andere Office 2013-Anwendungen. Eine Dokumentation der einzelnen Details des Modells für SharePoint-Add-ins, SharePoint-basierten Workflows finden Sie unter Webparts, Entwicklung mit anderen SharePoint-Features und eine Dokumentation der Office-Add-ins, [Apps für Office und SharePoint](http://msdn.microsoft.com/en-us/library/fp161507%28office.15%29.aspx). 
  
## <a name="introduction-to-the-project-sdk"></a>Einführung in das Project-SDK
<a name="pj15_Welcome_IntroToSDK"> </a>

Projektserver 2013 ist eine Plattform für die Erstellung von lokalen oder cloudbasierten Enterprise Project Management-Lösungen und zum Erstellen von apps, die Endbenutzer erkennen und über einen öffentlichen oder privaten app-Katalog erwerben kann. Die Project Server 2013-Architektur basiert auf der Plattform mit vielen Erweiterungen und Verbesserungen in Microsoft Office Project Server 2007 eingeführt. Die neuen Features umfassen ein Client-seitigen Objektmodell (CSOM) zum Aktivieren des Zugriffs auf Project Online, einen OData-Dienst für online-Zugriff auf Project Server-Daten, remote-Ereignisempfänger, Workflowarchitektur, die auf Version 4 der Windows-Workflow basiert reporting Foundation (WF4) und Office-Add-ins, die eine allgemeine Architektur für die Aufgabe Bereich Erweiterungen in Microsoft Office 2013-Clientanwendungen ist.
  
Eine wichtige Änderung in Project Server 2013 ist die Verwendung einer einzigen Datenbank anstelle der Datenbanken Entwurf, veröffentlicht, Archiv und Berichterstellung in Project Server 2010. Weitere Informationen zu neuen Features und veralteten Features finden Sie unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md). Informationen zu Änderungen in der Project Server-Plattform finden Sie unter [Architektur von Project Server 2013](project-server-2013-architecture.md). Eine Übersicht über die Entwicklungsplattform, vorhanden ist, in Project Server 2010 und Project Server 2013 ist auf der Grundlage finden Sie unter [Erste Schritte bei der Entwicklung für Project 2010](http://msdn.microsoft.com/en-us/library/gg607685.aspx) bei MSDN. 
  
Projektserver 2013 baut auf der Microsoft .NET Framework 4 und Microsoft SharePoint Server 2013. Die Artikel und die Beispiele in diesem SDK bieten einen Ausgangspunkt für die Entwicklung von benutzerdefinierten Lösungen und apps; Sie führen Sie alle Programmierbarkeit Features von Project Server oder Project Professional nicht behandelt. Das [Project Developer Center](http://msdn.microsoft.com/library/4e5245c3-4891-455b-b321-1819cdd77247.aspx) enthält Links zu Project Artikeln, Blogs, Videos, Webcasts, Artikel mit visuellen Anleitungen und andere Ressourcen. 
  
Project 2013-SDK umfasst Entwicklerinformationen für Project Server 2013, Project Web App, Project Professional 2013 und Project Standard 2013 für. SDK-Artikel dienen zur Hilfe für Entwickler und Administratoren Project und Project Server für die Erweiterbarkeit und Planen von benutzerdefinierten Lösungen bewerten.
  
### <a name="feedback"></a>Feedback
<a name="pj15_Welcome_Feedback"> </a>

Wir möchten von Ihnen zu hören. In den Themen online auf MSDN können Sie Kommentare, Codebeispiele, hinzufügen oder markieren den Inhalt als Fehler im Abschnitt **Community-Inhalte** am unteren Rand jeder Seite. Bei der Installation des Project 2013 SDK-Downloads haben die lokale Dokumentation Artikel jeder einen Link *Feedback senden* , der sich unterhalb des Titels befindet. Wählen Sie den Link zum Senden einer e-Mails an das Team der SDK, jederzeit in der Lesemoduslayout-SDK. Sie können Korrekturen, eine Anforderung für Klarstellung oder ein Codebeispiel oder sonstige Kommentare senden, und helfen Sie uns die stärkere Inhalte. 
  
### <a name="download"></a>Download
<a name="pj15_Welcome_Download"> </a>

Download des Project 2013 SDK steht im [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20) ( `https://www.microsoft.com/en-us/download/details.aspx?id=30435%20`). Der Download enthält die Project2013SDK.HxS (die Datei, die dieses Artikels), verwandte Codebeispiele, Assemblys und andere Ressourcen. Project 2013-SDK umfasst den Reporting Datentabellen Verweis noch nicht.
  
### <a name="whats-new-in-the-project-sdk"></a>Neuigkeiten im Project-SDK
<a name="pj15_Welcome_WhatsNew"> </a>

Die Hauptaufgabe des Project 2013 SDK ist eine Übersicht der Programmierbarkeit und eine Dokumentation der CSOM und verwandte Features für das Erstellen von apps, die Project Server Interface (PSI)-Diensten und Aufgabenbereich-apps für Project Professional 2013 bereitstellen. Project 2013 SDK enthält schrittweise Beispiele für wichtige Bereiche für die Anpassung von Project Server 2013 und die Project-Clients (Project Standard 2013, Project Professional 2013 und Project Web App). Die Dokumentation ist unvollständig. Weitere Inhalte zu wird in zukünftigen Versionen hinzugefügt. 
  
Die zugrunde liegende Technologie für die Kommunikation ist Windows Communication Foundation (WCF) in Project Server 2013, einschließlich Szenarien für die Cloud, die Project Server-CSOM und lokale-Entwicklung mithilfe der PSI verwenden. Der Vorversion ASMX Webdienstverweise basieren auch auf der WCF-Architektur. Festlegen eines Verweises auf einen Webdienst PSI (ASMX-Datei) in Project Server 2013 Anhängen erfordert die `?wsdl` URL-Option, um den Pfad. Beispielsweise `http://ServerName/ProjectServerName/_vti_bin/PSI/Resource.asmx?wsdl`.
  
> [!NOTE]
> Obwohl nur die am häufigsten verwendeten Project Server-Features behandelt, es wird empfohlen, dass Sie das CSOM nach Möglichkeit für Applikationen verwenden lokal und in der Cloud. Obwohl es in Project Server 2013 weiterhin verfügbar ist, ist die ASMX-Schnittstelle für die PSI veraltet. Für lokale-Anwendungen, die uneingeschränkten Zugriff auf die PSI erfordern, sollten Sie die WCF-Schnittstelle für die PSI, statt die ASMX-Schnittstelle verwenden. 
  
Kopieren die CSOM-Assemblys für Project Server 2013 und SharePoint Server 2013 auf dem Entwicklungscomputer wird Entwicklung auf einem Windows 7-Computer unterstützt. Der SDK-Download enthält die CSOM-Assemblys für Project Server und eine Lizenz Redistribution. Wenn Sie die SharePoint-CSOM Assemblys erhalten möchten, finden Sie unter [Client Components SDK für SharePoint Server 2013](http://www.microsoft.com/en-us/download/details.aspx?id=35585).
  
Für die Entwicklung mit den WCF-Diensten können Sie einen Verweis auf eine PSI-Proxyassembly festlegen oder der Lösung PSI-Proxydateien hinzufügen. Sie können über einen Remotecomputer in derselben Domäne direkte Verweise auf die Project Server-Front-End-ASMX-Webdienste festlegen, oder eine Proxyassembly oder Proxydateien verwenden. Der SDK-Download enthält Proxydateien für die WCF-Dienste und die ASMX-Webdienste sowie Skripts für das Erstellen der Proxyassemblys und für das Generieren der aktualisierten Proxydateien.
  
In Project Server 2013 können Sie erstellt deklarative Workflows für Project Server mit Microsoft SharePoint Designer 2013 für beide lokalen und online verwenden. SharePoint Designer 2013 verwendet die Workflow-Aktivitätseigenschaften und Methoden in der CSOM. Entwicklung und Bereitstellung von Visual Studio 2012-Lösungen, die Project Server-Webparts enthalten oder Anpassungen von Project Web App wird nur auf einem Project Server-Computer unterstützt.
  
Eine Übersicht über neue Features der Programmierbarkeit und veralteten Features in Project Server 2013 finden Sie unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md). Eine andere wichtige Änderung in Project Server 2013 ist die Verwendung von WF4-basierten Workflows zum Verwalten der Erstellung und Genehmigung von Projektvorschlägen, die auf unternehmensprojektvorlagen basieren. 
  
Die neuen Themen umfassen Folgendes:
  
- [Erstellen einer SharePoint gehosteten Project Server-add-ins](create-a-sharepoint-hosted-project-server-add-in.md) veranschaulicht, wie mithilfe von Visual Studio für die remote-Entwicklung einer App, die mit Project Server 2013 und Project Online verwendet werden können. 
    
- [Architektur von Project Server 2013](project-server-2013-architecture.md) erläutert die wichtigsten neuen Features von Project Server-Plattform. 
    
- [Erste Schritte mit dem Project Server 2013 JavaScript-Objektmodell](getting-started-with-the-project-server-2013-javascript-object-model.md) zeigt, wie Webanwendungen entwickeln, die Project Server zugreifen können. 
    
- [Erste Schritte mit dem Project Server-CSOM und .NET](getting-started-with-the-project-server-csom-and-net.md) veranschaulicht, wie das clientseitige Objektmodell zur Anwendungsentwicklung, anstatt der PSI-Dienste verwenden. 
    
- [Aufgabenbereich-apps für Project Professional](task-pane-add-ins-for-project.md) Einführung in Office-Add-ins für Project 2013 gelten. Das Office 2013-SDK enthält Artikel, die zeigen, wie Sie zum Entwickeln von apps für den Aufgabenbereich für Project und den anderen Office 2013-Clients. 
    
- [Erstellen eines Project Server-Workflows für das Bedarfsmanagement](create-a-project-server-workflow-for-demand-management.md) zeigt, wie SharePoint Designer 2013 zum Erstellen von Project Server-Workflows verwendet werden können. 
    
- [ProjectData - Projekt OData-Dienstverweises](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx) enthält eine Übersicht über den OData-Interface für Project Server-Berichtsdatenbank plus XML Referenzthemen für den **ProjectData** -Dienst. 
    
Themen im **Microsoft.ProjectServer.Client** -Namespace und neue Methoden in der PSI-Dienste haben nur minimale Dokumentation. Die meisten den Referenzthemen für die PSI-Dienste sind unverändert aus der Juli 2011 Version von Project 2010-SDK. 
  
### <a name="future-sdk-releases"></a>Künftige SDK-Versionen
<a name="pj15_Welcome_FutureReleases"> </a>

Project 2013-SDK werden mit neuen Artikeln und Referenzen herunter, die allgemeine Verfügbarkeit Version aktualisiert werden.
  
## <a name="sections-in-the-project-sdk"></a>Abschnitte im Project-SDK
<a name="pj15_Welcome_SectionsInTheSDK"> </a>

Es gibt zwei Abschnitte auf oberster Ebene in Project 2013 SDK:
  
- Im Abschnitt [Project Konzept- und Anleitungsthemen Artikel](project-conceptual-and-how-to-articles.md) enthält eine Übersicht der wichtigsten Features und Artikel mit schrittweise Verfahren für die Entwicklung. 
    
- Im Abschnitt [Project Server 2013 Class Library und Web-Dienstverweises](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) dokumentiert das Objektmodell der öffentlichen Assemblys, die Microsoft.ProjectServer.Client.dll-Assembly für das CSOM und der PSI-Dienste. 
    
Im Abschnitt **Konzept und Gewusst wie-Artikel** umfasst Folgendes: 
  
- [Neuigkeiten und was nicht mehr vorhandene für Entwickler (engl.)](updates-for-developers-in-project-2013.md) beschreibt die wichtigsten Features für neue Programmierbarkeit und veraltete Features in Project 2013. 
    
- [Übersicht über Project für Entwickler](http://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx) enthält Artikel zur Project Server-Architektur, Artikeln, in denen gezeigt, wie die ersten Schritte beim Entwickeln mit dem Clientobjektmodell, Informationen zu neuen Features in VBA für Projekt und einen Verweis auf das Office 2013 SDK enthält Themen zum Entwickeln von apps für den Aufgabenbereich für Project Professional 2013. 
    
- [Projekt Programmieraufgaben](project-programming-tasks.md) enthält Artikel mit Anleitungen zum Erstellen von apps für Project Server mithilfe von JavaScript mit dem CSOM, und Erstellen von Projektvorschlägen und Workflows für das bedarfsmanagement. 
    
- [Project 2013 programming Verweise](project-2013-programming-references.md) enthält eine Einführung in die PSI-Referenz für Project Server 2013, Informationen zu Project Server-Fehlercodes und der OData-Schemareferenz für den **ProjectData** -Dienst. 
    
> [!NOTE]
>  Im folgenden sind die Anforderungen zum Entwickeln und Bereitstellen der EPM-Lösungen und apps aus dem öffentlichen Office Store, die in Project Server 2013 integriert: > Sie müssen .NET Framework 4 oder .NET Framework 4.5 installieren, auf dem Entwicklungscomputer installiert und für die Bereitstellung Computer. Um zu bestimmen, ob die richtige Version installiert ist, öffnen Sie **Programme und Funktionen** in der Windows-Systemsteuerung. > Visual Studio 2012 installiert und .NET Framework 4.5 verwendet. Wenn Sie ein Visual Studio-Projekt erstellen, können Sie **.NET Framework 4.0** oder **NET Framework 4.5** in der Dropdown-Liste im Dialogfeld **Neues Projekt** auswählen. Sie können auch das **Zielframework** auf der Registerkarte **Anwendung** des Fensters **Eigenschaften** Projekt auswählen. > Können Visual Studio 2010 für Anwendungen, die die CSOM oder die PSI verwenden und für Project Aufgabenbereichs-apps. Visual Studio 2010 enthält jedoch nicht die Office-Add-ins Vorlagen, Office-Entwicklungstools oder SharePoint-Entwicklungstools für Office 2013. Informationen zum Herunterladen von Visual Studio 2012 und dem Webplattform-Installer (WebPI), die den Office und SharePoint-Entwicklungstools enthält, finden Sie [Downloads für Apps für Office und SharePoint](http://msdn.microsoft.com/en-us/office/apps/fp123627). > Es wird empfohlen, dass beim Entwickeln benutzerdefinierter Lösungen in einer testumgebung. Bei der Entwicklung von Lösungen für die aktuelle builds von Project Server 2013 und Project 2013, sie sollten mit aktualisierten Verweise erneut kompiliert werden, und möglicherweise zusätzliche Änderungen, spätere Versionen entwickelt. Lösungen für jede Vorabversion entwickelt wurden, funktionieren möglicherweise nicht mit die endgültige Produktversion. 
  
## <a name="see-also"></a>Siehe auch
<a name="pj15_Welcome_AR"> </a>

- [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md)
    
- [Architektur von Project Server 2013](project-server-2013-architecture.md)
    
- [Project 2013 SDK-Download](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [SharePoint Server 2013-Clientkomponenten – SDK](http://www.microsoft.com/en-us/download/details.aspx?id=35585)
    
- [Project für Entwickler](http://msdn.microsoft.com/project)
    
- [Office-Entwicklerdokumentation](http://msdn.microsoft.com/office)
    
- [Erste Schritte bei der Entwicklung für Project 2010](http://msdn.microsoft.com/en-us/library/gg607685.aspx)
    
- [Dokumentkonventionen](http://msdn.microsoft.com/library/6b38829f-1a9d-4fb6-ad3b-01182628080a.aspx)
    
- [Barrierefreiheit in SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj841103.aspx)
    
- [Eingabehilfen in Microsoft Office 365](http://www.microsoft.com/enable/products/office365/)
    
- [Anmerkung zur Microsoft online-Datenschutz](https://privacy.microsoft.com/en-us/privacystatement)
    

