---
title: Massen-Update für benutzerdefinierte Felder und Erstellen von Projektwebsites in Project Online
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: Damit werden Kunden optimal Project Online und unsere Service Erweiterbarkeit und Flexibilität zu verbessern, haben wir zwei Methoden das clientseitige Objektmodell hinzugefügt, die Sie in Project Online apps und Workflows verwenden können.
ms.openlocfilehash: 4f8fee5de5efb69f410b78e9ce93b9dc9bb133f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796188"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Massenaktualisierung von benutzerdefinierten Feldern und Erstellen von Projektwebsites aus einem Workflow in Project Online

Damit werden Kunden optimal Project Online und unsere Service Erweiterbarkeit und Flexibilität zu verbessern, haben wir zwei Methoden das clientseitige Objektmodell hinzugefügt, die Sie in Project Online apps und Workflows verwenden können.
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |Massen aktualisiert benutzerdefinierte Projektfelder. Für Project Online nur. Nur in der REST-API verfügbar.  <br/> |
|**CreateProjectSite** <br/> | Erstellt eine Projektwebsite. Für Project Online nur. Verfügbar in der REST-API, verwaltetes Clientobjektmodell und JavaScript-Clientobjektmodell.  <br/> |
   
Neben der Bereitstellung von mehr Flexibilität, bieten diese Methoden auch beträchtliche Leistungssteigerungen beim Speichern und Veröffentlichen von Projekten in einem Workflow. In diesem Artikel wird beschrieben, wie die Methoden in der REST-API verwendet und enthält Anweisungen zum Erstellen eines Workflows, Bulk Updates benutzerdefinierte Felder und ein Workflow, der eine Projektwebsite erstellt.
  
