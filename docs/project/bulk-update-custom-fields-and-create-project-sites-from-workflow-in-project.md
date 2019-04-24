---
title: Massenaktualisierung von benutzerdefinierten Feldern und Erstellen von Projektwebsites in Project Online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Um Kunden bei der optimalen Nutzung von Project online zu helfen und unsere Dienst Erweiterbarkeit und Flexibilität zu verbessern, haben wir zwei Methoden zum clientseitigen Objektmodell hinzugefügt, die Sie in Project Online-apps und-Workflows verwenden können.
ms.openlocfilehash: 4de42471cd8c2f12a982447ccffc27ec8104fa31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355380"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Massenaktualisierung von benutzerdefinierten Feldern und Erstellen von Projektwebsites aus einem Workflow in Project Online

Um Kunden bei der optimalen Nutzung von Project online zu helfen und unsere Dienst Erweiterbarkeit und Flexibilität zu verbessern, haben wir zwei Methoden zum clientseitigen Objektmodell hinzugefügt, die Sie in Project Online-apps und-Workflows verwenden können.
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |Massenaktualisierungen von Projekt benutzerdefinierten Feldern. Nur für Project online. Nur in der REST-API verfügbar.  <br/> |
|**CreateProjectSite** <br/> | Erstellt eine Projektwebsite. Nur für Project online. Verfügbar in der REST-API, dem verwalteten clientobjektmodell und dem JavaScript-clientobjektmodell.  <br/> |
   
Diese Methoden bieten nicht nur mehr Flexibilität, sondern auch erhebliche Leistungsverbesserungen beim Speichern und Veröffentlichen von Projekten in einem Workflow. In diesem Artikel wird beschrieben, wie Sie die Methoden in der REST-API verwenden und Anweisungen zum Erstellen eines Workflows bereitstellen, in dem benutzerdefinierte Felder und ein Workflow, der eine Projektwebsite erstellt, massenweise aktualisiert werden.
  
