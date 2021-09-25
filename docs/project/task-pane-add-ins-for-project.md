---
title: Aufgabenbereich-Add-Ins für Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project Standard 2013 und Project Professional 2013 unterstützen beide Aufgabenbereich-Office-Add-Ins. Sie können Aufgabenbereich-Add-Ins verwenden, um Projekt-, Aufgaben-, Ressourcen- und Ansichtsdaten in ein Projekt mit anderen Office 2013-Clientanwendungen, SharePoint Anwendungen, Webparts, anderen Webseiten und externen Daten zu integrieren.
ms.openlocfilehash: 826009a2359dd5d9b97a702674206f3a533b6a51
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566080"
---
# <a name="task-pane-add-ins-for-project"></a>Aufgabenbereich-Add-Ins für Project

Project Standard 2013 und Project Professional 2013 unterstützen beide Aufgabenbereich-Office-Add-Ins. Sie können Aufgabenbereich-Add-Ins verwenden, um Projekt-, Aufgaben-, Ressourcen- und Ansichtsdaten in ein Projekt mit anderen Office 2013-Clientanwendungen, SharePoint Anwendungen, Webparts, anderen Webseiten und externen Daten zu integrieren.
  
Office Add-Ins sind ein Erweiterungsmodell, das in mehreren Office 2013-Clientanwendungen unterstützt wird. Die vollständige Add-In-Plattform enthält Kontext-, Inhalts- und Aufgabenbereich-Add-In-Typen. Outlook 2013 unterstützt Mail-Add-Ins, die eine Webseite innerhalb einer E-Mail-Nachricht oder eines Kalenderterminelements anzeigen können, die sich auf Inhalte im Element beziehen. Word 2013 und Excel 2013 unterstützen Inhalts-Add-Ins, die eine Webseite als eingebetteten Inhalt in einem Dokument anzeigen können. Word 2013, Excel 2013 und Project Professional 2013 unterstützen Aufgabenbereich-Add-Ins, die eine Webseite in einem Aufgabenbereich anzeigen können, in dem der Inhalt mit Kontextinformationen innerhalb des Projekts verknüpft ist.
  
Beispielsweise kann ein Project-Add-In Daten im aktiven Projekt zusammenfassen und zusätzliche Daten zu einem ausgewählten Vorgang oder einer ausgewählten Ressource anzeigen. Verwandte Daten im Add-In können aus einer externen Quelle stammen, z. B. aus einer SharePoint Liste, Berichtstabellen in der Project Serverdatenbank, einem Webdienst oder einer anderen Unternehmensanwendung. Ein Aufgabenbereich-Add-In kann mit HTML 5, JavaScript, JQuery und anderen JavaScript-Bibliotheken entwickelt werden. Ein Aufgabenbereich-Add-In unterstützt nicht direkt ActiveX-, Silverlight- oder Flash-Komponenten. Obwohl ein Office-Add-In ein **IFrame-Element** verwenden kann, um auf eine serverseitige Webanwendung zuzugreifen, die ASP.NET und die .NET Framework 4.5-Bibliothek verwendet, wird diese Art von Lösung nicht empfohlen oder unterstützt. Das Add-In kann entwickelt werden, um Daten lokal zu speichern oder Daten an einen externen Speicherort zu schreiben. 
  
> [!NOTE]
> Aufgabenbereich-Project-Add-Ins können mithilfe der OAuth-Authentifizierung auf Daten aus Project Online zugreifen. Mit Project Professional 2013 können Sie Aufgabenbereich-Add-Ins entwickeln, die sowohl auf lokale Installationen von Project Server 2013 als auch auf lokale oder online SharePoint 2013 zugreifen. Weitere Informationen finden Sie beispielsweise unter [Verbinden eines Project Aufgabenbereich-Add-Ins mit PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) im Blog Project Programmierbarkeit. > Project Standard 2013 unterstützt keine direkte Integration mit Project Serverdaten oder SharePoint Aufgabenlisten, die mit Project Server synchronisiert werden. 
  
Weitere Informationen zu Add-Ins für Office 2013 finden Sie unter [Office und SharePoint Add-Ins.](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29) 
  
## <a name="developing-task-pane-add-ins"></a>Entwickeln von Aufgabenbereich-Add-Ins

Die Entwicklerdokumentation für Office und SharePoint-Add-Ins enthält umfassende Artikel und Referenzen. Eine Einführung in die Entwicklung von Add-Ins für Project Professional 2013 und andere Office 2013-Clientanwendungen sowie die JavaScript-Referenz und xml-Manifestreferenz finden Sie unter [Office Add-Ins.](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
  
Der Project 2013 SDK-Download enthält das Project OM Test-Beispiel-Add-In, das zeigt, wie die GUID eines Vorgangs, einer Ressource und einer Ansicht abgerufen wird, wie Eigenschaften des aktiven Projekts abgerufen werden und wie ein Vorgang, eine Ressource oder ein Ansichtsauswahl-Ereignishandler festgelegt wird.  Wenn Sie das SDK und Beispiele in der Project2013SDK.msi-Datei extrahieren und installieren, lesen Sie das  `\Samples\Apps\Copy_to_AppSource_FileShare` Unterverzeichnis und das  `\Samples\Apps\Copy_to_AppManifests_FileShare` Unterverzeichnis. Im JSOMCall.html Beispiel werden JavaScript-Funktionen in der office.js datei und project-15.js-Datei verwendet, die im Download enthalten sind. Mithilfe der entsprechenden Debugdateien (office.debug.js und project-15.debug.js) können Sie die Funktionen prüfen. 
  
Das  HelloProject_OData-Beispiel-Add-In für Project Professional 2013 wurde mit Visual Studio 2012 entwickelt. Das Add-In verwendet eine  REST-Abfrage des ProjectData-Diensts, um Berichtsdaten für Projektkosten und andere Informationen abzurufen, und vergleicht dann das aktuelle Projekt mit den Durchschnittswerten für alle Projekte in Project Web App. 
  
## <a name="see-also"></a>Siehe auch
<a name="bk_addresources"> </a>

- [Aufgabenbereich-Add-Ins für Project](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)
    
- [Verbinden eines Project Aufgabenbereich-Add-Ins mit PWA](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Project 2013 SDK-Download](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Office- und SharePoint-Add-Ins](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)
    
- [Office-Add-Ins](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
    

