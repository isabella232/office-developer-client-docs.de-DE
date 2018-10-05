---
title: Clientseitiges Objektmodell (CSOM) für Project 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 716325eb-b092-4934-921f-84129d0a1f5f
description: Das Project Server 2013 mithilfe der clientseitigen Objektmodell (CSOM) implementiert allgemeine Serverfunktionen. Die Project Server-CSOM umfasst eine Microsoft .NET Framework-CSOM, ein Microsoft Silverlight CSOM, eine Windows Phone 8-CSOM und eine JavaScript-Objektmodell (JSOM). Darüber hinaus enthält das CSOM einen OData-Dienst, der eine REST-Schnittstelle ermöglicht. Die REST-Schnittstelle ist in erster Linie für die Entwicklung von apps auf nicht-Windows-Plattformen wie iOS und Android vorgesehen.
ms.openlocfilehash: 8be603fbee35f228dea0fa6b6be087b8e09c30e5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394447"
---
# <a name="client-side-object-model-csom-for-project-2013"></a>Clientseitiges Objektmodell (CSOM) für Project 2013

Das Project Server 2013 mithilfe der clientseitigen Objektmodell (CSOM) implementiert allgemeine Serverfunktionen. Die Project Server-CSOM umfasst eine Microsoft .NET Framework-CSOM, ein Microsoft Silverlight CSOM, eine Windows Phone 8-CSOM und eine JavaScript-Objektmodell (JSOM). Darüber hinaus enthält das CSOM einen OData-Dienst, der eine REST-Schnittstelle ermöglicht. Die REST-Schnittstelle ist in erster Linie für die Entwicklung von apps auf nicht-Windows-Plattformen wie iOS und Android vorgesehen.
  
> [!NOTE]
> Für Project Online Solutions müssen das CSOM verwenden. Lokale apps können jedoch die CSOM oder Project Server Interface (PSI). Wenn das CSOM die Funktionen, den, die Sie verwenden möchten enthält, wird empfohlen, das CSOM für neue apps zu verwenden. 
  
