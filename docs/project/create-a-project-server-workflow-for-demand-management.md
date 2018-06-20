---
title: Erstellen eines Project Server-Workflows für das bedarfsmanagement
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: b0e4a3b3-d1df-454d-b74c-b980b0b456f6
description: In diesem Artikel wird beschrieben, wie zum Erstellen eines einfachen Workflows mithilfe von SharePoint Designer 2013.
ms.openlocfilehash: d548cbc47585add2648396f4736e6ad36a00bcb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796193"
---
# <a name="create-a-project-server-workflow-for-demand-management"></a>Erstellen eines Project Server-Workflows für das bedarfsmanagement

In diesem Artikel wird beschrieben, wie zum Erstellen eines einfachen Workflows mithilfe von SharePoint Designer 2013. Exportieren von Workflows in Visio 2013 für Visualisierung und zum Bearbeiten, oder Verwenden von Visio 2013 Design Project Server 2013-Workflows, und den Entwurf für die Veröffentlichung zu Project Web App in SharePoint Designer 2013 importieren. Weitere Informationen zu der SharePoint-Workflow-Plattform und Erstellen von Workflows mit Visio 2013 und SharePoint Designer 2013 finden Sie unter [Workflows in SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163986%28office.15%29.aspx) Artikel in der SharePoint 2013-Entwicklerdokumentation. 
  