> [!NOTE]
> Weitere Informationen zum Aufrufen von REST-APIs in SharePoint 2013-Workflows, finden Sie unter [Verwenden von SharePoint-REST-Dienste von Workflows mit einem POST-Methode](http://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl) und [der SharePoint 2013 Rest-API in einem SharePoint Designer-Workflow aufrufen](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/). 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>BULK Update benutzerdefinierte Projektfelder mithilfe eines Workflows
<a name="BulkUpdateCustomFields"> </a>

Bisher konnte Workflows nur ein benutzerdefiniertes Feld zu einem Zeitpunkt aktualisiert werden. Benutzerdefinierte Projektfelder One nacheinander aktualisieren kann in eine schlechte End-User Experience führen, wenn Benutzer zwischen Projektdetailseiten umzustellen. Jedes Update erforderlich, eine separate Server-Anforderung mit der Aktion **Projektfeld festlegen** , und aktualisieren mehrere benutzerdefinierte Felder auf hoher Latenz, Netzwerk mit niedriger Bandbreite war der Gesamtumsatz ein einfacher Aufwand. Um dieses Problem zu beheben, haben wir die **UpdateCustomFields** -Methode der REST-API, dass-Sie Massen können benutzerdefinierte Felder aktualisieren hinzugefügt. Um **UpdateCustomFields**zu verwenden, übergeben Sie ein Wörterbuch, enthält den Namen und Werten aller benutzerdefinierten Felder, den Sie aktualisieren möchten.
  
Die REST-Methode finden Sie unter den folgenden Endpunkt:
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> Ersetzen Sie die `<site-url>` Platzhalter in den Beispielen mit der URL der Project Web App (PWA) Website und die `<guid>` Platzhalter für Ihr Projekt UID. 
  
In diesem Abschnitt wird beschrieben, wie zum Erstellen eines Workflows, Bulk benutzerdefinierte Felder für ein Projekt aktualisiert wird. Der Workflow die folgenden allgemeinen Schritte:
  
- Warten Sie auf das Projekt, das zu aktualisierende um eingecheckt abrufen
    
- Erstellen einer Datengruppe, die alle benutzerdefinierten Felds-Updates für das Projekt definiert.
    
- Das Projekt auszuchecken
    
- Rufen Sie **UpdateCustomFields** , um die benutzerdefinierten Felds Updates auf das Projekt anwenden 
    
- Melden Sie relevanten Informationen in der Workflowverlaufsliste (sofern erforderlich)
    
- Veröffentlichen des Projekts
    
- Überprüfen des Projekts
    
Der endgültige, End-to-End-Workflow sieht folgendermaßen aus:
  
![Ende zum workflow] (media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "Ende zum workflow")
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>Zum Erstellen eines Workflows aktualisiert, Bulk benutzerdefinierte Felder

1. Optional. Speichern Sie die vollständige URL des Projekts in einer Variablen, die Sie im Verlauf des Workflows verwenden können.
    
    ![Speichern Sie die URL des Projekts in einer Variablen] (media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "Speichern Sie die URL des Projekts in einer Variablen")
  
2. Fügen Sie den **Projektereignis warten** auf den Workflow, und wählen Sie das Ereignis **beim Einchecken eines Projekts** . 
    
    ![Warten Sie auf das Projekt eingecheckt werden] (media/699aa9c7-b3c9-426e-a775-96993a13559c.png "Warten Sie auf das Projekt eingecheckt werden")
  
3. Erstellen Sie ein **RequestHeader** Wörterbuch mit der Aktion **Wörterbuch erstellen** . Verwenden Sie den gleichen Anforderungsheader für alle, die den Webdienst in diesem Workflow aufruft. 
    
    ![Das RequestHeader Wörterbuch erstellen] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Das RequestHeader Wörterbuch erstellen")
  
4. Fügen Sie die folgenden zwei Elemente, um das Wörterbuch.
    
    |Name|Typ|Wert|
    |:-----|:-----|:-----|
    |Annehmen  <br/> |Zeichenfolge  <br/> |Application/Json; OData = verbose  <br/> |
    |Content-Type  <br/> |Zeichenfolge  <br/> |Application/Json; OData = verbose  <br/> |
   
    ![Hinzufügen eines Accept-Headers] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Hinzufügen eines Accept-Headers")
  
5. Erstellen Sie ein **RequestBody** Wörterbuch mit der Aktion **Wörterbuch erstellen** . Dieses Wörterbuch speichert alle Updates dar, die Sie anwenden möchten. 
    
    Jedes benutzerdefinierte Feld Update erfordert vier Zeilen: des Felds (1) Metadaten-Typ, Schlüssel (2), Wert (3) und (4) Werttyp.
    
    - **__metadata/Typ** Das Feld Metadaten-Typ. Dieser Eintrag ist immer gleich und verwendet die folgenden Werte: 
    
       - Name: CustomFieldDictionary (i) / __metadata/Typ (wobei **i** der Index jedes benutzerdefinierten Felds im Wörterbuch, beginnend mit 0 ist) 
            
       - Typ: Zeichenfolge
            
       - Wert: SP. KeyValue
    
       ![Definieren eines benutzerdefinierten Felds Updates] (media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "Definieren eines benutzerdefinierten Felds Updates")
  
    - **Schlüssel** Der interne Name des benutzerdefinierten Felds, im Format: *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       Navigieren Sie zur **InternalName** Endpunkt finden Sie den internen Namen eines benutzerdefinierten Felds:`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       Wenn Sie die benutzerdefinierten Felder manuell erstellt haben, werden die Werte von Site zu Site davon abweichen. Wenn Sie den Workflow auf mehreren Websites wiederverwenden möchten, stellen Sie sicher, dass das benutzerdefinierte Feld IDs richtig sind.
    
    - **Wert** Der Wert des benutzerdefinierten Feldes zugewiesen. Für benutzerdefinierte Felder, die mit Nachschlagetabellen verknüpft sind, müssen Sie die internen Namen der Einträge in der Nachschlagetabellen anstelle von tatsächlichen Nachschlagetabellenwerte verwenden. 
    
       Der interne Name des Nachschlagetabelleneintrags finden Sie unter den folgenden Endpunkt:`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       Wenn Sie einen benutzerdefinierten Felds der Nachschlagetabelle legen Sie bis zu mehrere Werte akzeptiert, verwenden Sie haben `;#` Werte verketten (wie im nachfolgenden Beispiel Wörterbuch dargestellt). 
    
    - **Werttyp** Der Typ des benutzerdefinierten Felds, die Sie aktualisieren. 
    
       - Verwenden Sie für Text, Dauer, Kennzeichen und LookupTable-Felder Edm.String
    
       - Verwenden Sie für Zahlenfelder Edm.Int32, Edm.Double oder eine andere OData-akzeptiert Zahl Art
    
       - Verwenden Sie für Datumsfelder Edm.DateTime
    
       Das Wörterbuch für die Beispiel unten definiert Updates für drei benutzerdefinierte Felder. Die erste für eine mehrere Wert benutzerdefinierten Felds der Nachschlagetabelle ist, die zweite wird für ein numerisches Feld und der dritte ist für ein Date-Feld. Hinweis wie der **CustomFieldDictionary** Index erhöht. 
    
       > [!NOTE]
       > Diese Werte sind nur zur Veranschaulichung. Die Schlüssel-Wert-Paaren, die Sie verwenden, hängt von der PWA-Daten ab. 
  
       |Name|Typ|Wert|
       |:-----|:-----|:-----|
       |CustomFieldDictionary (0) / __metadata/Typ  <br/> |Zeichenfolge  <br/> |SP. KeyValue  <br/> |
       |CustomFieldDictionary (0) / -Taste  <br/> |Zeichenfolge  <br/> |Benutzerdefinierte\_ce23fbf43fa0e411941000155d3c8201  <br/> |
       |CustomFieldDictionary (0) / Wert  <br/> |Zeichenfolge  <br/> |Eintrag\_b9a2fd69279de411940f00155d3c8201; #Entry\_baa2fd69279de411940f00155d3c8201  <br/> |
       |CustomFieldDictionary (0) / Werttyp  <br/> |Zeichenfolge  <br/> |Edm.String  <br/> |
       |CustomFieldDictionary (1) / __metadata/Typ  <br/> |Zeichenfolge  <br/> |SP. KeyValue  <br/> |
       |CustomFieldDictionary (1) / Schlüssel  <br/> |Zeichenfolge  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |CustomFieldDictionary (1)-Wert  <br/> |Zeichenfolge  <br/> |90.5  <br/> |
       |CustomFieldDictionary (1) / Werttyp  <br/> |Zeichenfolge  <br/> |Edm.Double  <br/> |
       |CustomFieldDictionary (2) / __metadata/Typ  <br/> |Zeichenfolge  <br/> |SP. KeyValue  <br/> |
       |CustomFieldDictionary (2) / Schlüssel  <br/> |Zeichenfolge  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |CustomFieldDictionary (2)-Wert  <br/> |Zeichenfolge  <br/> |2015-04-01T00:00:00.0000000  <br/> |
       |CustomFieldDictionary (2) / Werttyp  <br/> |Zeichenfolge  <br/> |Edm.DateTime  <br/> |
   
       ![Wörterbuch, das benutzerdefinierte Feld Updates definiert] (media/41a1f18f-a6b2-40ff-904b-437baf962621.png "Wörterbuch, das benutzerdefinierte Feld Updates definiert")
  
6. Hinzufügen einer Aktion **HTTP-Webdienst aufrufen,** um das Projekt ausgecheckt. 
    
    ![Rufen Sie die Checkout-Methode] (media/8ce56014-0317-419b-afa7-229d05c86885.png "Rufen Sie die Checkout-Methode")
  
7. Bearbeiten der Eigenschaften des Webdienstaufrufs Anforderungsheaders angeben. Um das Dialogfeld **Eigenschaften** zu öffnen, mit der rechten Maustaste der Aktion, und wählen Sie **Eigenschaften**aus.
    
    ![Angeben der Anfrage-Header in Webdienst Aufrufen von Eigenschaften] (media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "Angeben der Anfrage-Header in Webdienst Aufrufen von Eigenschaften")
  
8. Hinzufügen einer Aktion **HTTP-Webdienst aufrufen,** um die **UpdateCustomFields** -Methode aufrufen. 
    
    ![Erstellen einer HTTP-Webdienst aufrufen-Aktion] (media/9a73a201-c035-41b4-8798-506ac48b90f8.png "Erstellen einer HTTP-Webdienst aufrufen-Aktion")
  
    Hinweis Die `/Draft/` Segment in der Webdienst-URL. Die vollständige URL sollte wie folgt aussehen:`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![Rufen Sie die UpdateCustomFields-Methode] (media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "Rufen Sie die UpdateCustomFields-Methode")
  
9. Bearbeiten Sie die Eigenschaften für den Webdienst aufgerufen, binden Sie die Parameter **RequestHeader** und **RequestContent** auf, die Sie erstellt haben. Sie können auch eine neue Variable zum Speichern der **ResponseContent**erstellen.
    
    ![Binden Sie die Wörterbücher auf die Anforderungsheader und Inhalte] (media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "Binden Sie die Wörterbücher auf die Anforderungsheader und Inhalte")
  
10. Optional. Lesen Sie aus der Antwort Wörterbuch, überprüfen Sie den Status des Warteschlangenauftrags und die Informationen in der Workflow-Verlaufsliste protokollieren.
    
    ![Einrichten der Protokollierung] (media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "Einrichten der Protokollierung")
  
11. Fügen Sie einen Webdienstaufruf an den Endpunkt **Veröffentlichen** , um das Projekt zu veröffentlichen. Verwenden Sie immer den gleichen Anforderungsheader. 
    
    ![Rufen Sie die Publish-Methode] (media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Rufen Sie die Publish-Methode")
  
    ![Rufen Sie die Eigenschaften für den Webdienst veröffentlichen] (media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "Rufen Sie die Eigenschaften für den Webdienst veröffentlichen")
  
12. Fügen Sie eine endgültige Web Service-Aufruf an den Endpunkt **Checkin** zum Einchecken des Projekts. 
    
    ![Rufen Sie die Checkin-Methode] (media/430510cb-0774-4911-af7f-b565b83eba0e.png "Rufen Sie die Checkin-Methode")
  
    ![Eigenschaften für die Checkin-Webdienst aufrufen] (media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Eigenschaften für die Checkin-Webdienst aufrufen")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>Erstellen Sie eine Projektwebsite mithilfe eines Workflows

Jedes Projekt haben einen eigenen dedizierten SharePoint-Websites, in dem Teammitglieder können zusammenarbeiten, Dokumente freizugeben, lösen von Problemen und usw.. Bisher Websites können nur erstellt werden, automatisch in zuerst veröffentlichen oder manuell vom Projektmanager in Project Professional oder vom Administrator in PWA-Einstellungen, oder sie können deaktiviert werden.
  
Wir haben die **CreateProjectSite** -Methode hinzugefügt, damit Sie beim Erstellen von Projektwebsites auswählen können. Dies ist besonders für Organisationen, die bei der ersten veröffentlichen, anstatt ihre Websites beim ein Projektvorschlag eine bestimmte Phase in einem vordefinierten Workflow erreicht automatisch erstellen möchten. Zurückstellen Project Site Creation erheblich verbessert die Leistung über das Erstellen eines Projekts. 
  
**Erforderliche:** Bevor Sie **CreateProjectSite**verwenden können, muss die Einstellung **Benutzern erlauben, wählen** für Project Site Creation in **PWA-Einstellungen** festgelegt werden > ** verbundene SharePoint-Websites ** > **Einstellungen**.
  
![Festlegen "Ermöglicht Benutzern die Auswahl" in PWA-Einstellungen] (media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "Einstellung Benutzerberechtigungen zum Wählen Sie in PWA-Einstellungen")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>Zum Erstellen eines Workflows erstellt, die eine Projektwebsite

1. Erstellen oder Bearbeiten eines vorhandenen Workflows, und wählen Sie den Schritt, wo Sie Ihre Projektwebsites erstellen möchten.
    
2. Erstellen Sie ein **RequestHeader** Wörterbuch mit der Aktion **Wörterbuch erstellen** . 
    
    ![Das RequestHeader Wörterbuch erstellen] (media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "Das RequestHeader Wörterbuch erstellen")
  
3. Fügen Sie die folgenden zwei Elemente, um das Wörterbuch.
    
    |Name|Typ|Wert|
    |:-----|:-----|:-----|
    |Annehmen  <br/> |Zeichenfolge  <br/> |Application/Json; OData = verbose  <br/> |
    |Content-Type  <br/> |Zeichenfolge  <br/> |Application/Json; OData = verbose  <br/> |
   
    ![Hinzufügen eines Accept-Headers] (media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Hinzufügen eines Accept-Headers")
  
4. Fügen Sie den **HTTP-Webdienst aufrufen** . Ändern Sie die Anforderung zum **POST**verwenden, und legen Sie die URL im folgenden Format:
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![Erstellen von CreateProjectSite-Endpunkt-URI] (media/42a90a5e-8d1b-4667-a933-785175212847.png "Erstellen von CreateProjectSite-Endpunkt-URI")
  
    Übergeben Sie den Namen der Project-Website an die **CreateProjectSite** -Methode als Zeichenfolge. Um den Namen des Projekts als Websitename verwenden, übergeben Sie eine leere Zeichenfolge. Achten Sie darauf, dass Sie eindeutige Namen verwenden, die nächste Projektwebsite, die Sie erstellen funktioniert. 
    
5. Bearbeiten Sie die Eigenschaften für den Webdienst aufgerufen, an das Wörterbuch den Parameter **RequestHeader** binden, dass Sie erstellt haben. 
    
    ![Binden Sie das Wörterbuch, das die Anforderung] (media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "Binden Sie das Wörterbuch, das die Anforderung")
  
## <a name="see-also"></a>Siehe auch

- [Project-Programmieraufgaben](project-programming-tasks.md)
- [Clientseitiges Objektmodell (CSOM) für Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Workflows in SharePoint 2013](http://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    

