---
title: Massenaktualisierung benutzerdefinierter Felder und Erstellen von Projektwebsites in Project Online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Um Kunden dabei zu helfen, Project Online optimal zu nutzen und die Diensterweiterung und -flexibilität zu verbessern, haben wir dem clientseitigen Objektmodell zwei Methoden hinzugefügt, die Sie in Project Online Apps und Workflows verwenden können.
ms.openlocfilehash: aadb20a85b97dad42c7158e52b7611609cc23496
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563203"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Massenaktualisierung von benutzerdefinierten Feldern und Erstellen von Projektwebsites aus einem Workflow in Project Online

Um Kunden dabei zu helfen, Project Online optimal zu nutzen und die Diensterweiterung und -flexibilität zu verbessern, haben wir dem clientseitigen Objektmodell zwei Methoden hinzugefügt, die Sie in Project Online Apps und Workflows verwenden können.
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |Massenaktualisierung benutzerdefinierter Projektfelder. Nur für Project Online. Nur in der REST-API verfügbar.  <br/> |
|**CreateProjectSite** <br/> | Erstellt eine Project Website. Nur für Project Online. Verfügbar in der REST-API, im verwalteten Clientobjektmodell und im JavaScript-Clientobjektmodell.  <br/> |
   
Diese Methoden bieten nicht nur mehr Flexibilität, sie bieten auch erhebliche Leistungsverbesserungen beim Speichern und Veröffentlichen von Projekten in einem Workflow. Dieser Artikel beschreibt die Verwendung der Methoden in der REST-API und enthält Anweisungen zum Erstellen eines Workflows, der benutzerdefinierte Felder massenweise aktualisiert, und eines Workflows, der eine Project Website erstellt.
  
