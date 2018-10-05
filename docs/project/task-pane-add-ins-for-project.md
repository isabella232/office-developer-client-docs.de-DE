---
title: Aufgabenbereich-Add-Ins für Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project Standard 2013 und Project Professional 2013 unterstützen sowohl im Aufgabenbereich Office-Add-ins. Sie können Task Pane-add-ins zur Integration von Project, Aufgabe, Ressource verwenden und Anzeigen von Daten in einem Projekt mit anderen Office 2013-Clientanwendungen, SharePoint-Anwendungen, Webparts, andere Webseiten und externe Daten.
ms.openlocfilehash: 26942cab1d1b127872a230a46fbc6242ab27b754
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396015"
---
# <a name="task-pane-add-ins-for-project"></a>Aufgabenbereich-Add-Ins für Project

Project Standard 2013 und Project Professional 2013 unterstützen sowohl im Aufgabenbereich Office-Add-ins. Sie können Task Pane-add-ins zur Integration von Project, Aufgabe, Ressource verwenden und Anzeigen von Daten in einem Projekt mit anderen Office 2013-Clientanwendungen, SharePoint-Anwendungen, Webparts, andere Webseiten und externe Daten.
  
Office-Add-ins ist ein Modell der Erweiterbarkeit, die in Office 2013-Clientanwendungen unterstützt wird. Die vollständige-add-in-Plattform enthält kontextbezogene, Inhalte und task Pane-add-in Typen. Outlook 2013 unterstützt e-Mail-add-ins, die eine Webseite in einer e-Mail-Nachricht anzeigen können oder Kalender Terminelement, die Inhalte im Element zugeordnet ist. Word 2013 und Excel 2013 unterstützen Content-add-ins, die eine Webseite als eingebetteten Inhalt in einem Dokument anzeigen können. Word 2013, Excel 2013 und Project Professional 2013 unterstützen Aufgabe Bereich-add-ins, die eine Webseite in einem Aufgabenbereich anzeigen können, in dem der Inhalt Kontextinformationen innerhalb des Projekts verknüpft ist.
  
Beispiel kann eines Projekt-add-ins Zusammenfassen von Daten in das aktive Projekt und zusätzliche Daten über einen ausgewählten Vorgang oder eine Ressource anzeigen. Verwandte Daten in das Add-in können aus einer externen Quelle wie einer SharePoint-Liste reporting Tabellen in der Project Server-Datenbank, einem Webdienst oder einer anderen enterpriseanwendung stammen. Ein Task Pane-add-in kann mit 5 HTML, JavaScript, JQuery und anderen JavaScript-Bibliotheken entwickelt werden. Ein Task Pane-add-in unterstützt nicht direkt ActiveX, Silverlight oder Flash-Komponenten. Obwohl ein Office-Add-in ein **IFrame** -Element von Zugriff auf eine serverseitige Webanwendung, die ASP.NET und .NET Framework 4.5-Bibliothek verwendet mithilfe, ist dieser Art von Lösung nicht empfohlen oder unterstützt. Das Add-in kann zum Speichern von Daten lokal oder Schreiben von Daten in einem externen Standort entwickelt werden. 
  
> [!NOTE]
> Aufgabenbereich Projekt-Add-ins kann Daten aus Project Online mithilfe von OAuth-Authentifizierung zugreifen. Mit Project Professional 2013 können Sie Task Pane-add-ins entwickeln, die beide lokale Installationen von Project Server 2013 und lokalen oder online SharePoint 2013 zugreifen. [Herstellen einer Verbindung mit einer Aufgabenbereich-App für Projekt-add-in PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) im Blog Project-Programmibility beispielsweise angezeigt. > Project Standard 2013 unterstützt keine direkte Integration mit Project Server-Daten oder SharePoint-Aufgabenlisten, die mit Project Server synchronisiert werden. 
  
Weitere Informationen zu add-ins für Office 2013 finden Sie unter [Office und SharePoint-Add-ins](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29). 
  
## <a name="developing-task-pane-add-ins"></a>Entwickeln von Task Pane-add-ins

Entwicklerdokumentation für Office und SharePoint-Add-ins enthält umfassende Artikel und Referenzen. Eine Einführung in die Entwicklung-add-ins für Project Professional 2013 und andere Office 2013-Clientanwendungen sowie für die JavaScript-Referenz und XML-manifest (engl.) finden Sie unter [Office-Add-ins](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29).
  
Der Project 2013-SDK-Download enthält die **Project OM Test** Beispiel-add-in, die zeigt, wie Sie die GUID des eine Vorgangs-, Ressourcen- und Ansicht abrufen, das Abrufen der Eigenschaften des aktiven Projekts und zum Festlegen einer Vorgangs-, Ressourcen- oder SelectionChanged-Ereignishandler anzuzeigen. Wenn Sie extrahieren und installieren das SDK und die Beispiele in der Datei Project2013SDK.msi, finden Sie unter der `\Samples\Apps\Copy_to_AppSource_FileShare` Unterverzeichnis und die `\Samples\Apps\Copy_to_AppManifests_FileShare` Unterverzeichnis. Im Beispiel JSOMCall.html verwendet JavaScript-Funktionen in der Datei office.js und Project-15.js-Datei, die im Download enthalten sind. Sie können die entsprechenden Debug-Dateien (office.debug.js und project-15.debug.js) verwenden, um die Funktionen zu untersuchen. 
  
**HelloProject_OData** Beispiel-add-in für Project Professional 2013 wurde mit Visual Studio 2012 entwickelt. Das Add-In wird eine REST-Abfrage für den **ProjectData** -Dienst verwendet, um Daten für Projektkosten und andere Informationen reporting erhalten möchten, und klicken Sie dann vergleicht des aktuellen Projekts mit die Durchschnittswerte für alle Projekte in Project Web App. 
  
## <a name="see-also"></a>Siehe auch
<a name="bk_addresources"> </a>

- [Aufgabenbereich-Add-Ins für Project](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)
    
- [Herstellen einer Verbindung mit einem Aufgabenbereich Projekt-add-in PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Project 2013 SDK-Download](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Office- und SharePoint-Add-Ins](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)
    
- [Office-Add-Ins](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
    

