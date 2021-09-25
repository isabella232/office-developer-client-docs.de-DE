---
title: JavaScript-Bibliothek und REST-Referenz für Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: Die JavaScript-Bibliothek und REST-Referenz für Project Server 2013 enthält Informationen zum JavaScript-Objektmodell und zur REST-Schnittstelle, die Sie für den Zugriff auf Project Serverfunktionen verwenden. Sie können diese APIs verwenden, um browserübergreifende Web-Apps, Project Professional 2013-Add-Ins und Apps für Nicht-Windows-Geräte zu entwickeln, die auf Project Server 2013 und Project Online zugreifen.
ms.openlocfilehash: 54b7c17d2090fb15eec14d740aa835d6b167a1e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616152"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>JavaScript-Bibliothek und REST-Referenz für Project Server

Die JavaScript-Bibliothek und REST-Referenz für Project Server 2013 enthält Informationen zum JavaScript-Objektmodell und zur REST-Schnittstelle, die Sie für den Zugriff auf Project Serverfunktionen verwenden. Sie können diese APIs verwenden, um browserübergreifende Web-Apps, Project Professional 2013-Add-Ins und Apps für Nicht-Windows-Geräte zu entwickeln, die auf Project Server 2013 und Project Online zugreifen.
  
> [!NOTE]
> Das JavaScript-Objektmodell und die REST-Schnittstelle sind am clientseitigen Serverobjektmodell (CSOM) Project ausgerichtet. Sie bieten eine äquivalente Funktionalität wie der **Namespace "Microsoft.ProjectServer.Client"** im CSOM. 
  
Sie können über das JavaScript-Objektmodell, das im [PS-Namespace](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) in der Datei definiert ist, auf Project Serverfunktionalität `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` zugreifen. Das [ProjectContext-Objekt](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) im [PS-Namespace](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) ist der Einstiegspunkt für das JavaScript-Objektmodell. 
  
> [!NOTE]
> Um das JavaScript-Objektmodell zu durchsuchen und beim Debuggen zu helfen, können Sie die PS.debug.js-Datei im selben Verzeichnis verwenden. Zur Unterstützung der Entwicklung auf einem Remotecomputer enthält der [Project 2013 SDK-Download](https://www.microsoft.com/en-us/download/details.aspx?id=30435) die .NET Framework-Assemblys für das CSOM sowie die dateien PS.js und PS.debug.js. 
  
Sie können auch über die REST-Schnittstelle auf Project Serverfunktionalität zugreifen. Der Einstiegspunkt zur REST-Schnittstelle ist die **ProjectServer-Ressource,** auf die Sie mithilfe des  `https://ServerName/pwaName/_api/ProjectServer` Endpunkt-URI zugreifen. Die folgende Abfrage ruft beispielsweise die Zuordnungen im angegebenen Projekt ab (ersetzen Sie  _ServerName_ und  _pwaName,_ und ändern Sie die GUID so, dass sie mit einem Projekt übereinstimmt).
  
`https://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

Die **ProjectServer-Ressource** wird in [ProjectServer-Ressourcen in der REST-Schnittstelle](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources)beschrieben. Weitere REST-Ressourcen werden in der Dokumentation für die entsprechenden JavaScript-Objekte und -Member in dieser Referenz beschrieben. Weitere Informationen zur Verwendung von REST finden Sie unter [Clientseitiges Objektmodell (CSOM) für Project Server](client-side-object-model-csom-for-project-2013.md) und [Programmierung mithilfe des SharePoint 2013 REST-Diensts.](https://msdn.microsoft.com/library/fp142385%28office.15%29.aspx)
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>JavaScript-Bibliothek und REST-Referenz für Project Server
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [PS.js JavaScript-Bibliothek und REST-Referenz](https://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx) Enthält Informationen zum JavaScript-Objektmodell und zur REST-Schnittstelle für Project Server 2013. 
    
## <a name="see-also"></a>Siehe auch
<a name="bk_addresources"> </a>

- [Project 2013-Entwicklerdokumentation](project-2013-developer-documentation.md)   
- [Clientseitiges Objektmodell (CSOM) für Project Server](client-side-object-model-csom-for-project-2013.md)   
- [Erste Schritte mit dem JavaScript-Objektmodell](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [Arbeiten mit Projekten unter Verwendung des JavaScript-Objektmodells](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

