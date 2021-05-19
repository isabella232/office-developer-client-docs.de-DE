---
title: JavaScript-Bibliothek und REST-Referenz für Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: Die JavaScript-Bibliothek und die REST-Referenz für Project Server 2013 enthält Informationen über das JavaScript-Objektmodell und die REST-Schnittstelle, die Sie für den Zugriff auf Project Serverfunktionen verwenden. Sie können diese APIs verwenden, um browserübergreifende Webanwendungen, Project Professional 2013-Add-Ins und Apps für Nicht-Windows-Geräte zu entwickeln, die auf Project Server 2013 und Project Online.
ms.openlocfilehash: fb58de1e3858a39f42cc9a643a7394cec191a462
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358107"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>JavaScript-Bibliothek und REST-Referenz für Project Server

Die JavaScript-Bibliothek und die REST-Referenz für Project Server 2013 enthält Informationen über das JavaScript-Objektmodell und die REST-Schnittstelle, die Sie für den Zugriff auf Project Serverfunktionen verwenden. Sie können diese APIs verwenden, um browserübergreifende Webanwendungen, Project Professional 2013-Add-Ins und Apps für Nicht-Windows-Geräte zu entwickeln, die auf Project Server 2013 und Project Online.
  
> [!NOTE]
> Das JavaScript-Objektmodell und die REST-Schnittstelle richten sich Project clientseitigen Serverobjektmodell (CSOM) aus. Sie bieten die gleiche Funktionalität wie **der Microsoft.ProjectServer.Client-Namespace** im CSOM. 
  
Sie können auf Project Serverfunktionen über das JavaScript-Objektmodell [](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) zugreifen, das im PS-Namespace in der Datei definiert `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` ist. Das [ProjectContext-Objekt](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) im [PS-Namespace](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) ist der Einstiegspunkt zum JavaScript-Objektmodell. 
  
> [!NOTE]
> Um das JavaScript-Objektmodell zu durchsuchen und beim Debuggen zu helfen, können Sie die PS.debug.js im gleichen Verzeichnis verwenden. Zur Unterstützung der Entwicklung auf einem Remotecomputer enthält der [Project 2013 SDK-Download](https://www.microsoft.com/en-us/download/details.aspx?id=30435) die .NET Framework-Assemblys für das CSOM sowie die PS.js- und PS.debug.js-Dateien. 
  
Sie können auch über die REST-Schnittstelle auf Project Serverfunktionen zugreifen. Der Einstiegspunkt zur REST-Schnittstelle ist die **ProjectServer-Ressource,** auf die Sie mithilfe des  `https://ServerName/pwaName/_api/ProjectServer` Endpunkt-URI zugreifen. Die folgende Abfrage ruft z. B. die Zuordnungen im angegebenen Projekt ab (ersetzen  _Sie ServerName_ und  _pwaName,_ und ändern Sie die GUID, um einem Projekt zu entsprechen).
  
`https://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

Die **ProjectServer-Ressource** wird unter [ProjectServer-Ressourcen in der REST-Schnittstelle beschrieben.](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources) Andere REST-Ressourcen werden in der Dokumentation für die entsprechenden JavaScript-Objekte und -Member in dieser Referenz beschrieben. Weitere Informationen zur Verwendung von REST finden Sie unter [Client-side object model (CSOM) for Project Server](client-side-object-model-csom-for-project-2013.md) and [Programming using the SharePoint 2013 REST service](https://msdn.microsoft.com/library/fp142385%28office.15%29.aspx).
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>JavaScript-Bibliothek und REST-Referenz für Project Server
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [PS.js-JavaScript-Bibliothek und REST-Referenz](https://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx) Enthält Informationen zum JavaScript-Objektmodell und zur REST-Schnittstelle für Project Server 2013. 
    
## <a name="see-also"></a>Siehe auch
<a name="bk_addresources"> </a>

- [Project 2013-Entwicklerdokumentation](project-2013-developer-documentation.md)   
- [Clientseitiges Objektmodell (CSOM) für Project Server](client-side-object-model-csom-for-project-2013.md)   
- [Erste Schritte mit dem JavaScript-Objektmodell](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [Arbeiten mit Projekten unter Verwendung des JavaScript-Objektmodells](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

