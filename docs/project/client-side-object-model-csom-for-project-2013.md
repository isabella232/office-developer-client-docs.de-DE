---
title: Clientseitiges Objektmodell (CSOM) für Project 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.assetid: 716325eb-b092-4934-921f-84129d0a1f5f
description: Das clientseitige Objektmodell (CSOM) von Project Server 2013 implementiert allgemeine Serverfunktionen. Das Project Server CSOM umfasst ein Microsoft .NET CSOM, ein Microsoft Silverlight CSOM, ein Windows Phone 8 CSOM und ein JavaScript Object Model (JSOM). Darüber hinaus enthält das CSOM einen OData-Dienst, der eine REST-Schnittstelle ermöglicht. Die REST-Schnittstelle ist in erster Linie für die Entwicklung von Apps auf Nicht-Windows-Plattformen wie iOS und Android gedacht.
ms.localizationpriority: high
ms.openlocfilehash: 339e5dc9c05402e1be4aed30bf6448bc59b0c422
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563133"
---
# <a name="client-side-object-model-csom-for-project-2013"></a>Clientseitiges Objektmodell (CSOM) für Project 2013

Das clientseitige Objektmodell (CSOM) von Project Server 2013 implementiert allgemeine Serverfunktionen. Das Project Server CSOM umfasst ein Microsoft .NET CSOM, ein Microsoft Silverlight CSOM, ein Windows Phone 8 CSOM und ein JavaScript Object Model (JSOM). Darüber hinaus enthält das CSOM einen OData-Dienst, der eine REST-Schnittstelle ermöglicht. Die REST-Schnittstelle ist in erster Linie für die Entwicklung von Apps auf Nicht-Windows-Plattformen wie iOS und Android gedacht.
  
> [!NOTE]
> Lösungen für Project Online müssen das CSOM verwenden. Lokale Apps können jedoch entweder das CSOM oder das Project Server Interface (PSI) verwenden. Wenn das CSOM die Funktionalität enthält, die Sie verwenden möchten, empfehlen wir Ihnen, das CSOM für neue Apps zu verwenden. 
  
