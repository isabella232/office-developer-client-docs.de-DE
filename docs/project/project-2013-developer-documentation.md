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
- sdk, project 2013,Project 2013, SDK-Übersicht
ms.assetid: f66adbf1-5cb5-4dd0-be08-45e1c88c010c
description: Hier finden Sie Dokumentationen, Codebeispiele, Anleitungen und Programmierungsreferenzen, die beim Erstellen von Apps für den Office Store oder beim Erstellen eines privaten App-Katalogs behilflich sind. Sie helfen zudem beim Anpassen und Integrieren von Project Server und der Project-Clients mit einer großen Vielfalt an anderen Desktop- und Geschäftsanwendungen für das Enterprise-Projektmanagement.
localization_priority: Priority
ms.openlocfilehash: cb4dd31a76b897bb5dba39e6b20d0a238bd95293
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707822"
---
# <a name="project-2013-developer-documentation"></a>Project 2013-Entwicklerdokumentation

Hier finden Sie Dokumentationen, Codebeispiele, Anleitungen und Programmierungsreferenzen, die beim Erstellen von Apps für den Office Store oder beim Erstellen eines privaten App-Katalogs behilflich sind. Sie helfen zudem beim Anpassen und Integrieren von Project Server und der Project-Clients mit einer großen Vielfalt an anderen Desktop- und Geschäftsanwendungen für das Enterprise-Projektmanagement.
  
Willkommen beim Microsoft Project 2013 Software Development Kit (SDK). Das SDK enthält Dokumentationen, Codebeispiele, Anleitungen und Programmierungsreferenzen, die beim Erstellen von Apps für einen öffentlichen Store oder beim Erstellen eines privaten App-Katalogs behilflich sind. Sie helfen zudem beim Anpassen und Integrieren von Project Server und der Project-Clients mit einer großen Vielfalt an anderen Desktop- und Geschäftsanwendungen für das Enterprise-Projektmanagement.
  
> [!NOTE]
> Project Server 2013 basiert auf der SharePoint Server 2013- Plattform; Project 2013 weist größtenteils dieselbe Infrastruktur wie die anderen Office 2013-Anwendungen auf. Dokumentation zum Modell für SharePoint-Add-Ins, zu SharePoint-basierten Workflows, zu Webparts, zur Entwicklung mit anderen SharePoint-Features und Dokumentation von Office-Add-Ins finden Sie unter [SharePoint Add-Ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) und [Office Add-Ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins). 
  
## <a name="introduction-to-the-project-sdk"></a>Einführung in das Project-SDK
<a name="pj15_Welcome_IntroToSDK"> </a>

Project Server 2013 ist eine Plattform zum Erstellen lokaler oder cloudbasierter Projektmanagementlösungen für Unternehmen und zum Erstellen von Apps, die Endbenutzer über einen öffentlichen Store oder einen privaten App-Katalog erkunden und erwerben können. Die Project Server 2013-Architektur basiert auf der Plattform, die in Microsoft Office Project Server 2007 eingeführt wurde, und umfasst viele Ergänzungen und Verbesserungen. Zu den neuen Features gehört ein clientseitiges Objektmodell (CSOM), um Zugriff auf Project Online, einen OData-Dienst für Onlinezugriff auf Project Server-Berichtsdaten, Remoteereignisempfänger, Workflowarchitektur, die auf Version 4 von Windows Workflow Foundation (WF4) basiert, und Office-Add-Ins zu ermöglichen, eine gängige Architektur für Aufgabenbereichserweiterungen in Microsoft Office 2013-Clientanwendungen.
  