In CSOM-Erweiterungen bietet das **ProjectContext** -Objekt den Einstiegspunkt für Server-Inhalte und Funktionen. Verwenden Sie das [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) -Objekt, das .NET CSOM, des Silverlight-CSOM und dem Windows Phone-Clientobjektmodell und die JSOM verwendet die folgenden ** ProjectContext** Objekt. **ProjectContext** Eigenschaften ermöglichen den direkten Zugriff auf Project Server-Objekte in der aktuellen Project Web App-Websitesammlung Core. Informationen über den Speicherort CSOM-Assemblys und die JavaScript-Datei finden Sie unter [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
 **Apps und das Sicherheitsmodell** Apps müssen das CSOM für CRUD verwenden (erstellen, lesen, aktualisieren und löschen) Vorgänge mit Project Server 2013 und Project Online. Project-apps verwenden Sie das Authentifizierungsmodell nur-app-nicht in SharePoint 2013. Eine app für Project Server erfordert eine bestimmte berechtigungsanforderungsbereich, der angibt, in dessen Namen Befehle ausgeführt werden. 
  
 **REST-Abfragen** Sie können die REST-Abfragen des CSOM OData-Diensts erstellen, ohne die Metadaten verarbeiten. Einige Drittanbieter-Tools mit der .NET Assemblies für das CSOM zur Entwicklung von apps für andere Geräte zu aktivieren. Beispielsweise Durchsuchen des Internets für "plattformübergreifende .NET Development Tools für IOS- oder Android." 
  
> [!NOTE]
> Obwohl die `$metadata` Option für den **ProjectData** reporting-Dienst ist ungültig ( `https://ServerName/pwaName/_api/ProjectData/$metadata`), die `$metadata` option für die endgültige Produktversion von Project Server 2013 **ProjectServer** -Dienst, der die CSOM entfernt wird. Die CSOM-Objekte und Elemente, die als REST-Endpunkte verfügbar sind, finden Sie unter [JavaScript-Bibliothek und REST-Referenz für Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md). 
  
Um die Entitäten in der CSOM über die REST-Schnittstelle verfügbar angezeigt wird, können Sie die `https://ServerName/pwaName/_api/ProjectServer` Abfrage. Für REST-Abfragen spiegelt die Entität **ProjectServer** eng Eigenschaften des [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) -Objekts in der Assembly Microsoft.ProjectServer.Client.dll verwaltet und die folgenden [ ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) -Objekts in der JSOM. Sie können beispielsweise Ihr Browser verwenden, zum Abrufen von Informationen aus der CSOM zu Projekten in Project Web App, die Zuordnungen in ein angegebenes Projekt und dem Namen der Aufgabe einer angegebenen Zuordnung für eine angegebene Ressource mithilfe der folgenden Abfragen (jede Abfrage verwendet die gleiche `https://ServerName/pwaName/_api` URL-Präfix). Die GUIDs sind Beispielwerte für **Project.Id**, **EnterpriseResource.Id**und **Assignment.Id**.
  
```HTML
/ProjectServer/Projects
/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments
/ProjectServer/EnterpriseResources('28eeb2b5-fe74-4efc-aa35-6a64514d1526')/Assignments('a2eafeb5-437c-e111-92fc-00155d3ba208')/Task?$select=Name
```

Im Gegensatz zu den OData-Interface für den **ProjectData** -Dienst für die berichterstellung schreibgeschützt ist, können Sie mithilfe von REST-Abfragen mit der **ProjectServer** -Dienst CRUD-Vorgänge durchführen. REST-Abfragen für die Project Server-CSOM sind in erster Linie für Plattformen als Windows-Desktop, wie Windows RT, iOS und Android ausgelegt. Für Windows-Desktop und Server-Plattformen wie Windows 7, Windows 8 und Windows Server 2008 R2 können Sie die CSOM verwaltete Assemblys verwenden. Für Web-apps können Sie PS.js für JavaScript verwenden. Informationen dazu, wie folgt CRUD-Vorgänge unter Verwendung von REST-Abfragen finden Sie unter dem Thema [Verwendung OData-Abfragevorgängen in SharePoint-REST-Anforderungen](https://msdn.microsoft.com/library/d4b5c277-ed50-420c-8a9b-860342284b72%28Office.15%29.aspx) in SharePoint 2013 SDK. Informationen zur Verwendung von des **ProjectData** -Diensts finden Sie unter [Abfragen von OData-feeds für Project-Berichtsdaten](https://msdn.microsoft.com/library/office/jj163048.aspx).
  
Tabelle 1 enthält die **ProjectContext** -Eigenschaften, die Project Server-Objekte darstellen. Diese Objekte können Sie anderen Project Server 2013-Entitäten wie Zuordnungen und Aufgaben abrufen. 
  
**Tabelle 1. ProjectContext-Eigenschaften, mit denen auf Project Server-Objekte im CSOM und JSOM zugegriffen werden kann**

|**CSOM (.NET, Silverlight und Windows Phone)**|**JSOM**|
|:-----|:-----|
|[CustomFields](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.CustomFields.aspx) <br/> |customFields  <br/> |
|[EnterpriseProjectTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseProjectTypes.aspx) <br/> |enterpriseProjectTypes  <br/> |
|[EnterpriseResources](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EnterpriseResources.aspx) <br/> |enterpriseResources  <br/> |
|[EntityTypes](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EntityTypes.aspx) <br/> |entityTypes  <br/> |
|[Ereignishandler](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.EventHandlers.aspx) <br/> |Ereignishandler  <br/> |
|[Ereignisse](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Events.aspx) <br/> |events  <br/> |
|[Suchtabellen](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.LookupTables.aspx) <br/> |Suchtabellen  <br/> |
|[Phasen](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Phases.aspx) <br/> |phases  <br/> |
|[Projects](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Projects.aspx) <br/> |projects  <br/> |
|[Phasen](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.Stages.aspx) <br/> |stages  <br/> |
|[WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowActivities.aspx) <br/> |workflowActivities  <br/> |
|[WorkflowDesigner](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WorkflowDesigner.aspx) <br/> |workflowDesigner  <br/> |
   
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Erste Schritte mit dem Project Server-CSOM und .NET](getting-started-with-the-project-server-csom-and-net.md) enthält eine Übersicht über die Project Server-CSOM und .NET Anweisungen zur Erstellung eine einfache .NET CSOM-Erweiterung in Visual Studio 2012 und unterstützende Codebeispiele. 
  
[Erste Schritte mit dem Project Server 2013 JavaScript-Objektmodell](getting-started-with-the-project-server-2013-javascript-object-model.md) enthält eine Übersicht über die Project Server-JSOM Anleitung zum Erstellen einer einfachen JSOM-Erweiterungs in Visual Studio 2012 und unterstützende Codebeispiele. 
  
Lesen Sie auch die folgenden Artikel, in denen die Verwendung des CSOM erläutert wird:
  
- [Massenaktualisierung von benutzerdefinierten Feldern und Erstellen von Projektwebsites aus einem Workflow in Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
    
- [Arbeiten mit Projekten unter Verwendung des JavaScript-Objektmodells](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    
> [!NOTE]
> Sie können auch Visual Studio 2010 für die Entwicklung mit dem Clientobjektmodell .NET Framework 4. 
  
## <a name="reference"></a>Referenz

[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
  
## <a name="see-also"></a>Siehe auch



[Project Server 2013-Architektur](project-server-2013-architecture.md)


[Auswählen des richtigen API-Satzes in SharePoint 2013](https://msdn.microsoft.com/library/f36645da-77c5-47f1-a2ca-13d4b62b320d%28Office.15%29.aspx)