> [!NOTE]
> Weitere Informationen zum Aufrufen von REST-APIs aus SharePoint 2013-Workflows finden Sie unter [using SharePoint Rest Services from Workflow with Post Method](https://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) und [Calling the SharePoint 2013 Rest API from a SharePoint Designer Workflow](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/). 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>Massenaktualisierung von Projekt benutzerdefinierten Feldern aus einem Workflow
<a name="BulkUpdateCustomFields"> </a>

Bisher konnten Workflows nur ein benutzerdefiniertes Feld gleichzeitig aktualisieren. Das nacheinander aktualisieren von benutzerdefinierten Feldern kann zu einer schlechten Endbenutzererfahrung führen, wenn Benutzer zwischen Projekt Detail Seiten wechseln. Jedes Update erforderte eine separate Serveranforderung mithilfe der Aktion **Projektfeld festlegen** , und das Aktualisieren mehrerer benutzerdefinierter Felder in einem Netzwerk mit hoher Latenz und niedriger Bandbreite führte zu einem nicht trivialen Overhead. Um dieses Problem zu beheben, haben wir die **UpdateCustomFields** -Methode zur Rest-API hinzugefügt, mit der Sie benutzerdefinierte Felder Massenaktualisieren können. Um **UpdateCustomFields**zu verwenden, führen Sie ein Wörterbuch mit den Namen und Werten aller benutzerdefinierten Felder aus, die Sie aktualisieren möchten.
  
Die REST-Methode finden Sie unter folgendem Endpunkt:
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> Ersetzen Sie `<site-url>` den Platzhalter in den Beispielen durch die URL Ihrer Project Web App (PWA)-Website `<guid>` und den Platzhalter mit ihrer Projekt-UID. 
  
In diesem Abschnitt wird beschrieben, wie Sie einen Workflow erstellen, in dem benutzerdefinierte Felder für ein Projekt massenweise aktualisiert werden. Der Workflow folgt diesen allgemeinen Schritten:
  
- Warten Sie, bis das Projekt, das Sie aktualisieren möchten, eingecheckt wird.
    
- Erstellen eines Datasets, das alle benutzerdefinierten Feld Aktualisierungen für das Projekt definiert
    
- AusChecken des Projekts
    
- Aufrufen von **UpdateCustomFields** zum Anwenden der Aktualisierungen des benutzerdefinierten Felds auf das Projekt 
    
- Protokollieren relevanter Informationen in der Workflowverlaufsliste (falls erforderlich)
    
- Veröffentlichen des Projekts
    
- EinChecken des Projekts
    
Der abschließende End-to-End-Workflow sieht wie folgt aus:
  
![End-to-End-Workflow] (media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "End-to-End-Workflow")
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>So erstellen Sie einen Workflow, der Massenaktualisierungen für benutzerdefinierte Felder durchführen

1. Optional. Speichern Sie die vollständige URL des Projekts in einer Variablen, die Sie im gesamten Workflow verwenden können.
    
    ![Speichern der URL des Projekts in einer Variablen] (media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "Speichern der URL des Projekts in einer Variablen")
  
2. Fügen Sie die Aktion auf **Projektereignis warten** zum Workflow hinzu, und wählen Sie das Ereignis **beim Einchecken eines Projekts** aus. 
    
    ![Warten Sie, bis das Projekt eingecheckt wird] . (media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Warten Sie, bis das Projekt eingecheckt wird") .
  
3. Erstellen eines **requestHeader** -Wörterbuchs mit der Aktion **Wörterbuch** erstellen. Sie verwenden denselben Anforderungsheader für alle Webdienstaufrufe in diesem Workflow. 
    
    ![Erstellen des requestHeader-Wörterbuchs] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Erstellen des requestHeader-Wörterbuchs")
  
4. Fügen Sie dem Wörterbuch die folgenden beiden Elemente hinzu.
    
    |Name|Typ|Wert|
    |:-----|:-----|:-----|
    |Annehmen  <br/> |Zeichenfolge  <br/> |Application/JSON; odata = ausführlich  <br/> |
    |Content-Type  <br/> |Zeichenfolge  <br/> |Application/JSON; odata = ausführlich  <br/> |
   
    ![Hinzufügen eines Accept] -Headers (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Hinzufügen eines Accept") -Headers
  
5. Erstellen eines **requestBody** -Wörterbuchs mit der Aktion **Wörterbuch** erstellen. Dieses Wörterbuch speichert alle Feld Aktualisierungen, die Sie anwenden möchten. 
    
    Für jedes benutzerdefinierte Feld Update sind vier Zeilen erforderlich: der (1) Metadatentyp, (2) Schlüssel, (3) Wert und (4) Werttyp.
    
    - **__metadata/Typ** Der Metadatentyp des Felds. Dieser Datensatz ist immer derselbe und verwendet die folgenden Werte: 
    
       - Name: customFieldDictionary (i)/__metadata/Type (wobei **i** der Index der einzelnen benutzerdefinierten Felder im Wörterbuch ist, beginnend mit 0) 
            
       - Typ: Zeichenfolge
            
       - Wert: SP. KeyValue
    
       ![Definieren einer benutzerdefinierten Feld Aktualisierung] (media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Definieren einer benutzerdefinierten Feld Aktualisierung")
  
    - **Schlüssel** Der interne Name des benutzerdefinierten Felds im Format: *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       Sie können den internen Namen eines benutzerdefinierten Felds ermitteln, indem Sie zu dem **internen** Name-Endpunkt navigieren:`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       Wenn Sie Ihre benutzerdefinierten Felder manuell erstellt haben, unterscheiden sich die Werte von Website zu Website. Wenn Sie planen, den Workflow über mehrere Standorte hinweg wiederzuverwenden, stellen Sie sicher, dass die benutzerdefinierten Feld-IDs richtig sind.
    
    - **Wert** Der Wert, der dem benutzerdefinierten Feld zugewiesen werden soll. Bei benutzerdefinierten Feldern, die mit Nachschlagetabellen verknüpft sind, müssen Sie die internen Namen der Nachschlagetabellen Einträge anstelle der tatsächlichen Nachschlagetabellenwerte verwenden. 
    
       Den internen Namen des Nachschlagetabellen Eintrags finden Sie unter folgendem Endpunkt:`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       Wenn Sie ein benutzerdefiniertes Nachschlagetabellen Feld für die Annahme mehrerer Werte eingerichtet haben `;#` , verwenden Sie zum Verketten von Werten (wie im folgenden Beispielwörterbuch dargestellt). 
    
    - **ValueType** Der Typ des benutzerdefinierten Felds, das Sie aktualisieren. 
    
       - Verwenden Sie für Text-, Duration-, Flag-und Nachschlagefeld-Felder die Datei EDM. String
    
       - Verwenden Sie für Number-Felder EDM. Int32, EDM. Double oder einen anderen vom OData akzeptierten Zahlentyp.
    
       - Verwenden Sie für Datumsfelder EDM. DateTime.
    
       Das folgende Beispielwörterbuch definiert Updates für drei benutzerdefinierte Felder. Die erste ist für ein benutzerdefiniertes Feld mit mehreren Werten Nachschlagetabellen, die zweite für ein number-Feld und die dritte für ein Date-Feld. Beachten Sie, wie sich der **customFieldDictionary** -Index erhöht. 
    
       > [!NOTE]
       > Diese Werte dienen nur zur Illustration. Die Schlüssel-Wert-Paare, die Sie verwenden, hängen von ihren PWA-Daten ab. 
  
       |Name|Typ|Wert|
       |:-----|:-----|:-----|
       |customFieldDictionary (0)/__metadata/Type  <br/> |Zeichenfolge  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary (0)/Key  <br/> |Zeichenfolge  <br/> |Benutzer\_definierte ce23fbf43fa0e411941000155d3c8201  <br/> |
       |customFieldDictionary (0) Umfangs  <br/> |Zeichenfolge  <br/> |Eintrag\_b9a2fd69279de411940f00155d3c8201; #Entry\_baa2fd69279de411940f00155d3c8201  <br/> |
       |customFieldDictionary (0)/ValueType  <br/> |Zeichenfolge  <br/> |Edm.String  <br/> |
       |customFieldDictionary (1)/__metadata/Type  <br/> |Zeichenfolge  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary (1)/Key  <br/> |Zeichenfolge  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customFieldDictionary (1) Umfangs  <br/> |Zeichenfolge  <br/> |90,5  <br/> |
       |customFieldDictionary (1)/ValueType  <br/> |Zeichenfolge  <br/> |Edm.Double  <br/> |
       |customFieldDictionary (2)/__metadata/Type  <br/> |Zeichenfolge  <br/> |SP. KeyValue  <br/> |
       |customFieldDictionary (2)/Key  <br/> |Zeichenfolge  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customFieldDictionary (2) Umfangs  <br/> |Zeichenfolge  <br/> |2015-04-01T00:00:00.0000000  <br/> |
       |customFieldDictionary (2)/ValueType  <br/> |Zeichenfolge  <br/> |Edm.DateTime  <br/> |
   
       ![Wörterbuch, das benutzerdefinierte Feld Aktualisierungen definiert] (media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Wörterbuch, das benutzerdefinierte Feld Aktualisierungen definiert")
  
6. Fügen Sie eine Aktion zum **Aufrufen des http-** Webdiensts hinzu, um das Projekt zu überprüfen. 
    
    ![Aufrufen der Checkout-Methode] (media/8ce56014-0317-419b-afa7-229d05c86885.png "Aufrufen der Checkout-Methode")
  
7. Bearbeiten Sie die Eigenschaften des Webdienstaufrufs, um den Anforderungsheader anzugeben. Klicken Sie zum Öffnen des Dialogfelds **Eigenschaften** mit der rechten Maustaste auf die Aktion, und wählen Sie **Eigenschaften**aus.
    
    ![Angeben des Anforderungsheaders in Webdienstaufruf Eigenschaften] (media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Angeben des Anforderungsheaders in Webdienstaufruf Eigenschaften")
  
8. Fügen Sie die Aktion **http-Webdienst aufrufen** hinzu, um die **UpdateCustomFields** -Methode aufzurufen. 
    
    ![Erstellen einer Aktion zum Aufrufen des http-] Webdiensts (media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Erstellen einer Aktion zum Aufrufen des http-") Webdiensts
  
    NoTieren Sie sich das `/Draft/` Segment in der WEBDIENST-URL. Die vollständige URL sollte wie folgt aussehen:`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![Aufrufen der UpdateCustomFields-Methode] (media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Aufrufen der UpdateCustomFields-Methode")
  
9. Bearbeiten Sie die Eigenschaften des Webdienstaufrufs, um die Parameter **RequestHeader** und **RequestContent** an die von Ihnen erstellten Wörterbücher zu binden. Sie können auch eine neue Variable zum Speichern der **ResponseContent**erstellen.
    
    ![Binden der Wörterbücher an den Anforderungsheader und-Inhalt] (media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Binden der Wörterbücher an den Anforderungsheader und-Inhalt")
  
10. Optional. Lesen Sie im Antwort Wörterbuch, um den Status des Warteschlangenauftrags zu überprüfen und die Informationen in der Workflowverlaufsliste zu protokollieren.
    
    ![Einrichten der Protokollierung] (media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Einrichten der Protokollierung")
  
11. Fügen Sie dem Veröffentlichungs Endpunkt einen **** Webdienstaufruf hinzu, um das Projekt zu veröffentlichen. Verwenden Sie immer den gleichen Anforderungsheader. 
    
    ![Aufrufen der Publish-Methode] (media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Aufrufen der Publish-Methode")
  
    ![Eigenschaften für den Webdienstaufruf veröffentlichen] (media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Eigenschaften für den Webdienstaufruf veröffentlichen")
  
12. Fügen Sie dem **Eincheck** Endpunkt einen endgültigen Webdienstaufruf hinzu, um das Projekt einzuchecken. 
    
    ![Aufrufen der Checkin-Methode] (media/430510cb-0774-4911-af7f-b565b83eba0e.png "Aufrufen der Checkin-Methode")
  
    ![Eigenschaften für den Eincheck Aufruf des] Webdiensts (media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Eigenschaften für den Eincheck Aufruf des") Webdiensts

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>Erstellen einer Projektwebsite aus einem Workflow

Jedes Projekt kann über eigene dedizierte SharePoint-Websites verfügen, in denen Teammitglieder zusammenarbeiten, Dokumente freigeben, Probleme auslösen usw. Bisher konnten Websites nur beim ersten veröffentlichen oder manuell vom Projektmanager in Project Professional oder vom Administrator in PWA-Einstellungen erstellt oder deaktiviert werden.
  
Wir haben die **CreateProjectSite** -Methode hinzugefügt, damit Sie auswählen können, wann Projektwebsites erstellt werden. Dies ist besonders nützlich für Organisationen, die ihre Websites automatisch erstellen möchten, wenn ein Projektvorschlag eine bestimmte Stufe in einem vordefinierten Workflow erreicht, statt bei der ersten Veröffentlichung. Durch das Verschieben der Projektwebsite Erstellung wird die Leistung des Erstellens eines Projekts erheblich verbessert. 
  
**Voraussetzung:** Bevor Sie **CreateProjectSite**verwenden können, muss die Einstellung **Benutzerauswahl zulassen** für die Erstellung von Projektwebsites in **PWA-Einstellungen** > * * verbundene SharePoint-Websites * * >- **Einstellungen**festgelegt werden.
  
![Einstellung "Benutzer können wählen" in PWA-Einstellungen] (media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Festlegen, dass Benutzer in PWA-Einstellungen auswählen können")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>So erstellen Sie einen Workflow, der eine Projektwebsite erstellt

1. Erstellen oder bearbeiten Sie einen vorhandenen Workflow, und wählen Sie den Schritt aus, in dem Sie die Projektwebsites erstellen möchten.
    
2. Erstellen eines **requestHeader** -Wörterbuchs mit der Aktion **Wörterbuch** erstellen. 
    
    ![Erstellen des requestHeader-Wörterbuchs] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Erstellen des requestHeader-Wörterbuchs")
  
3. Fügen Sie dem Wörterbuch die folgenden beiden Elemente hinzu.
    
    |Name|Typ|Wert|
    |:-----|:-----|:-----|
    |Annehmen  <br/> |Zeichenfolge  <br/> |Application/JSON; odata = ausführlich  <br/> |
    |Content-Type  <br/> |Zeichenfolge  <br/> |Application/JSON; odata = ausführlich  <br/> |
   
    ![Hinzufügen eines Accept] -Headers (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Hinzufügen eines Accept") -Headers
  
4. Fügen Sie die Aktion **http-Webdienst aufrufen** hinzu. Ändern Sie den Anforderungstyp in use **Post**, und legen Sie die URL im folgenden Format fest:
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![Erstellen des CreateProjectSite-Endpunkt-URI] (media/42a90a5e-8d1b-4667-a933-785175212847.png "Erstellen des CreateProjectSite-Endpunkt-URI")
  
    Geben Sie den Namen der Projektwebsite als Zeichenfolge an die **CreateProjectSite** -Methode an. Um den Projektnamen als Websitenamen zu verwenden, geben Sie eine leere Zeichenfolge an. Achten Sie darauf, eindeutige Namen zu verwenden, damit die nächste von Ihnen erstellte Projektwebsite funktioniert. 
    
5. Bearbeiten Sie die Eigenschaften des Webdienstaufrufs, um den Parameter **RequestHeader** an das von Ihnen erstellte Wörterbuch zu binden. 
    
    ![Binden des Wörterbuchs an die Anforderung] (media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "Binden des Wörterbuchs an die Anforderung")
  
## <a name="see-also"></a>Siehe auch

- [Project-Programmieraufgaben](project-programming-tasks.md)
- [Clientseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Workflows in SharePoint 2013](https://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