In CSOM-Erweiterungen bietet das **ProjectContext**-Objekt den Einstiegspunkt für Serverinhalte und -funktionen. Das .NET-CSOM, das Silverlight-CSOM und das Windows Phone-CSOM verwenden das [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx)-Objekt, und das JSOM verwendet das **PS.ProjectContext**-Objekt. **ProjectContext**-Eigenschaften bieten direkten Zugriff auf Project Server-Kernobjekte in der aktuellen Project-Web-App-Websitesammlung. Informationen zum Speicherort der CSOM-Assemblys und der JavaScript-Datei finden Sie unter [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
 **Apps und das Sicherheitsmodell** Apps müssen für CRUD-Vorgänge (Create, Read, Update, Delete) das CSOM mit Project Server 2013 und Project Online verwenden. Project-Apps verwenden nicht das Nur-App-Authentifizierungsmodell in SharePoint 2013. Eine Project Server-App erfordert einen bestimmten Berechtigungsanforderungsumfang, der angibt, in wessen Auftrag Befehle ausgeführt werden sollen. 
  
 **REST-Abfragen** Sie können REST-Abfragen des CSOM OData-Dienstes ohne die Verwendung von Metadaten erstellen. Bei einigen Drittanbietertools können Sie die .NET-Assemblys für das CSOM zum Entwickeln von Apps für andere Geräte verwenden. Durchsuchen Sie beispielsweise das Internet nach "Plattformübergreifende .NET-Entwicklungstools für iOS und Android". 
  
> [!NOTE]
> Obwohl die Option `$metadata` für den **ProjectData**-Berichtsdienst gültig ist (`https://ServerName/pwaName/_api/ProjectData/$metadata`), wurde die Option `$metadata` für den **ProjectServer**-Dienst des clientseitigen Objektmodells in der veröffentlichten Version von Project Server 2013 entfernt. Um die CSOM-Objekte und Elemente zu suchen, die als REST-Endpunkte zur Verfügung stehen, lesen Sie die Informationen unter [JavaScript-Bibliothek und REST-Referenz für Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md). 
  
Sie können die `https://ServerName/pwaName/_api/ProjectServer`-Abfrage verwenden, um die im CSOM über die REST-Oberfläche verfügbaren Entitäten anzuzeigen. Bei REST-Abfragen spiegelt die **ProjectServer**-Entität die Eigenschaften des [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx)-Objekts in der verwalteten Assembly „Microsoft.ProjectServer.Client.dll“ und des [PS.ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx)-Objekts im JSOM wider. Sie können zum Beispiel Ihren Browser verwenden, um Informationen vom CSOM zu Projekten in Project-Web-App, zu den Zuweisungen in einem bestimmten Projekt und zu dem Aufgabennamen einer angegebenen Zuweisung für eine angegebene Ressource abzurufen, indem Sie die folgenden Abfragen verwenden (jede Abfrage verwendet dasselbe `https://ServerName/pwaName/_api`-URL-Präfix). Die GUIDs sind Beispielwerte für **Project.Id**, **EnterpriseResource.Id** und **Assignment.Id**.
  
```HTML
/ProjectServer/Projects
/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments
/ProjectServer/EnterpriseResources('28eeb2b5-fe74-4efc-aa35-6a64514d1526')/Assignments('a2eafeb5-437c-e111-92fc-00155d3ba208')/Task?$select=Name
```

Im Gegensatz zur OData-Schnittstelle für den **ProjectData**-Dienst, die für die Berichterstellung schreibgeschützt ist, können Sie CRUD-Vorgänge mithilfe von REST-Abfragen mit dem **ProjectServer**-Dienst ausführen. REST-Abfragen für das Project Server-CSOM wurden in erster Linie für andere Plattformen als Windows-Desktop entworfen, z. B. Windows RT, iOS und Android. Für Windows-Desktop und Serverplattformen wie Windows 7, Windows 8 und Windows Server 2008 R2, können Sie die CSOM-verwalteten Assemblys verwenden. Bei Web-Apps können Sie PS.js für JavaScript verwenden. Informationen zum Ausführen von CRUD-Vorgängen mithilfe von REST-Abfragen finden Sie im Thema [Verwenden von OData-Abfragevorgängen in SharePoint REST-Anforderungen](https://msdn.microsoft.com/library/d4b5c277-ed50-420c-8a9b-860342284b72%28Office.15%29.aspx) im SharePoint 2013 SDK. Weitere Informationen zur Verwendung des **ProjectData**-Diensts finden Sie unter [Abfragen von OData-Feeds für Project-Berichtsdaten](https://msdn.microsoft.com/library/office/jj163048.aspx).
  
In Tabelle 1 sind die **ProjectContext**-Eigenschaften aufgeführt, die Project Server-Objekte darstellen. Sie können diese Objekte verwenden, um andere Project Server 2013-Entitäten, z. B. Zuweisungen und Aufgaben, abzurufen. 
  
**Tabelle 1. ProjectContext-Eigenschaften, mit denen auf Project Server-Objekte im CSOM und JSOM zugegriffen werden kann**

|**CSOM (.NET, Silverlight und Windows Phone)**|**JSOM**|
|:-----|:-----|
|[CustomFields](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.CustomFields.aspx) <br/> |customFields  <br/> |
|[EnterpriseProjectTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseProjectTypes.aspx) <br/> |enterpriseProjectTypes  <br/> |
|[EnterpriseResources](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseResources.aspx) <br/> |enterpriseResources  <br/> |
|[EntityTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EntityTypes.aspx) <br/> |entityTypes  <br/> |
|[EventHandlers](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EventHandlers.aspx) <br/> |eventHandlers  <br/> |
|[Ereignisse](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Events.aspx) <br/> |Ereignisse  <br/> |
|[LookupTables](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.LookupTables.aspx) <br/> |lookupTables  <br/> |
|[Phases](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Phases.aspx) <br/> |phases  <br/> |
|[Projekte](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Projects.aspx) <br/> |projects  <br/> |
|[Stages](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Stages.aspx) <br/> |stages  <br/> |
|[WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowActivities.aspx) <br/> |workflowActivities  <br/> |
|[WorkflowDesigner](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowDesigner.aspx) <br/> |workflowDesigner  <br/> |
   
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

Unter [Erste Schritte mit dem Project Server-CSOM und .NET](getting-started-with-the-project-server-csom-and-net.md) finden Sie grundlegende Informationen zum Project Server-CSOM und zu .NET-Anweisungen zum Erstellen einer einfachen .NET-CSOM-Erweiterung in Visual Studio 2012 und Codebeispiele. 
  
Unter [Erste Schritte mit dem Project Server 2013-JavaScript-Objektmodell](getting-started-with-the-project-server-2013-javascript-object-model.md) finden Sie grundlegende Informationen zum Project Server-JSOM, Anweisungen zum Erstellen einer einfachen JSOM-Erweiterung in Visual Studio 2012 und Codebeispiele. 
  
Lesen Sie auch die folgenden Artikel, in denen die Verwendung des CSOM erläutert wird:
  
- [Massenaktualisierung von benutzerdefinierten Feldern und Erstellen von Projektwebsites aus einem Workflow in Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
    
- [Arbeiten mit Projekten unter Verwendung des JavaScript-Objektmodells](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    
> [!NOTE]
> Sie können auch Visual Studio 2010 für die .NET Framework 4-Entwicklung mit dem CSOM verwenden. 
  
## <a name="reference"></a>Referenz

[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
  
## <a name="see-also"></a>Siehe auch



[Project Server 2013-Architektur](project-server-2013-architecture.md)


[Auswählen des richtigen API-Satzes in SharePoint 2013](https://msdn.microsoft.com/library/f36645da-77c5-47f1-a2ca-13d4b62b320d%28Office.15%29.aspx)