Eine wesentliche Änderung in Project Server 2013 ist die Verwendung einer einzigen Datenbank anstelle der Entwurfs-, Veröffentlichungs-, Archiv- und Berichtsdatenbanken in Project Server 2010. Weitere Informationen zu neuen Features und veralteten Features finden Sie unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md). Informationen zu Änderungen in der Project Server-Plattform finden Sie unter [Project Server 2013-Architektur](project-server-2013-architecture.md). Eine Übersicht über die Entwicklungsplattform, die in Project Server 2010 vorhanden ist und auf der Project Server 2013 basiert, finden Sie unter [Erste Schritte mit der Entwicklung für Project 2010](https://msdn.microsoft.com/library/gg607685.aspx) auf MSDN. 
  
Projekt Server 2013 basiert auf dem Microsoft .NET Framework 4 und auf Microsoft SharePoint Server 2013. Die Artikel und Beispiele in diesem SDK bieten einen Startplatz für das Entwickeln benutzerdefinierter Lösungen und Apps. Sie zielen nicht auf alle Programmierbarkeitsfeatures von Project Server oder Project Professional ab. Das [Project Developer Center](https://msdn.microsoft.com/library/4e5245c3-4891-455b-b321-1819cdd77247.aspx) enthält Links zu Artikeln, Blogs, Videos, Webcasts, visuellen Anleitungen und anderen Ressourcen, die mit Project in Zusammenhang stehen. 
  
Das Project 2013-SDK enthält Entwicklerinformationen für Project Server 2013, Project Web App, Project Professional 2013 und Project Standard 2013. Die SDK-Artikel sind ausgelegt, um Entwickler und Administratoren beim Evaluieren von Project und Project Server in Bezug auf die Erweiterbarkeit und die Planung benutzerdefinierter Lösungen zu unterstützen.
  
### <a name="feedback"></a>Feedback
<a name="pj15_Welcome_Feedback"> </a>

Wir freuen uns über Ihr Feedback. In den Onlinethemen auf MSDN können Sie Kommentare und Codebeispiele hinzufügen oder die Inhalte im Abschnitt **Communityinhalt** am Ende jeder Seite als Fehler kennzeichnen. Wenn Sie das Project 2013-SDK-Download installieren, verfügen die lokalen Dokumentationsartikel über den Link *Feedback senden*, der sich unter dem Titel befindet. Während Sie das SDK lesen, können Sie jederzeit auf den Link klicken, um eine E-Mail an das SDK-Team zu senden. Sie können Korrekturen, eine Anforderung zur Klärung oder für ein Codebeispiel und andere Kommentare senden; damit helfen Sie uns, unsere Inhalte zu verbessern. 
  
### <a name="download"></a>Download
<a name="pj15_Welcome_Download"> </a>

Der Download für das Project 2013-SDK ist im [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20) ( `https://www.microsoft.com/en-us/download/details.aspx?id=30435%20`) verfügbar. Der Download umfasst Project2013SDK.HxS (die Datei, die diesen Artikel enthält), verwandte Codebeispiele, weitervertreibbare Assemblys und andere Ressourcen. Im Project 2013-SDK ist noch nicht der Verweis auf die Berichts-DataTables enthalten.
  
### <a name="whats-new-in-the-project-sdk"></a>Neuigkeiten im Project-SDK
<a name="pj15_Welcome_WhatsNew"> </a>

Die Hauptfunktion des Project 2013-SDKs ist eine Übersicht über die Programmierbarkeit und Dokumentation des CSOM und verwandter Features zum Erstellen von Apps, der PSI-Dienste (Project Server Interface) und Aufgabenbereich-Apps für Project Professional 2013. Das Project 2013-SDK umfasst Beispiele mit schrittweisen Anleitungen für wesentliche Bereiche der Anpassung von Project Server 2013 und der Project-Clients (Project Standard 2013, Project Professional 2013 und Project Web App). Die Dokumentation ist unvollständig. Weitere Inhalte werden in späteren Versionen hinzugefügt. 
  
Die zugrunde liegende Technologie für die Netzwerkkommunikation ist Windows Communication Foundation (WCF) in Project Server 2013, einschließlich Cloudszenarios, die das clientseitige Objektmodell von Project Server und die lokale Entwicklung mithilfe der PSI verwenden. Die alten ASMX-Webdienstverweise basieren auch auf der WCF-Architektur. Für das Festlegen eines Verweises auf einen PSI-Webdienst (ASMX-Datei) in Project Server 2013 muss die `?wsdl`-URL-Option an den Pfad angefügt werden. Zum Beispiel: `https://ServerName/ProjectServerName/_vti_bin/PSI/Resource.asmx?wsdl`.
  
> [!NOTE]
> Es wird empfohlen, dass Sie, wenn möglich, das CSOM für Anwendungen (sowohl lokal als auch in der Cloud) verwenden, obwohl es nur die am häufigsten verwendeten Project Server-Features abdeckt. Die ASMX-Schnittstelle für die PSI ist zwar in Project Server 2013 noch verfügbar, ist aber veraltet. Für lokale Anwendungen, die Vollzugriff auf die PSI erfordern, sollten Sie die WCF-Schnittstelle für die PSI anstelle der ASMX-Schnittstelle verwenden. 
  
Die Entwicklung auf einem Windows 7-Computer wird unterstützt, indem Sie die CSOM-Assemblys für Project Server 2013 und für SharePoint Server 2013 auf den Entwicklungscomputer kopieren. Der SDK-Download enthält die CSOM-Assemblys für Project Server und eine Weiterverteilungslizenz. Informationen zum Abrufen der SharePoint-Assemblys finden Sie unter [SharePoint Server 2013 Client Components SDK](https://www.microsoft.com/en-us/download/details.aspx?id=35585).
  
Für die Entwicklung mit den WCF-Diensten können Sie einen Verweis auf eine PSI-Proxyassembly festlegen oder der Lösung PSI-Proxydateien hinzufügen. Sie können über einen Remotecomputer in derselben Domäne direkte Verweise auf die Project Server-Front-End-ASMX-Webdienste festlegen, oder eine Proxyassembly oder Proxydateien verwenden. Der SDK-Download enthält Proxydateien für die WCF-Dienste und die ASMX-Webdienste sowie Skripts für das Erstellen der Proxyassemblys und für das Generieren der aktualisierten Proxydateien.
  
In Project Server 2013 können Sie deklarative Project Server-Workflows mithilfe von Microsoft SharePoint Designer 2013 für die lokale Verwendung und die Onlineverwendung erstellen. SharePoint Designer 2013 verwendet die Eigenschaften und Methoden der Workflowaktivität des CSOM. Die Entwicklung und Bereitstellung von Visual Studio 2012-Lösungen, die Project Server-Webparts enthalten, oder Anpassungen von Project Web App werden nur auf einem Computer mit Project Server unterstützt.
  
Eine Übersicht über die neuen Programmierbarkeitsfeatures und die veralteten Features in in Project Server 2013 finden Sie unter [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md). Eine andere umfassende Änderung in Project Server 2013 betrifft die Verwendung von WF4-basierten Workflows zum Verwalten der Erstellung und Genehmigung von Projektvorschlägen, die auf Enterprise-Projektvorlagen basieren. 
  
Die neuen Themen umfassen Folgendes:
  
- [Erstellen eines auf SharePoint gehosteten Project Server-Add-Ins](create-a-sharepoint-hosted-project-server-add-in.md) zeigt die Verwendung von Visual Studio für die Remoteentwicklung einer App, die mit Project Server 2013 und Project Online verwendet werden kann. 
    
- [Project Server 2013-Architektur](project-server-2013-architecture.md) erläutert die wichtigsten neuen Features der Project Server-Plattform. 
    
- [Erste Schritte mit dem JavaScript-Objektmodell in Project Server 2013](getting-started-with-the-project-server-2013-javascript-object-model.md) zeigt das Entwickeln von Webanwendungen, die auf Project Server zugreifen können. 
    
- [Erste Schritte mit dem Project Server-CSOM und .NET](getting-started-with-the-project-server-csom-and-net.md) zeigt die Verwendung des clientseitigen Objektmodells zum Entwickeln von Anwendungen anstelle der Verwendung der PSI-Dienste. 
    
- [Aufgabenbereich-Apps für Project Professional](task-pane-add-ins-for-project.md) führt Office-Add-Ins entsprechend der Anwendung in Project 2013 ein. Das Office 2013-SDK umfasst Artikel, in denen gezeigt wird, wie Aufgabenbereich-Apps für Project und die anderen Office 2013-Clients entwickelt werden. 
    
- [Erstellen eines Project Server-Workflows für das Bedarfsmanagement](create-a-project-server-workflow-for-demand-management.md) zeigt, wie SharePoint Designer 2013 zum Erstellen von Project Server-Workflows verwendet werden kann. 
    
- [ProjectData – OData-Dienstreferenz für Project](https://msdn.microsoft.com/library/office/jj163015.aspx) enthält eine Übersicht der OData-Schnittstelle für die Project Server-Berichterstellung sowie XML-Referenzthemen für den **ProjectData**-Dienst. 
    
Themen im **Microsoft.ProjectServer.Client**-Namespace und neue Methoden in den PSI-Diensten weisen nur eine minimale Dokumentation auf. Die meisten Referenzthemen für die PSI-Dienste sind seit der Version vom Juli 2011 des Project 2010-SDKs unverändert. 
  
### <a name="future-sdk-releases"></a>Künftige SDK-Versionen
<a name="pj15_Welcome_FutureReleases"> </a>

Das Project 2013-SDK wird mit neuen Artikeln und Referenzinhalten für die Version bei allgemeiner Verfügbarkeit aktualisiert.
  
## <a name="sections-in-the-project-sdk"></a>Abschnitte im Project-SDK
<a name="pj15_Welcome_SectionsInTheSDK"> </a>

Im Project 2013-SDK sind zwei Abschnitte auf oberster Ebene vorhanden:
  
- Der Abschnitt [Konzept und Anleitungen für Project](project-conceptual-and-how-to-articles.md) enthält Übersichten über die wichtigsten Features und Artikel mit schrittweisen Prozeduren für die Entwicklung. 
    
- Der Abschnitt [Project Server 2013-Klassenbibliothek und Webdienstverweis](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) dokumentiert das Objektmodell der öffentlichen Assemblys, die Microsoft.ProjectServer.Client.dll-Assembly für das CSOM und die PSI-Dienste. 
    
Der Abschnitt **Konzept und Anleitungen** enthält Folgendes: 
  
- [Was ist neu und was ist für Entwickler](updates-for-developers-in-project-2013.md) beschreibt die wichtigsten neuen Programmierbarkeitsfeatures und veraltete Features in Project 2013. 
    
- [Projekt-Übersicht für Entwickler](https://msdn.microsoft.com/library/8da91ab0-af4f-429f-8241-490600e3f7bd%28Office.15%29.aspx) enthält Artikel über die Project Server-Architektur, Artikel mit den ersten Schritten für die Entwicklung mit dem CSOM, Informationen über neue Features in VBA für Project und einen Verweis auf das Office 2013-SDK, das Themen über das Entwickeln von Aufgabenbereich-Apps für Project Professional 2013 enthält. 
    
- [Project-Programmieraufgaben](project-programming-tasks.md) enthält Anleitungen über das Erstellen von Apps für Project Server mithilfe von JavaScript mit dem CSOM und das Erstellen von Projektvorschlägen und Workflows für das Projektbedarfsmanagement. 
    
- [Project 2013-Programmierreferenzen](project-2013-programming-references.md) enthält eine Einführung in die PSI-Referenz für Project Server 2013, Informationen über Project Server-Fehlercodes und die OData-Schemareferenz für den **ProjectData**-Dienst. 
    
> [!NOTE]
>  Nachfolgend finden Sie die Anforderungen zum Entwickeln und Bereitstellen von EPM-Lösungen und -Apps aus dem öffentlichen Office Store, die in Project Server 2013 integriert werden können: > Sie müssen das .NET Framework 4 oder das .NET Framework 4.5 auf dem Entwicklungscomputer und auf den Bereitstellungscomputern installieren. Um zu ermitteln, ob die korrekte Version installiert ist, öffnen Sie in der Windows-Systemsteuerung **Programme und Funktionen**. >  Visual Studio 2012 installiert und verwendet das .NET Framework 4.5. Wenn Sie ein Visual Studio-Projekt erstellen, können Sie entweder **.NET Framework 4.0** oder **.NET Framework 4.5** in der Dropdownliste des Dialogfelds **Neues Projekt** auswählen. Sie können auch das **Zielframework** auf der Registerkarte **Anwendung** des Project-Fensters **Eigenschaften** auswählen. >  Sie können Visual Studio 2010 für Anwendungen verwenden, die das CSOM oder die PSI verwenden, und für Project Aufgabenbereich-Apps. Visual Studio 2010 enthält jedoch keine Office-Add-Ins-Vorlagen, Office-Entwicklungstools oder SharePoint-Entwicklungstools für Office 2013. Informationen zum Herunterladen von Visual Studio 2012 und Web Platform Installer (WebPI), der die Office- und SharePoint-Entwicklungstools umfasst, finden Sie unter [Downloads für Apps für Office und SharePoint](https://msdn.microsoft.com/office/apps/fp123627). > Es wird empfohlen, dass Sie benutzerdefinierte Lösungen in einer Testumgebung entwickeln. Wenn Sie Lösungen für die aktuellen Builds von Project Server 2013 und Project 2013 entwickeln, sollten diese mit aktualisierten Verweisen neu kompiliert werden; möglicherweise sind weitere Änderungen erforderlich, damit diese mit höheren Versionen funktionieren. Lösungen, die für eine Vorabversion entwickelt wurden, funktionieren möglicherweise nicht mit der veröffentlichten Version. 
  
## <a name="see-also"></a>Siehe auch
<a name="pj15_Welcome_AR"> </a>

- [Updates für Entwickler in Project 2013](updates-for-developers-in-project-2013.md)
    
- [Project Server 2013-Architektur](project-server-2013-architecture.md)
    
- [Project 2013-SDK-Download](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [SharePoint Server 2013 Client Components SDK](https://www.microsoft.com/en-us/download/details.aspx?id=35585)
    
- [Project für Entwickler](https://msdn.microsoft.com/project)
    
- [Office-Entwicklerdokumentation](https://msdn.microsoft.com/office)
    
- [Erste Schritte mit der Entwicklung für Project 2010](https://msdn.microsoft.com/library/gg607685.aspx)
    
- [Konventionen in diesem Dokument](https://msdn.microsoft.com/library/6b38829f-1a9d-4fb6-ad3b-01182628080a.aspx)
    
- [Barrierefreiheit in SharePoint 2013](https://msdn.microsoft.com/library/jj841103.aspx)
    
- [Barrierefreiheit in Microsoft Office 365](https://www.microsoft.com/enable/products/office365/)
    
- [Microsoft Online-Datenschutzhinweis](https://privacy.microsoft.com/de-DE/privacystatement)
    

