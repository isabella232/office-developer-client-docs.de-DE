---
title: Aufgabenbereich-Add-Ins für Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project Standard 2013 und Project Professional 2013 beide unterstützen Aufgabenbereich-Office-Add-Ins. Sie können Aufgabenbereich-Add-Ins verwenden, um Projekt-, Vorgangs-, Ressourcen-und Ansichtsdaten in ein Projekt mit anderen Office 2013-Clientanwendungen, SharePoint-Anwendungen, Webparts, anderen Webseiten und externen Daten zu integrieren.
ms.openlocfilehash: 26942cab1d1b127872a230a46fbc6242ab27b754
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330016"
---
# <a name="task-pane-add-ins-for-project"></a>Aufgabenbereich-Add-Ins für Project

Project Standard 2013 und Project Professional 2013 beide unterstützen Aufgabenbereich-Office-Add-Ins. Sie können Aufgabenbereich-Add-Ins verwenden, um Projekt-, Vorgangs-, Ressourcen-und Ansichtsdaten in ein Projekt mit anderen Office 2013-Clientanwendungen, SharePoint-Anwendungen, Webparts, anderen Webseiten und externen Daten zu integrieren.
  
Office-Add-Ins ist ein Erweiterbarkeitsmodell, das in mehreren Office 2013-Clientanwendungen unterstützt wird. Die vollständige Add-in-Plattform umfasst Kontext-, Inhalts-und Aufgabenbereich-Add-in-Typen. Outlook 2013 unterstützt e-Mail-Add-Ins, die eine Webseite in einer e-Mail-Nachricht oder einem Kalendertermin Element anzeigen können, das sich auf Inhalte im Element bezieht. Word 2013 und Excel 2013 unterstützen Inhalts-Add-Ins, die eine Webseite als eingebetteten Inhalt in einem Dokument anzeigen können. Word 2013, Excel 2013 und Project Professional 2013 unterstützen Aufgabenbereich-Add-Ins, die eine Webseite in einem Aufgabenbereich anzeigen können, in der sich der Inhalt mit Kontextinformationen im Projekt zusammenhängt.
  
Beispielsweise kann ein Projekt-Add-in Daten im aktiven Projekt zusammenfassen und zusätzliche Daten zu einer ausgewählten Aufgabe oder Ressource anzeigen. Verwandte Daten im Add-in können aus einer externen Quelle wie einer SharePoint-Liste, Berichtstabellen in der Project Server-Datenbank, einem Webdienst oder einer anderen Unternehmensanwendung stammen. Ein Aufgabenbereich-Add-in kann mit HTML 5, JavaScript, JQuery und anderen JavaScript-Bibliotheken entwickelt werden. Ein Aufgabenbereich-Add-in unterstützt nicht direkt ActiveX-, Silverlight-oder Flash-Komponenten. Obwohl ein Office-Add-in ein **iframe** -Element für den Zugriff auf eine serverseitige Webanwendung verwenden kann, die ASP.net und die .net Framework 4,5-Bibliothek verwendet, wird diese Art von Lösung nicht empfohlen oder unterstützt. Das Add-in kann zum lokalen Speichern von Daten oder zum Schreiben von Daten an einen externen Speicherort entwickelt werden. 
  
> [!NOTE]
> Aufgabenbereich-Projekt-Add-Ins können mithilfe der OAuth-Authentifizierung auf Daten aus Project Online zugreifen. Mit Project Professional 2013 können Sie Aufgabenbereich-Add-ins entwickeln, die auf lokale Installationen von Project Server 2013 und lokal oder Online SharePoint 2013 zugreifen. Weitere Informationen finden Sie unter [Verbinden eines Project-Aufgabenbereich-Add-Ins mit PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) im Project Programmibility-Blog. > Project Standard 2013 unterstützt keine direkte Integration mit Project Server-Daten oder SharePoint-Aufgabenlisten, die mit Project Server synchronisiert werden. 
  
Weitere Informationen zu Add-Ins für Office 2013 finden Sie unter [Office-und SharePoint-Add-ins](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29). 
  
## <a name="developing-task-pane-add-ins"></a>Entwickeln von Aufgabenbereich-Add-ins

Die Entwicklerdokumentation für Office-und SharePoint-Add-Ins enthält umfassende Artikel und Verweise. Eine Einführung in die Entwicklung von Add-Ins für Project Professional 2013 und andere Office 2013-Clientanwendungen sowie für die JavaScript-Referenz und XML-Manifest-Referenz finden Sie unter [Office-Add-ins](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29).
  
Der Project 2013 SDK-Download umfasst das **Project OM-Test** Beispiel-Add-in, das zeigt, wie die GUID eines Vorgangs, einer Ressource und einer Ansicht abgerufen wird, wie Eigenschaften des aktiven Projekts abgerufen werden und wie der Ereignishandler für Vorgangs-, Ressourcen-oder Ansichtsauswahl Änderungen festgelegt wird. Wenn Sie das SDK und die Beispiele in der Datei Project2013SDK. msi extrahieren und installieren, finden `\Samples\Apps\Copy_to_AppSource_FileShare` Sie weitere Informationen unter `\Samples\Apps\Copy_to_AppManifests_FileShare` Verzeichnis. Das Datei jsomcall. html-Beispiel verwendet JavaScript-Funktionen in der Datei "Office. js" und in der Datei "Project-15. js", die im Download enthalten sind. Mithilfe der entsprechenden Debugdateien (office.debug.js und project-15.debug.js) können Sie die Funktionen prüfen. 
  
Das **HelloProject_OData** -Beispiel-Add-in für Project Professional 2013 wurde mit Visual Studio 2012 entwickelt. Das Add-in verwendet eine REST-Abfrage des **ProjectData** -Diensts, um Berichtsdaten für Projektkosten und andere Informationen abzurufen, und vergleicht dann das aktuelle Projekt mit den Durchschnittswerten für alle Projekte in Project Web App. 
  
## <a name="see-also"></a>Siehe auch
<a name="bk_addresources"> </a>

- [Aufgabenbereich-Add-Ins für Project](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)
    
- [Verbinden eines Project-Aufgabenbereich-Add-Ins mit PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Project 2013 SDK-Download](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Office- und SharePoint-Add-Ins](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)
    
- [Office-Add-Ins](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
    