> [!NOTE]
> Weitere Informationen zum Aufrufen von REST-APIs aus SharePoint 2013-Workflows finden Sie unter [Using SharePoint REST services from workflow with POST method](https://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) and Calling the SharePoint [2013 Rest API from a SharePoint Designer Workflow.](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/) 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>Massenaktualisierung von benutzerdefinierten Projektfeldern aus einem Workflow
<a name="BulkUpdateCustomFields"> </a>

Bisher konnten Workflows jeweils nur ein benutzerdefiniertes Feld aktualisieren. Das aktualisieren benutzerdefinierter Projektfelder kann zu einer schlechten Endbenutzererfahrung führen, wenn Benutzer zwischen Project Detailseiten wechseln. Jedes Update erforderte eine separate Serveranforderung mithilfe der Aktion **"Project Feld festlegen",** und das Aktualisieren mehrerer benutzerdefinierter Felder in einem Netzwerk mit hoher Latenz und geringer Bandbreite führte zu einem nicht trivialen Aufwand. Um dieses Problem zu beheben, haben wir die **UpdateCustomFields-Methode** zur REST-API hinzugefügt, mit der Sie benutzerdefinierte Felder massenweise aktualisieren können. Um **UpdateCustomFields** zu verwenden, übergeben Sie ein Wörterbuch, das die Namen und Werte aller benutzerdefinierten Felder enthält, die Sie aktualisieren möchten.
  
Die REST-Methode befindet sich am folgenden Endpunkt:
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> Ersetzen Sie den `<site-url>` Platzhalter in den Beispielen durch die URL Ihrer Project Web App-Website (PWA) und den `<guid>` Platzhalter durch die Projekt-UID. 
  
In diesem Abschnitt wird beschrieben, wie Sie einen Workflow erstellen, der benutzerdefinierte Felder für ein Projekt massenweise aktualisiert. Der Workflow folgt den folgenden allgemeinen Schritten:
  
- Warten Sie, bis das Projekt, das Sie aktualisieren möchten, eingecheckt wird
    
- Erstellen eines Datensatzes, der alle Benutzerdefinierten Feldaktualisierungen für das Projekt definiert
    
- Sehen Sie sich das Projekt an.
    
- Aufrufen von **UpdateCustomFields** zum Anwenden der Aktualisierungen des benutzerdefinierten Felds auf das Projekt 
    
- Protokollieren relevanter Informationen in der Workflowverlaufsliste (falls erforderlich)
    
- Veröffentlichen des Projekts
    
- Einchecken des Projekts
    
Der letzte End-to-End-Workflow sieht wie folgt aus:
  
![End-to-end workflow](media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "End-to-end workflow")
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>So erstellen Sie einen Workflow, der benutzerdefinierte Felder massenweise aktualisiert

1. Optional. Store die vollständige URL Ihres Projekts in einer Variablen, die Sie im gesamten Workflow verwenden können.
    
    ![Speichern der URL des Projekts in einer Variablen](media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "Speichern der URL des Projekts in einer Variablen")
  
2. Fügen Sie dem Workflow die Aktion **"Auf Project Ereignis warten"** hinzu, und wählen Sie das Ereignis **"Wenn ein Projekt eingecheckt wird".** 
    
    ![Wait for the project to be checked in](media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Wait for the project to be checked in")
  
3. Erstellen Sie ein **requestHeader-Wörterbuch** mithilfe der Wörterbucherstellungsaktion.  Sie verwenden den gleichen Anforderungsheader für alle Webdienstaufrufe in diesem Workflow. 
    
    ![Build the requestHeader dictionary](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Build the requestHeader dictionary")
  
4. Fügen Sie dem Wörterbuch die folgenden beiden Elemente hinzu.
    
    |Name|Typ|Wert|
    |:-----|:-----|:-----|
    |Annehmen  <br/> |String  <br/> |application/json; odata=verbose  <br/> |
    |Content-Type  <br/> |Zeichenfolge  <br/> |application/json; odata=verbose  <br/> |
   
    ![Hinzufügen eines Accept-Headers](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Hinzufügen eines Accept-Headers")
  
5. Erstellen Sie ein **requestBody-Wörterbuch** mithilfe der Wörterbucherstellungsaktion.  In diesem Wörterbuch werden alle Feldaktualisierungen gespeichert, die Sie anwenden möchten. 
    
    Jede Aktualisierung des benutzerdefinierten Felds erfordert vier Zeilen: den Metadatentyp (1), den Schlüssel (2), den Wert (3) und den Werttyp (4).
    
    - **__metadata/Typ** Der Metadatentyp des Felds. Dieser Datensatz ist immer identisch und verwendet die folgenden Werte: 
    
       - Name: customFieldDictionary(i)/__metadata/type (wobei **i** der Index jedes benutzerdefinierten Felds im Wörterbuch ist, beginnend mit 0) 
            
       - Typ: Zeichenfolge
            
       - Wert: SP. Keyvalue
    
       ![Definieren einer benutzerdefinierten Feldaktualisierung](media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Definieren einer benutzerdefinierten Feldaktualisierung")
  
    - **Schlüssel** Der interne Name des benutzerdefinierten Felds im Format: *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       Sie finden den internen Namen eines benutzerdefinierten Felds, indem Sie zum **InternalName-Endpunkt** navigieren: `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       Wenn Sie Ihre benutzerdefinierten Felder manuell erstellt haben, unterscheiden sich die Werte von Website zu Website. Wenn Sie den Workflow für mehrere Websites wiederverwenden möchten, stellen Sie sicher, dass die benutzerdefinierten Feld-IDs korrekt sind.
    
    - **Wert** Der Wert, der dem benutzerdefinierten Feld zugewiesen werden soll. Für benutzerdefinierte Felder, die mit Nachschlagetabellen verknüpft sind, müssen Sie die internen Namen der Nachschlagetabelleneinträge anstelle der tatsächlichen Nachschlagetabellenwerte verwenden. 
    
       Den internen Namen des Nachschlagetabelleneintrags finden Sie am folgenden Endpunkt: `https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       Wenn Sie ein benutzerdefiniertes Feld für die Nachschlagetabelle eingerichtet haben, um mehrere Werte zu akzeptieren, verwenden Sie  `;#` dies zum Verketten von Werten (siehe Beispielverzeichnis unten). 
    
    - **ValueType** Der Typ des benutzerdefinierten Felds, das Sie aktualisieren. 
    
       - Verwenden Sie für Felder "Text", "Duration", "Flag" und "LookupTable" die Zeichenfolge "Edm.String".
    
       - Verwenden Sie für Zahlenfelder Edm.Int32, Edm.Double oder einen beliebigen anderen OData-akzeptierten Nummerntyp.
    
       - Verwenden Sie für Datumsfelder Edm.DateTime
    
       Im folgenden Beispielwörterbuch werden Updates für drei benutzerdefinierte Felder definiert. Die erste ist für ein benutzerdefiniertes Feld für die Nachschlagetabelle mit mehreren Werten, das zweite für ein Zahlenfeld und das dritte für ein Datumsfeld. Beachten Sie, wie der **customFieldDictionary-Index** erhöht wird. 
    
       > [!NOTE]
       > Diese Werte dienen nur zur Veranschaulichung. Welche Schlüssel-Wert-Paare Sie verwenden, hängt von Ihren PWA Daten ab. 
  
       |Name|Typ|Wert|
       |:-----|:-----|:-----|
       |customFieldDictionary(0)/__metadata/type  <br/> |String  <br/> |SP. Keyvalue  <br/> |
       |customFieldDictionary(0)/Key  <br/> |String  <br/> |Custom \_ ce23fbf43fa0e411941000155d3c8201  <br/> |
       |customFieldDictionary(0)/Value  <br/> |String  <br/> |Entry \_ b9a2fd69279de411940f00155d3c8201;#Entry \_ baa2fd69279de411940f00155d3c8201  <br/> |
       |customFieldDictionary(0)/ValueType  <br/> |String  <br/> |Edm.String  <br/> |
       |customFieldDictionary(1)/__metadata/type  <br/> |String  <br/> |SP. Keyvalue  <br/> |
       |customFieldDictionary(1)/Key  <br/> |String  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customFieldDictionary(1)/Value  <br/> |String  <br/> |90.5  <br/> |
       |customFieldDictionary(1)/ValueType  <br/> |String  <br/> |Edm.Double  <br/> |
       |customFieldDictionary(2)/__metadata/type  <br/> |String  <br/> |SP. Keyvalue  <br/> |
       |customFieldDictionary(2)/Key  <br/> |String  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customFieldDictionary(2)/Value  <br/> |String  <br/> |2015-04-01T00:00:00  <br/> |
       |customFieldDictionary(2)/ValueType  <br/> |String  <br/> |Edm.DateTime  <br/> |
   
       ![Wörterbuch, das benutzerdefinierte Feldaktualisierungen definiert](media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Wörterbuch, das benutzerdefinierte Feldaktualisierungen definiert")
  
6. Fügen Sie eine **Http-Webdienstaktion aufrufen** hinzu, um das Projekt auszuchecken. 
    
    ![Call the Checkout method](media/8ce56014-0317-419b-afa7-229d05c86885.png "Call the Checkout method")
  
7. Bearbeiten Sie die Eigenschaften des Webdienstaufrufs, um den Anforderungsheader anzugeben. Klicken Sie zum Öffnen des Dialogfelds **"Eigenschaften"** mit der rechten Maustaste auf die Aktion, und wählen Sie **"Eigenschaften"** aus.
    
    ![Angeben des Anforderungsheaders in den Eigenschaften des Webdienstaufrufs](media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Angeben des Anforderungsheaders in den Eigenschaften des Webdienstaufrufs")
  
8. Fügen Sie eine **Call HTTP Web Service-Aktion** hinzu, um die **UpdateCustomFields-Methode** aufzurufen. 
    
    ![Create a Call HTTP Web Service action](media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Create a Call HTTP Web Service action")
  
    Notieren Sie sich das  `/Draft/` Segment in der Webdienst-URL. Die vollständige URL sollte wie folgt aussehen: `https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![Aufrufen der UpdateCustomFields-Methode](media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Aufrufen der UpdateCustomFields-Methode")
  
9. Bearbeiten Sie die Eigenschaften des Webdienstaufrufs, um die **Parameter "RequestHeader"** und **"RequestContent"** an die erstellten Wörterbücher zu binden. Sie können auch eine neue Variable zum Speichern von **ResponseContent** erstellen.
    
    ![Binden der Wörterbücher an den Anforderungsheader und den Inhalt](media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Binden der Wörterbücher an den Anforderungsheader und den Inhalt")
  
10. Optional. Lesen Sie aus dem Antwortwörterbuch, um den Status des Warteschlangenauftrags zu überprüfen und die Informationen in der Workflowverlaufsliste zu protokollieren.
    
    ![Setting up logging](media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Setting up logging")
  
11. Fügen Sie einen Webdienstaufruf zum **Veröffentlichungsendpunkt** hinzu, um das Projekt zu veröffentlichen. Verwenden Sie immer denselben Anforderungsheader. 
    
    ![Aufrufen der Publish-Methode](media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Aufrufen der Publish-Methode")
  
    ![Properties for the Publish web service call](media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Properties for the Publish web service call")
  
12. Fügen Sie dem **Checkin-Endpunkt** einen endgültigen Webdienstaufruf hinzu, um das Projekt einchecken zu können. 
    
    ![Call the Checkin method](media/430510cb-0774-4911-af7f-b565b83eba0e.png "Call the Checkin method")
  
    ![Eigenschaften des Checkin-Webdienstaufrufs](media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Eigenschaften des Checkin-Webdienstaufrufs")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>Erstellen einer Project Website aus einem Workflow

Jedes Projekt kann über eigene dedizierte SharePoint Websites verfügen, auf denen Teammitglieder zusammenarbeiten, Dokumente freigeben, Probleme auslösen können usw. Zuvor konnten Websites nur automatisch bei der ersten Veröffentlichung oder manuell vom Projektmanager in Project Professional oder vom Administrator in PWA Einstellungen erstellt oder deaktiviert werden.
  
Wir haben die **CreateProjectSite-Methode** hinzugefügt, damit Sie auswählen können, wann Projektwebsites erstellt werden sollen. Dies ist besonders nützlich für Organisationen, die ihre Websites automatisch erstellen möchten, wenn ein Projektvorschlag eine bestimmte Phase in einem vordefinierten Workflow erreicht, anstatt bei der ersten Veröffentlichung. Durch das Verschieben der Projektwebsiteerstellung wird die Leistung beim Erstellen eines Projekts erheblich verbessert. 
  
**Voraussetzung:** Bevor Sie **CreateProjectSite** verwenden können, muss die Einstellung **"Benutzer auswählen zulassen"** für die Erstellung von Projektwebsites in **PWA Einstellungen** > ** Verbundene SharePoint Sites ** > **Einstellungen** festgelegt werden.
  
![Die Einstellung "Benutzern die Auswahl erlauben" in den PWA-Einstellungen](media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Setting Allow users to choose in PWA settings")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>So erstellen Sie einen Workflow, der eine Project Website erstellt

1. Erstellen oder bearbeiten Sie einen vorhandenen Workflow, und wählen Sie den Schritt aus, in dem Sie Ihre Project Websites erstellen möchten.
    
2. Erstellen Sie ein **requestHeader-Wörterbuch** mithilfe der Wörterbucherstellungsaktion.  
    
    ![Build the requestHeader dictionary](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Build the requestHeader dictionary")
  
3. Fügen Sie dem Wörterbuch die folgenden beiden Elemente hinzu.
    
    |Name|Typ|Wert|
    |:-----|:-----|:-----|
    |Annehmen  <br/> |String  <br/> |application/json; odata=verbose  <br/> |
    |Content-Type  <br/> |Zeichenfolge  <br/> |application/json; odata=verbose  <br/> |
   
    ![Hinzufügen eines Accept-Headers](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Hinzufügen eines Accept-Headers")
  
4. Fügen Sie die **Aktion "HTTP-Webdienst aufrufen"** hinzu. Ändern Sie den Anforderungstyp, um **POST** zu verwenden, und legen Sie die URL mit dem folgenden Format fest:
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![Building the CreateProjectSite endpoint URI](media/42a90a5e-8d1b-4667-a933-785175212847.png "Building the CreateProjectSite endpoint URI")
  
    Übergeben Sie den Namen des Project-Standorts als Zeichenfolge an die **CreateProjectSite-Methode.** Übergeben Sie eine leere Zeichenfolge, um den Projektnamen als Websitenamen zu verwenden. Achten Sie darauf, eindeutige Namen zu verwenden, damit die nächste Projektwebsite, die Sie erstellen, funktioniert. 
    
5. Bearbeiten Sie die Eigenschaften des Webdienstaufrufs, um den **Parameter "RequestHeader"** an das von Ihnen erstellte Wörterbuch zu binden. 
    
    ![Binden des Wörterbuchs an die Anforderung](media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "Binden des Wörterbuchs an die Anforderung")
  
## <a name="see-also"></a>Siehe auch

- [Project-Programmieraufgaben](project-programming-tasks.md)
- [Clientseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Workflows in SharePoint 2013](https://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