Informationen zur Vorbereitung von Project Server für Workflows finden Sie unter [starten: Legen Sie einrichten und Konfigurieren von SharePoint 2013-Workflow-Manager](http://msdn.microsoft.com/en-us/library/jj163276%28office.15%29.aspx).

<a name="pj15_CreateWorkflowSPD_General"> </a>

## <a name="creating-a-general-workflow"></a>Erstellen eines allgemeinen Workflows

Verwenden Sie die folgenden Schritte zum Erstellen eines Project Server 2013-Workflows mithilfe von SharePoint Designer 2013. Der Workflow wird für das bedarfsmanagement von Projektvorschlägen entwickelt.
  
Ausführliche Schritte finden Sie im Abschnitt [Erstellen eines verzweigungsworkflows](#pj15_CreateWorkflowSPD_Detailed) . 
  
### <a name="to-create-a-project-server-workflow-general-procedure"></a>So erstellen Sie einen Project Server-Workflow (allgemeines Verfahren)

1. Ermitteln Sie die Anforderungen, und entwerfen Sie dann den Workflow. Unterteilen Sie ihn in Phasen und Stufen, und ermitteln Sie die benutzerdefinierten Felder, die vom Workflow verwendet werden.
    
2. Erstellen Sie in Project Web App Entitäten, die der Workflow benötigt:
    
    1. Prüfen Sie die vorhandenen Workflowphasen; erstellen Sie Phasen nach Bedarf.
        
    2. Erstellen Sie die benutzerdefinierten Enterprise-Felder, die der Workflow verwendet. Damit ein benutzerdefiniertes Feld in einer Workflowphase verfügbar ist, muss es von einem Workflow gesteuert sein.
        
    3. Bearbeiten oder erstellen Sie die Projektdetailseiten (Project Detail Pages, PDPs), die von Ihren Workflowphasen zum Sammeln von Informationen für das Projekt verwendet werden. In diesem Fall werden von den Phasen Standard-Projektdetailseiten verwendet, die so bearbeitet werden, dass sie ein neues benutzerdefiniertes Feld enthalten.
        
    4. Erstellen Sie die erforderlichen Workflowphasen, und verknüpfen Sie dann jede Workflowphase mit der korrekten Phase.
    
3. Erstellen Sie den Workflow in SharePoint Designer 2013 mithilfe deklarative Anweisungen im **textbasierten Designer**:
    
    > [!NOTE]
    > Sie können auch in den **Visual Designer** in SharePoint Designer 2013 wechseln oder Importieren einen vorhandenen Workflow aus Visio 2013. Führen Sie diese Schritte, um den **textbasierter Designer**verwenden: 
    > 
    > 1. Öffnen Sie die Project Web App-Website, und erstellen Sie einen Website-Workflow, der die Workflow-Plattform für **SharePoint 2013-Workflow - Project Server** verwendet. 
    > 2. Fügen Sie die Phasen hinzu, die vom Workflow verwendet werden.
    > 3. Fügen Sie die Schritte, Bedingungen, Aktionen und Schleifen des Workflows hinzu, die in jeder Phase erforderlich sind.
    > 4. Prüfen Sie auf Workflowfehler, und beheben Sie diese.
    > 5. (Optional) Wechseln Sie zum **Visual Designer**der Ansicht oder exportieren Sie des Workflows in Visio 2013-Datei. Sie können die Visio-Ansicht ändern und speichern Sie Änderungen an der aktuellen Workflow. Sie können die Visio-Datei bearbeiten und Importieren in SharePoint Designer 2013 andere Workflows erstellen können.
    > 6. Veröffentlichen des Workflows. Nach der Veröffentlichung, zeigt den Workflow in der Liste der Workflows für die Project Web App-Website.
    
4. Verwenden Sie den Workflow in Project Web App für das bedarfsmanagement von Projektvorschlägen:
    
    1. Erstellen Sie eine Enterprise-Projektvorlage (Enterprise Project Template, EPT), die den Workflow verwendet.
        
    2. Erstellen Sie auf der Project Center-Seite ein Projekt, das die EPT für den Workflow verwendet, und wechseln Sie dann durch die Workflowphasen.
        
    3. Testen Sie den Workflow sorgfältig.
        
    4. Stellen Sie den Workflow auf einem Produktionsserver bereit.

<a name="pj15_CreateWorkflowSPD_Detailed"> </a>

## <a name="creating-a-branching-workflow"></a>Erstellen eines Verzweigungsworkflows

Bevor Sie SharePoint Designer 2013 zum Erstellen eines Project Server-Workflows verwenden können, muss der Workflow-Manager-Client 1.0-Dienst für die Project Server 2013-Workflow-Aktivitäten verwenden konfiguriert werden. Informationen zur Konfiguration von Workflow-Manager-Client 1.0 finden Sie unter [Workflows in SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163986%28office.15%29.aspx) Artikel in der Entwicklerdokumentation für SharePoint Server 2013. 
  
Das folgende detaillierte Verfahren umfasst die gleichen Schritte wie im Abschnitt [Erstellen eines allgemeinen Workflows](#pj15_CreateWorkflowSPD_General) . 
  
### <a name="to-create-a-project-server-branching-workflow-detailed-procedure"></a>So erstellen Sie einen Project Server-Verzweigungsworkflow (ausführliches Verfahren)

#### <a name="1-plan-and-design-the-workflow"></a>1. planen Sie und Entwerfen Sie des Workflows.

Project Server-Workflows mit mehreren integrieren kann Stufen und Phasen in einem projektbedarfsmanagement Prozess. Da Workflows komplex sein können, müssen Sie verstehen die geschäftlichen Anforderungen und Planen Sie einen Workflow sorgfältig. Entwerfen Sie für ein einfaches Beispiel einen verzweigungsworkflow, der die geschätzte Kosten für einen Projektvorschlag verwendet, um zu bestimmen, ob das Angebot akzeptiert wird. Wenn die geschätzte Kosten größer ist als 25.000 USD, Ablehnen des Vorschlags; Sie andernfalls annehmen Sie den Vorschlag, und erstellen Sie ein Projekt.
    
Da Sie können Visio 2013 und SharePoint Designer 2013 zum Entwerfen und Erstellen von Workflows für Project Server 2013, können Sie leichter mit Workflows experimentieren, als mit Project Server 2010 möglich ist. Der Workflow Beispielentwurf in diesem Artikel wird genauso wie in den Artikel [Erstellen eines verzweigungsworkflows Workflows](http://msdn.microsoft.com/library/a02cafdc-d881-4271-b446-d8b2cd456a52%28Office.15%29.aspx) in Project 2010-SDK. Beim Entwerfen und erstellen Sie einen Workflow Test auf einem Remotecomputer mit einer Testinstanz von Project Web App können – Sie müssen nicht direkt auf einem Computer Project Server 2013 Workflows erstellen. 
    
#### <a name="2-create-the-entities-that-your-workflow-requires"></a>2. Erstellen der Entitäten, die den Workflow erforderlich.

Überprüfen Sie in Project Web App die verfügbaren Workflowphasen und Phasen und benutzerdefinierten Enterprise-Feldern, die verfügbar sind. Erstellen Sie bei Bedarf die Entitäten, die den Workflow erforderlich, wie in der folgenden Schritte aus:
    
1. **Workflowphasen** Die Standardinstallation von Project Web App enthält die erstellen, auswählen, planen, verwalten und nach Abschluss des Vorgangs Phasen. Für die Verzweigung Workflowbeispiel müssen Sie keinen anderen Phasen zu erstellen. 
        
2. **Benutzerdefinierte Enterprise-Felder** Die verzweigungsworkflow erfordert ein Projekt Kosten benutzerdefiniertes Feld, das Workflow gesteuert wird. Der Wert eines benutzerdefinierten Felds Workflow gesteuert wird auf einer Projektdetailseite festgelegt, die vom Workflow verwendet. Wählen Sie beispielsweise das Symbol **Einstellungen** in der oberen rechten einer Project Web App-Seite, wählen Sie **PWA-Einstellungen**, und wählen Sie dann **benutzerdefinierte Enterprise-Felder und Nachschlagetabellen**.
        
   Erstellen eines benutzerdefinierten Felds mit dem Namen Vorschlagskosten für die **Project** -Entität, und wählen Sie den **Kosten**. Geben Sie die Beschreibung Kosten für einen Projektvorschlag geschätzt. Wählen Sie im Abschnitt **Verhalten** **Verhalten vom Workflow gesteuert**.
        
3. **Projektdetailseiten** Bearbeiten Sie oder erstellen Sie die PDPs, die die Workflowphasen verwendet werden soll. Führen Sie beispielsweise die folgenden Schritte aus: 
        
    1. Wählen Sie auf der Seite servereinstellungen **Projektdetailseiten** aus, und wählen Sie dann die Projektdetailseite **ProjectInformation** aus. 
            
    2. Wählen Sie auf der Registerkarte **Seite** des Menübands in der Gruppe **Bearbeiten** **Seite bearbeiten**.
            
    3. Wählen Sie den Pfeil nach unten in der oberen rechten des **Grundlegenden Info** -Webparts aus, und wählen Sie dann auf **Webpart bearbeiten**. Oder wählen Sie auf der Registerkarte **Webpart** im Menüband in der Gruppe **Eigenschaften** **-Webpart-Eigenschaften** -Editor-Webpart angezeigt. 
            
    4. Die **Angezeigte Projektfelder** Abschnitt des Editors Teil (siehe Abbildung 1), wählen Sie **Ändern**.
            
    5. Fügen Sie das benutzerdefinierte Feld **Vorschlagskosten** , verschieben Sie diese über das Feld **Besitzer** in der Liste **Ausgewählte Projektfelder** , und klicken Sie dann auf **OK** (siehe Abbildung 1).
      
    6. Im-Editor-Webpart wählen Sie **OK**und dann in der Gruppe **Bearbeiten** auf der Registerkarte **Seite** des Menübands auf **Bearbeitung beenden** . Abbildung 2 zeigt das benutzerdefinierte Feld **Vorschlagskosten** , das die der Projektinformationen hinzugefügt wird. 

    **Abbildung 1. Bearbeiten des Projektfelder-Webparts auf einer Projektdetailseite**

    ![Bearbeiten der Felder für die Project-Webpart auf einer Projektdetailseite] (media/pj15_CreateWorkflowSPD_EditPDP.gif "Bearbeiten der Felder für die Project-Webpart auf einer Projektdetailseite")

    **Abbildung 2. Die bearbeitete PDP beinhaltet das benutzerdefinierte Feld Vorschlagskosten**

    ![Die bearbeitete PDP beinhaltet das Feld Vorschlagskosten] (media/pj15_CreateWorkflowSPD_EditedPDP.gif "Die bearbeitete PDP beinhaltet das Feld Vorschlagskosten")
  
4. **Workflowstufen** Erstellen Sie die Phasen, die für die einzelnen Phasen des Workflows erforderlich sind. Klicken Sie auf der Seite servereinstellungen wählen Sie **Workflowstufen aus**, und wählen Sie dann auf **Neue WORKFLOWSTUFE**. Abbildung 3 zeigt einen Teil der Seite Workflowstufe hinzufügen.
    
    **Abbildung 3. Hinzufügen einer Workflowphase in Project Web App**

    ![Hinzufügen einer Workflowphase in Project Web App] (media/pj15_CreateWorkflowSPD_AddWorkflowStage.gif "Hinzufügen einer Workflowphase in Project Web App")
  
    Das Verzweigen Workflowbeispiel verwendet die vier Stufen, die in Tabelle 1 aufgeführt sind. Im Abschnitt **Zusätzliche Einstellungen für sichtbare Projektdetailseite** Seitenrand Workflowstufe hinzufügen (nicht in Abbildung 3 dargestellt) sind die Werte optional. Sie bieten weitere Informationen auf der Seite Workflowstatus. Beispielsweise, da die anfängliche Vorschlag Details PDP Benutzereingaben erforderlich sind, können Sie das Kontrollkästchen **der Projektdetailseite Aufmerksamkeit** , und fügen Sie eine bestimmte Beschreibung wie legen Sie den Namen des Projekts und Kosten für diese PDP.
    
    In Abbildung 4 sind die vier Stufen abgebildet, die auf der Seite "Workflowstufen" durchlaufen werden.
    
    **In Tabelle 1. Phasen für das verzweigungsworkflow**

    |Name|Beschreibung|Beschreibung für Einreichung|Phase|Sichtbare PDPs|Benutzerdefinierte Felder|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |Ursprüngliche Vorschlagsdetails  <br/> |Legen Sie den Projektnamen und die Kosten fest.  <br/> |Reichen Sie das Projekt als Vorschlag ein.  <br/> |Erstellen  <br/> |Projektinformationen  <br/> Projektdetails  <br/> |Vorschlagskosten (erforderlich)  <br/> |
    |Projektdetails  <br/> |Geben Sie nähere Informationen zum vorgeschlagenen Projekt an.  <br/> |Senden Sie die Details ab, um mit dem Projekt fortzufahren.  <br/> |Erstellen  <br/> |Projektinformationen  <br/> Projektdetails  <br/> |Vorschlagskosten (schreibgeschützt)  <br/> |
    |Automatische Ablehnung  <br/> |Der Vorschlag wird auf Grundlage der angegebenen Informationen abgelehnt.  <br/> | <br/> |Erstellen  <br/> |Projektinformationen  <br/> |Vorschlagskosten (schreibgeschützt)  <br/> |
    |Ausführung  <br/> |Der Vorschlag wurde angenommen und ist bereit für das Projektmanagement.  <br/> | <br/> |Verwalten  <br/> |Projektinformationen  <br/> Projektdetails  <br/> |Vorschlagskosten (schreibgeschützt)  <br/> |
   
    **Abbildung 4. Liste der Workflowphasen in Project Web App**

    ![Liste der Workflowphasen in Project Web App] (media/pj15_CreateWorkflowSPD_WorkflowStages.gif "Liste der Workflowphasen in Project Web App")
  
#### <a name="3-construct-the-workflow-in-the-text-based-designer"></a>3. erstellen Sie den Workflow im textbasierten Designer.

Erstellen Sie den Workflow in SharePoint Designer 2013 mithilfe deklarative Anweisungen im textbasierten Designer. Starten Sie Sie an die orangefarbene Einfügelinie abzurufenden kontextbezogene AutoVervollständigen-Anweisungen für die Workflowlogik und Schritte eingeben, oder Sie können die Logik und die Schritte in der Gruppe **Einfügen** auf der Registerkarte **WORKFLOW** des Menübands mithilfe von Inhaltssteuerelementen einfügen. 
    
1. Wählen Sie in der Backstage-Ansicht von SharePoint Designer 2013 **Website öffnen**. Öffnen Sie beispielsweise `http://ServerName/pwa`. Wählen Sie im **Navigationsbereich** **Workflows**aus. Wählen Sie dann auf der Registerkarte **WORKFLOWS** des Menübands in der Gruppe **neu** **Website-Workflow**. In diesem Beispiel nennen Sie den Workflow Verzweigung Workflow. Stellen Sie sicher, dass **SharePoint 2013-Workflow - Project Server** in der Dropdownliste **Plattformtyp** aktiviert ist (siehe Abbildung 5). 
    
    **Abbildung 5. Erstellen eines Project Server-Website-Workflows**

    ![Erstellen eines Project Server-Website-Workflows] (media/pj15_CreateWorkflowSPD_CreateSiteWorkflow.gif "Erstellen eines Project Server-Website-Workflows")
  
2. Wählen Sie auf der Registerkarte **Workflow Verzweigen** . Wählen Sie dann auf der Registerkarte **WORKFLOW** , der dem Menüband in der Gruppe **Verwalten** in der Dropdown-Liste **Ansichten** **textbasierter Designer**. Zum Anzeigen der Ansicht durch die blinkende Orange Zeile einfügen (siehe Abbildung 6), klicken Sie in der Ansicht.
    
    **Abbildung 6. Verwenden der textbasierten Designer-Ansicht für den workflow**

    ![Verwenden der textbasierten Designer-Ansicht] (media/pj15_CreateWorkflowSPD_TextBasedDesigner.gif "Verwenden der textbasierten Designer-Ansicht")
  
3. Fügen Sie in der Ansicht **textbasierter Designer** die Phasen, die vom Workflow verwendet. Wählen Sie auf der Registerkarte **WORKFLOW** , der dem Menüband in der Gruppe **Einfügen** in der **Phase** Dropdown-Liste unter **Erstellen**die **Ursprüngliche Vorschlagsdetails**.
    
    Platzieren Sie unten orangefarbene Einfügelinie entsprechend der **Stufe: ursprüngliche Vorschlagsdetails** ein, und fügen Sie die anderen Stufen, die vom Workflow verwendet: **Projektdetails**, **Automatische Ablehnung**und **Ausführung** (siehe Abbildung 7). 
    
    **Abbildung 7. Hinzufügen einer Stufe zu einem Workflow in SharePoint Designer**

    ![Hinzufügen einer Stufe zu einem Workflow in SPD] (media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Hinzufügen einer Stufe zu einem Workflow in SPD")
  
4. Fügen Sie in jeder Phase die Workflowschritte und die Workflowlogik hinzu: 
    
    1. Platzieren Sie die orangefarbene Einfügelinie am Anfang des Textkörpers Phase, in der Phase **Ursprüngliche Vorschlagsdetails** . In der Gruppe **Einfügen** auf dem Menüband **Aktion**wählen, führen Sie einen Bildlauf nach unten zu **Project Web App-Aktionen**, und wählen Sie dann auf **Projektereignis warten**. Wählen Sie **dieses Projektereignis**, und wählen Sie **Ereignis: Wenn ein Projekt eingereicht wird fest** in der Dropdown-Liste. 
    
    2. Fügen Sie im Abschnitt **Übergang zu Stufe** im Freigabefenster **Ursprüngliche Vorschlagsdetails** **Wenn beliebiger Wert gleich Wert ist**. Sie können starten Sie die Anweisung eingeben oder verwenden Sie das **Bedingung** -Steuerelement in der Gruppe **Einfügen** , klicken Sie im Menüband. 
    
    3. Wählen Sie **das erste Steuerelement** , und wählen Sie dann auf **fx** im Dialogfeld **Workflow-Nachschlagevorgang definieren** angezeigt (siehe Abbildung 8). Wählen Sie in der Dropdownliste **Datenquelle** **Projektdaten**aus. Wählen Sie in der Dropdownliste **Quellenfeld** **Vorschlagskosten**.
    
       **Abbildung 8. Definieren eines Suchwerts im workflow**

       ![Definieren eines Suchwerts im workflow] (media/pj15_CreateWorkflowSPD_DefineWorkflowLookup.gif "Definieren eines Suchwerts im workflow")
  
    4. Führen Sie die `If` Anweisung, sodass dieser Folgendes angezeigt wird: **Wenn Project Projektdaten: Vorschlagskosten höher sind als 25000**
    
       > [!NOTE]
       > Alternativ konnten Sie eine Workflow-Variable erstellen, legen Sie die Variable auf den Wert des benutzerdefinierten Feldes und vergleichen Sie die Variable mit einem Wert. Erstellen Sie beispielsweise aus der Dropdownliste **Lokale Variablen** auf dem Menüband eine Variable mit dem Namen **Gesamtpreis** (keine Leerzeichen) vom Typ **Number**. Klicken Sie im Dialogfeld **Workflow-Nachschlagevorgang definieren** **Workflowvariablen und-Parameter** für die Datenquelle auswählen, und wählen Sie dann **Variable: Gesamtpreis** wie das Feld. Die **If** -Anweisung werden dann: **Wenn Variable: Gesamtpreis ist größer als 25000**
  
    5. Platzieren Sie die orangefarbene Einfügelinie innerhalb der `If` verzweigen, und fügen Sie dann mithilfe des **Aktion** -Steuerelements in der Gruppe " **Einfügen** " auf dem Menüband **eine Stufe** . Wählen Sie das **Stufen** Dropdown-Steuerelement, und wählen Sie die Phase der **Automatischen Ablehnung** . 
    
       In ähnlicher Weise in der `Else` verzweigen, **Wechseln Sie zur Projektdetails** -Anweisung einfügen. Abbildung 9 zeigt die abgeschlossene **Ursprüngliche Vorschlagsdetails** Phase. 
    
       **Abbildung 9. Abgeschlossene Logik für die ursprüngliche Vorschlagsdetails Phase**

       ![Abgeschlossene Logik für ursprüngliche Vorschlagsdetails] (media/pj15_CreateWorkflowSPD_InitialStageLogic.gif "Abgeschlossene Logik für ursprüngliche Vorschlagsdetails")
  
    6. In der Phase der **Automatischen Ablehnung** es sei denn, Sie Anhalten des Workflows und einige Daten auf einer Projektdetailseite anzeigen möchten, lassen Sie den ersten Abschnitt leer. Im Abschnitt **Übergang zu Stufe** muss einen Übergang enthalten. Da keine anderen Stufe nach einer Ablehnung vorhanden ist, geben Sie für die Anweisung Gehe zu Ende des Workflows. 
    
    7. Fügen Sie in der Stufe ' **Projektdetails** ' navigieren Sie zur Ausführung im Abschnitt **Übergang zu Stufe** . Es sei denn, es zusätzliche Daten sind hinzufügen oder Sie den Workflow anhalten möchten, ist es nicht erforderlich, warten, bis eine gesendete Ereignis. 
    
    8. In **der Ausführungsphase** es sei denn, Sie den Workflow anhalten möchten, lassen Sie Abschnitt Aktion Phase leer. Klicken Sie im Abschnitt **Übergang zu Stufe** fügen Sie hinzu, **Wechseln Sie zum Ende des Workflows**.
    
5. Wählen Sie in der Gruppe **Speichern** auf dem Menüband auf Workflowfehler überprüft (siehe Abbildung 10) **Überprüfen auf Fehler** . Beheben Sie alle Fehler, und wählen Sie dann auf **Speichern**.
    
    **Abbildung 10. Überprüfen den Workflow bei Fehlern in SharePoint Designer**

    ![Überprüfen der Fehler im workflow] (media/pj15_CreateWorkflowSPD_SPDCheckForErrors.gif "Überprüfen der Fehler im workflow")
  
6. (Optional) Wählen Sie in der Gruppe **Verwalten** auf dem Menüband in der Dropdown-Menü **Ansichten** **Visual Designer**aus. In Abbildung 11 wird die Ansicht auf 50 % vergrößert.
    
    Sie können Elemente im Workflow mithilfe des visuellen Designers bearbeiten. Wählen Sie die Bedingung **Wenn beliebiger Wert gleich Wert ist** , wählen Sie das Symbol in der unteren linken Ecke der Bedingung, und wählen Sie dann den **Wert** , der die Bedingungen Vergleich im Dialogfeld **Eigenschaften** anzeigen. 
    
    **Abbildung 11. Mithilfe des visuellen Designers für einen workflow**

    ![Verwenden Sie die Visio-Entwurfsansicht des Workflows] (media/pj15_CreateWorkflowSPD_SwitchView.gif "Verwenden Sie die Visio-Entwurfsansicht des Workflows")
  
    Wenn der Workflow in der Visual Designer angezeigt wird, um speichern Sie den Workflow in einer Datei Visio 2013 (.vsdx) als Sicherung oder höher für zu verwenden, können Sie **nach Visio exportieren**.
    
7. Veröffentlichen des Workflows. Wenn Sie SharePoint Designer 2013 verwenden, um den Workflow auf der aktiven Project Web App-Website veröffentlichen, wird der Workflow für die SharePoint-Website oder in Azure registriert ist und für neue EPTs in Project Web App verfügbar wird.

#### <a name="4-create-an-ept-for-the-workflow-and-then-test-the-workflow"></a>4. erstellen ein EPT für den Workflow, und Testen Sie den Workflow.

Klicken Sie in Project Web App erstellen Sie eine EPT für den Workflow, und Testen Sie den Workflow, indem Sie einen Projektvorschlag erstellen:
    
1. Klicken Sie auf der Seite Einstellungen für PWA wählen Sie **Enterprise-Projekttypen**, und erstellen Sie eine EPT mit dem Namen Verzweigen Testen des Workflows. Deaktivieren Sie das Kontrollkästchen **neue Projekte als SharePoint-Aufgabenlistenprojekte erstellen** , sodass Project Server wird Vollzugriff auf Projekte verwalten, die mithilfe des EPT erstellt werden. Wählen Sie in der Dropdownliste **Website-Workflowzuordnung** **Verzweigungsworkflow** aus, und wählen Sie dann in der Dropdown-Liste **Neue Projektseite** auf der ersten Seite sein, die der Workflow zeigt die **Projektinformationen** PDP aus. 
    
    **Abbildung 12. Hinzufügen eines EPT für den workflow**

    ![Hinzufügen eines EPT für den workflow] (media/pj15_CreateWorkflowSPD_EPTs.gif "Hinzufügen eines EPT für den workflow")
  
    > [!NOTE]
    > Ein Wert **Ja** , in der **SharePoint-Aufgabenlistenprojekt** -Spalte in der Tabelle der Enterprise-Projekttypen bezieht sich auf eine EPT, mit dem erstellt eine SharePoint-Aufgabenliste, in dem die Aufgabenliste in Project Web App sichtbar ist, aber SharePoint behält die Kontrolle des Projekts . Weitere Informationen zum Verwalten von Projekten als SharePoint-Aufgabenlisten finden Sie unter [Architektur von Project Server 2013](project-server-2013-architecture.md). 
  
2. Öffnen Sie auf der Seite Projekte in Project Web App, und erstellen Sie ein Projekt mithilfe des neuen EPT (siehe Abbildung 13). Da **Verzweigen Testen des Workflows** **Verzweigungsworkflow**zugeordnet ist, wird unter Kontrolle des Workflows Erstellen eines Projekts gestartet.
    
    **Abbildung 13. Erstellen eines Projekts mithilfe des Test-Verzweigung Workflow EPT**

    ![Erstellen eines Projekts mithilfe des EPT] (media/pj15_CreateWorkflowSPD_NewProject.gif "Erstellen eines Projekts mithilfe des EPT")
  
3. Wenn der Workflow die PDP **Projektinformationen** angezeigt wird, fügen Sie die Projektfelder Daten hinzu. Geben Sie beispielsweise den **Vorschlagskosten** Wert 30000. Die englischen Version von Project Server ändert das Feld, um 30.000 $ anzeigen (siehe Abbildung 14).
    
    **Abbildung 14. Verwenden der bearbeiteten Projektinformationen**

    ![Verwenden der bearbeiteten Projektinformationen] (media/pj15_CreateWorkflowSPD_NewProjectStage1.gif "Verwenden der bearbeiteten Projektinformationen")
  
4. Wählen Sie auf der Registerkarte **Projekt** im Menüband in der Gruppe **Projekt** **zu speichern**. Projektserver die Daten in die PDP dem Projekt hinzugefügt, und zeigt dann die Seite "Workflowstatus" (siehe Abbildung 15). Um die vollständige Beschreibung der ursprüngliche Vorschlagsdetails Stufe im Workflow-Status Diagramm angezeigt wird, bewegen Sie den Mauszeiger über die Phase im Workflow Visualisierung Diagramm.
    
    Das Raster **Alle Workflowstufen** verwendet einen grünen Pfeil angezeigt wird, dass die ursprüngliche Vorschlagsdetails Phase Eingabe wartet. Dies ist, da die Submit-Ereignis in der ursprüngliche Vorschlagsdetails Phase der Workflow wartet. Wenn der Workflow nicht für eine Submit-Ereignis warten, können Sie in der Gruppe **Seite** , um zur nächsten PDP gelangen **nächsten** auswählen. 
    
    **Abbildung 15. Mithilfe der Seite Workflowstatus in der Phase der ursprüngliche Vorschlagsdetails**

    ![Workflow-Statusseite nach der ersten Stufe] (media/pj15_CreateWorkflowSPD_NewProjectStage1Status.gif "Workflow-Statusseite nach der ersten Stufe")
  
    Das Workflow-Visualisierung-Diagramm zeigt die aktuelle Phase in eine hellgrüne Farbe. In der Phase **Erstellen** ist die ursprüngliche Vorschlagsdetails Phase die aktuelle Stufe. 
    
5. Wählen Sie auf dem Menüband in **der Gruppe** **Senden**.
    
    > [!TIP]
    > Wenn das Steuerelement **einreichen** deaktiviert ist, wird aktualisieren Sie die Seite. 
  
    Wenn der **Vorschlagskosten** -Wert größer als 25.000 USD ist, wird der Workflow in die automatische Ablehnung Phase verschoben. Abbildung 16 zeigt den Status der automatischen Ablehnung, wenn Sie **Submit** erneut auswählen. Wenn die **Vorschlagskosten** 25.000 US-Dollar oder weniger, der Workflow in der Stufe ' Projektdetails verschiebt ' (siehe Abbildung 17). 
    
    **Abbildung 16. Der Workflow wird in der Phase der automatischen Ablehnung abgeschlossen**

    ![Der Workflow ist in automatischer Ablehnung abgeschlossen] (media/pj15_CreateWorkflowSPD_AutomatedRejectionCompleted.gif "Der Workflow ist in automatischer Ablehnung abgeschlossen")
  
    Abbildung 17 zeigt einen weiteren Test mit einen Projektvorschlag mit dem Namen **Test 2 - Verzweigung**, wobei der Stufe ' Projektdetails ' in der Phase erstellen aktuell ist. Der Verwaltungsphase zeigt in einem Licht blauer Farbe, die angibt, Phase noch nicht aktiv ist.
    
    **Abbildung 17. Der Workflow wird fortgesetzt, die Stufe ' Projektdetails ' ist die Kosten weniger als 25.000**

    ![Workflowstatus in der Stufe ' Projektdetails '] (media/pj15_CreateWorkflowSPD_ProjectDetailsStage.gif "Workflowstatus in der Stufe ' Projektdetails '")
  
6. Wenn Sie auf der Stufe ' Projektdetails ' zur nächsten Folie gewechselt, sind es keine zusätzlichen Daten in der Standardseite hinzu. Wählen Sie **Submit** erneut, um der Ausführungsphase anzuzeigen (siehe Abbildung 18). 
    
    **Abbildung 18. Der Workflow ist bereit, in der Ausführungsphase verwalten**

    ![Workflowstatus in der Ausführungsphase] (media/pj15_CreateWorkflowSPD_ExecutionStage.gif "Workflowstatus in der Ausführungsphase")
  
In der Stufe ' Projektdetails ' wartet der Workflow nicht auf Submit-Ereignis. Wenn das Projekt Details PDP zusätzliche erforderliche Felder enthält, wartet die Project Server, bis Sie Daten in die Felder hinzufügen, bevor Sie mit der Ausführungsphase fortfahren. Gemäß der Definition in der Verzweigungsworkflow wartet der Ausführungsphase auch nicht auf Submit-Ereignis. In der Ausführungsphase können Sie das Projekt als Projektmanager bearbeiten oder wählen Sie auf der Registerkarte **Projekt** im Menüband **Schließen** . Wenn Sie **Schließen**auswählen, können Sie im Projekt überprüfen und später bearbeiten oder lassen Sie das Projekt ausgecheckt.

Das **Verzweigungsworkflow** -Projekt ist ein einfaches Beispiel, das nur ein Vergleich testen verfügt. Der Workflow wird in drei Phasen in der Phase erstellen und einer Phase in der Verwaltungsphase Demand Management. Um einen Workflow sorgfältig zu testen, sollten Sie alle in den Zweigstellen des Workflows testen und extreme und typische Werte verwenden, um festzustellen, ob das Verhalten ist wie erwartet. 

<a name="pj15_CreateWorkflowSPD_ImportingVromVisio"> </a>

## <a name="importing-a-workflow-from-visio"></a>Importieren eines Workflows aus Visio

Um den Workflow zu ändern, können Sie erstellen oder Ändern von Workflow gesteuerte, benutzerdefinierte Felder und erstellen oder ändern Workflowphasen und-Stufen. SharePoint Designer 2013 können Sie das Hinzufügen von Bedingungen, Aktionen, Schleifen und Phasen, und klicken Sie dann speichern und erneutes Veröffentlichen des Workflows. Um wiederverwenden, oder behalten Sie eine Sicherung eines Workflows, können Sie es in Visio 2013-Datei exportieren. 
  
Sie können auch erstellen oder bearbeiten den Workflow in Visio 2013 und die Datei für die Verwendung von Project Web App in SharePoint Designer 2013 importieren. Um eine unveränderte Workflow zu verwenden, muss die Project Web App-Instanz Phase Workfloweigenschaften enthalten, die die gleichen, die in der ursprünglichen Project Web App-Instanz sind. Weitere Informationen zur Verwendung von Visio zum von Workflows erstellen können finden Sie unter [Entwickeln von Workflows in SharePoint Designer 2013 und Visio 2013](http://msdn.microsoft.com/en-us/library/jj163272%28office.15%29.aspx).
  
> [!NOTE]
> Beim Importieren einer Visio 2013-Datei in eine andere Instanz von Project Web App haben die Phasen verschiedenen Phasen GUIDs, auch wenn die Phase Namen identisch sind. Nachdem Sie den Workflow importiert haben, müssen Sie die Eigenschaften Stufe und Aktion um Werte verwenden, die speziell für die Project Web App-Instanz konfigurieren. 
> 
> Wenn Sie einen Workflow in Visio 2013 erstellen, haben die Phasen und Aktionen keine Eigenschaften, die spezifisch für eine Project Web App-Instanz sind, weil Visio keine Verbindung mit Project Web App hergestellt wird. Beim Verbinden von SharePoint Designer 2013 mit Project Web App erstellen Sie einen Workflow, und klicken Sie dann die VSDX-Datei importieren, überschreiben Sie den aktiven Workflow. Sie müssen die Eigenschaften Stufe und Aktion um den Werten entsprechen, die SharePoint Designer 2013 aus Project Web App ruft konfigurieren. 
  
### <a name="to-import-a-workflow-from-visio-to-sharepoint-designer"></a>So importieren Sie einen Workflow aus Visio in SharePoint Designer

1. Erstellen Sie einen einfachen Workflow in Visio 2013. Führen Sie beispielsweise die folgenden Schritte aus:
    
   1. Öffnen Sie Visio, und klicken Sie dann erstellen Sie einen Workflow. Wählen Sie im Bereich **Kategorien** für einen neuen Workflow, wählen Sie **Flussdiagramm**, wählen Sie die Vorlage für **Microsoft SharePoint 2013-Workflow** im Bereich **neu** , und wählen Sie dann auf **Erstellen**. Der Workflow wird mit einem Phasen-Shape mit der **Stufe 1**. Der Workflow enthält eine Komponente starten und eine EINGABETASTE Form und Ausgangs-Shape als Teil der Phasen-Shape.
    
      Wenn Sie mit dem Mauszeiger des Phasen-Shapes, und wählen Sie das Symbol **Eigenschaften** , wird die Auswahl deaktiviert. Sie können die Eigenschaften Stufe und Aktion festlegen, nachdem Sie das Workflowdiagramm in SharePoint Designer 2013 importieren. 
    
      > [!NOTE]
      >  Sie sollten nur die folgenden Shape-Schablonen in der Liste der Flussdiagramm-Shapes verwenden: 
      > - **Aktionen – SharePoint 2013-Workflow**
      > - **Komponenten – SharePoint 2013-Workflow**
      > - **Bedingungen – SharePoint 2013-Workflow**
  
   2. Klicken Sie im Bereich **Shapes** wählen Sie **Quick-Shapes aus**, und ziehen Sie dann die Form ' Bedingung ' mit der Bezeichnung **Wenn beliebiger Wert Wert gleich** rechts neben das Phasen-Shape. 
    
   3. Auf der Registerkarte **Start** des Menübands, wählen Sie das **Verbinder** -Tool aus, und klicken Sie dann das Ausgangs-Shape in der Phase mit dem Bedingungs-Shape verbinden (siehe Abbildung 19). 
    
      **Abbildung 19. Herstellen einer Verbindung mit einem Phasen-Shape mit einer Form ' Bedingung ' in einem Workflow Visio-Diagramm**

      ![Erstellen eines Workflowdiagramms in Visio] (media/pj15_CreateWorkflowSPD_NewVisioWorkflow.gif "Erstellen eines Workflowdiagramms in Visio")
  
   4. Ziehen Sie zwei weitere Phasen-Shapes rechts von der Form ' Bedingung ' aus. Die Shapes heißen **Phase 2** und **Schritt 3**.
    
   5. Verbinden Sie im rechten Teil der Form ' Bedingung ' über das **Verbinder** -Tool mit der EINGABETASTE Form der **Stufe 2**. Wählen Sie **das Zeigertool** , doppelklicken Sie auf die Verbindung zum Anzeigen eines TextBox-Objekts für den Namen, und nennen Sie die Verbindung Ja.
    
   6. Verbinden Sie den unteren Rand der Form ' Bedingung ' mit der EINGABETASTE Form der **Stufe 3**. Mit dem Tool **Zeiger** mit der rechten Maustaste der Verbindungs, und wählen Sie dann auf **Nein**. Entweder-Methode funktioniert für die Benennung von Konnektoren für der **Ja** oder **Nein**.
    
   7. Klicken Sie im Bereich **Shapes** shapesaktionen **– SharePoint 2013-Workflow**aus, und ziehen Sie dann die Aktion zum **Warten auf Projektereignis** in der Mitte des Shapes für **Phase 1** (siehe Abbildung 20). 
    
      **Abbildung 20. Abschließen des Workflows in Visio**

      ![Abschließen des Workflows in Visio] (media/pj15_CreateWorkflowSPD_CompletedVisioWorkflow.gif "Abschließen des Workflows in Visio")
  
   8. Wählen Sie auf der Registerkarte **Vorgang** im Menüband in der Gruppe **Diagrammüberprüfungdiagramm** **Überprüfen**aus. Beheben Sie alle Fehler, und speichern Sie die Zeichnung. Nennen Sie beispielsweise die Datei Testen des Workflows aus Visio.vsdx.
    
      Informationen zum Beheben von workflowfehlern finden Sie unter [Problembehandlung bei SharePoint Server 2013-workflowvalidierungsfehlern in Visio 2013](http://msdn.microsoft.com/en-us/library/jj163971%28v=office.15%29.aspx).
    
2. Öffnen Sie SharePoint Designer 2013, und öffnen Sie die gleiche Project Web App-Website, die Sie für das **Verzweigungsworkflow** -Beispiel verwendet. 
    
3. Wählen Sie im **Navigationsbereich** **Workflows** aus, und erstellen Sie einen Website-Workflow (Wählen Sie auf der Registerkarte **WORKFLOWS** des Menübands **Website-Workflow** ). Nennen Sie beispielsweise den Workflow einfacher Workflow aus Visio.
    
   Im Dialogfeld **Website-Workflow erstellen** stellen Sie sicher, dass der Plattformtyp **SharePoint 2013-Workflow - Project Server**ist. Wählen Sie **Erstellen**aus, und SharePoint Designer wird geöffnet, den **textbasierten** Bereich für den neuen Workflow. 
    
4. Wählen Sie in der Gruppe **Verwalten** auf der Registerkarte **WORKFLOW** des Menübands **Workflow-Einstellungen**.
    
5. Wählen Sie in der Gruppe **Verwalten** auf der Registerkarte **WORKFLOWEINSTELLUNGEN** des Menübands **aus Visio importieren**aus, und klicken Sie dann importieren Sie die **Testen des Workflows aus Visio.vsdx** -Datei, die Sie zuvor gespeichert haben. Ein **Microsoft SharePoint Designer** -Dialogfeld darauf hingewiesen, dass das zu importierende Diagramm keine Workfloweigenschaften enthält und gefragt, ob den aktuellen Workflow überschrieben werden. Wählen Sie auf **Ja**. SharePoint Designer importiert das Workflowdiagramm, generiert-Schablonen für Formen und zeigt den **Visual Designer** -Bereich, der des importierten Workflows enthält. 
    
6. Legen Sie die Eigenschaften jeder Form Phase im Workflow. Beispielsweise wird die erste Phase Form **Phase 1 (ungültig)**, mit der, da es keine gültige Phase in der verbundenen Project Web App-Instanz darstellt. Wenn Sie wählen oder bewegen Sie den Mauszeiger über die Phase, können Sie das Symbol **Eigenschaften** unten links der Phase Form anzeigen im Dialogfeld **Eigenschaften von Phase** im Feld (siehe Abbildung 21). Wählen Sie die **Ursprüngliche Vorschlagsdetails** Phase in der **Phase des** Dropdown-Liste, und wählen Sie dann auf **OK**. SharePoint Designer benennt die Phase an.
    
   **Abbildung 21. Festlegen der Stufe-Eigenschaft in SharePoint Designer**

   ![Festlegen von Eigenschaften in einem importierten workflow] (media/pj15_CreateWorkflowSPD_ImportFromVisio1.gif "Festlegen von Eigenschaften in einem importierten workflow")
  
   Legen Sie für die zweite Stufe der **Projektstufe** -Eigenschaft auf **Automatische Ablehnung**. Legen Sie für die dritte Phase der **Projektstufe** -Eigenschaft auf **Ausführung**.
    
7. Legen Sie auf ähnliche Weise für die Aktion **Warten auf Projektereignis** Eigenschaft **Ereignisname** auf **Ereignis: Wenn ein Projekt eingereicht wird fest**.
    
8. In ähnlicher Weise Festlegen der Eigenschaften der Bedingung **Wenn beliebiger Wert gleich Wert ist** . Legen Sie beispielsweise die erste **Value** -Eigenschaft auf **Projekt Projektdaten: Vorschlagskosten**. Legen Sie die **Operator** -Eigenschaft auf **ist kleiner als**. Legen Sie die zweite **Value** -Eigenschaft auf 5000.
    
9. Überprüfen Sie den Workflow auf Fehler, und speichern Sie den Workflow. Wenn keine Fehler aufgetreten sind, können Sie die Ansicht ändern, in den **textbasierter Designer** (siehe Abbildung 22). 
    
   **Abbildung 22. Anzeigen des importierten Workflows im textbasierten Designer**

   ![Anzeigen des importierten Workflows] (media/pj15_CreateWorkflowSPD_WorkflowFromVisio.gif "Anzeigen des importierten Workflows")
  
10. Veröffentlichen Sie den Workflow. Wenn Sie den Workflow speichern, aber nicht veröffentlichen, ist der Workflow nicht verfügbar, wenn Sie einen Enterprise-Projekttyp erstellen.
    
11. So testen Sie die importierten **einfacher Workflow aus Visio** in Project Web App erstellen Sie eine EPT, die vom Workflow verwendet, und klicken Sie dann erstellen Sie Projekte, die die neue EPT verwenden, wie Sie für das **Verzweigungsworkflow** -Beispiel. In diesem Fall werden, jedoch Projekte, die kleiner als 5.000 $ Kosten sind abgelehnt. 
    
In durcharbeiten in diesem Artikel, erstellt und getestet einen einfachen verzweigungsworkflow mithilfe von SharePoint Designer 2013 zum direkten Festlegen der Phasen, Bedingungen und Aktionen, die vom Workflow verwendet. Sie erstellt ein Diagramm für eine noch einfacher verzweigungsworkflow auch mithilfe von Visio 2013. Sie importiert das Visio-Workflowdiagramm in SharePoint Designer 2013, in dem Sie die Eigenschaften der einzelnen Phasen, Bedingung und Aktion aus die Verbindung mit Project Web App festlegen.
  
Visio 2013 und SharePoint Designer bieten zusammen komfortable Möglichkeiten für Entwickler, Projektmanager, Workflowentwickler und Tester erstellen, freigeben und Anpassen von Workflow-Entwürfe für die verschiedenen Installationen von Project Server 2013 und Project Online. Für Workflows, die programmgesteuerten Zugriff auf Project Server erforderlich, die SharePoint Designer nicht bereitstellt, können Sie mit dem clientseitigen Objektmodell (CSOM) Visual Studio 2012.
  
## <a name="see-also"></a>Siehe auch

- [Architektur von Project Server 2013](project-server-2013-architecture.md)
- [Start: Einrichten und Konfigurieren von SharePoint 2013-Workflow-Manager](http://msdn.microsoft.com/en-us/library/jj163276%28office.15%29.aspx)
- [Grundlegendes zu packen und POST von Workflows in SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj819316%28office.15%29.aspx)
- [Workflows in SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163986%28office.15%29.aspx)
- [Workflowentwicklung in SharePoint Designer 2013 und Visio 2013](http://msdn.microsoft.com/en-us/library/jj163272%28office.15%29.aspx)
- [Problembehandlung bei SharePoint Server 2013-workflowvalidierungsfehlern in Visio 2013](http://msdn.microsoft.com/en-us/library/jj163971%28v=office.15%29.aspx)
- [Workflow- und Projektbedarfsmanagement](http://msdn.microsoft.com/library/cf7433a3-a531-4467-ac0c-df0c5d6881ae%28Office.15%29.aspx)

