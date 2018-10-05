---
title: Erstellen eines Project Server-Workflows für das bedarfsmanagement
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: b0e4a3b3-d1df-454d-b74c-b980b0b456f6
description: In diesem Artikel wird beschrieben, wie zum Erstellen eines einfachen Workflows mithilfe von SharePoint Designer 2013.
ms.openlocfilehash: bbefc5d30ccb508a24c32fe41e733e6e8187ecd9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388301"
---
# <a name="create-a-project-server-workflow-for-demand-management"></a>Erstellen eines Project Server-Workflows für das bedarfsmanagement

In diesem Artikel wird beschrieben, wie zum Erstellen eines einfachen Workflows mithilfe von SharePoint Designer 2013. Exportieren von Workflows in Visio 2013 für Visualisierung und zum Bearbeiten, oder Verwenden von Visio 2013 Design Project Server 2013-Workflows, und den Entwurf für die Veröffentlichung zu Project Web App in SharePoint Designer 2013 importieren. Weitere Informationen zu der SharePoint-Workflow-Plattform und Erstellen von Workflows mit Visio 2013 und SharePoint Designer 2013 finden Sie unter [Workflows in SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx) Artikel in der SharePoint 2013-Entwicklerdokumentation. 
  
Informationen zur Vorbereitung von Project Server für Workflows finden Sie unter [starten: Legen Sie einrichten und Konfigurieren von SharePoint 2013-Workflow-Manager](https://msdn.microsoft.com/library/jj163276%28office.15%29.aspx).

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

Bevor Sie SharePoint Designer 2013 zum Erstellen eines Project Server-Workflows verwenden können, muss der Workflow-Manager-Client 1.0-Dienst für die Project Server 2013-Workflow-Aktivitäten verwenden konfiguriert werden. Informationen zur Konfiguration von Workflow-Manager-Client 1.0 finden Sie unter [Workflows in SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx) Artikel in der Entwicklerdokumentation für SharePoint Server 2013. 
  
Das folgende detaillierte Verfahren umfasst die gleichen Schritte wie im Abschnitt [Erstellen eines allgemeinen Workflows](#pj15_CreateWorkflowSPD_General) . 
  
### <a name="to-create-a-project-server-branching-workflow-detailed-procedure"></a>So erstellen Sie einen Project Server-Verzweigungsworkflow (ausführliches Verfahren)

#### <a name="1-plan-and-design-the-workflow"></a>1. planen Sie und Entwerfen Sie des Workflows.

Project Server-Workflows mit mehreren integrieren kann Stufen und Phasen in einem projektbedarfsmanagement Prozess. Da Workflows komplex sein können, müssen Sie verstehen die geschäftlichen Anforderungen und Planen Sie einen Workflow sorgfältig. Entwerfen Sie für ein einfaches Beispiel einen verzweigungsworkflow, der die geschätzte Kosten für einen Projektvorschlag verwendet, um zu bestimmen, ob das Angebot akzeptiert wird. Wenn die geschätzte Kosten größer ist als 25.000 USD, Ablehnen des Vorschlags; Sie andernfalls annehmen Sie den Vorschlag, und erstellen Sie ein Projekt.
    
Da Sie können Visio 2013 und SharePoint Designer 2013 zum Entwerfen und Erstellen von Workflows für Project Server 2013, können Sie leichter mit Workflows experimentieren, als mit Project Server 2010 möglich ist. Der Workflow Beispielentwurf in diesem Artikel wird genauso wie in den Artikel [Erstellen eines verzweigungsworkflows Workflows](https://msdn.microsoft.com/library/a02cafdc-d881-4271-b446-d8b2cd456a52%28Office.15%29.aspx) in Project 2010-SDK. Beim Entwerfen und erstellen Sie einen Workflow Test auf einem Remotecomputer mit einer Testinstanz von Project Web App können – Sie müssen nicht direkt auf einem Computer Project Server 2013 Workflows erstellen. 
    
#### <a name="2-create-the-entities-that-your-workflow-requires"></a>2. Erstellen der Entitäten, die den Workflow erforderlich.

Überprüfen Sie in Project Web App die verfügbaren Workflowphasen und Phasen und benutzerdefinierten Enterprise-Feldern, die verfügbar sind. Erstellen Sie bei Bedarf die Entitäten, die den Workflow erforderlich, wie in der folgenden Schritte aus:
    
1. **Workflowphasen** Die Standardinstallation von Project Web App enthält die erstellen, auswählen, planen, verwalten und nach Abschluss des Vorgangs Phasen. Für die Verzweigung Workflowbeispiel müssen Sie keinen anderen Phasen zu erstellen. 
        
2. **Benutzerdefinierte Enterprise-Felder** Die verzweigungsworkflow erfordert ein Projekt Kosten benutzerdefiniertes Feld, das Workflow gesteuert wird. Der Wert eines benutzerdefinierten Felds Workflow gesteuert wird auf einer Projektdetailseite festgelegt, die vom Workflow verwendet. Wählen Sie beispielsweise das Symbol **Einstellungen** in der oberen rechten einer Project Web App-Seite, wählen Sie **PWA-Einstellungen**, und wählen Sie dann **benutzerdefinierte Enterprise-Felder und Nachschlagetabellen**.
        
   Erstellen eines benutzerdefinierten Felds mit dem Namen Vorschlagskosten für die **Project** -Entität, und wählen Sie den **Kosten**. Geben Sie die Beschreibung Kosten für einen Projektvorschlag geschätzt. Wählen Sie im Abschnitt **Verhalten** **Verhalten vom Workflow gesteuert**.
        
3. **Projektdetailseiten** Bearbeiten Sie oder erstellen Sie die PDPs, die die Workflowphasen verwendet werden soll. Führen Sie beispielsweise die folgenden Schritte aus: 
        
    1. Wählen Sie auf der Seite mit den Servereinstellungen **Projektdetailseiten** und dann die Projektdetailseite **ProjectInformation** aus. 
            
    2. Wählen Sie im Menüband auf der Registerkarte **SEITE** in der Gruppe **Bearbeiten****Seite bearbeiten** aus.
            
    3. Wählen Sie den Pfeil nach unten in der oberen rechten des **Grundlegenden Info** -Webparts aus, und wählen Sie dann auf **Webpart bearbeiten**. Oder wählen Sie auf der Registerkarte **Webpart** im Menüband in der Gruppe **Eigenschaften** **-Webpart-Eigenschaften** -Editor-Webpart angezeigt. 
            
    4. Wählen Sie im Abschnitt **Angezeigte Projektfelder** des Bearbeitungs-Webparts (siehe Abbildung 1) **Ändern** aus.
            
    5. Fügen Sie das benutzerdefinierte Feld **Vorschlagskosten** , verschieben Sie diese über das Feld **Besitzer** in der Liste **Ausgewählte Projektfelder** , und klicken Sie dann auf **OK** (siehe Abbildung 1).
      
    6. Wählen Sie im Bearbeitungs-Webpart **OK** und dann im Menüband auf der Registerkarte **SEITE** in der Gruppe **Bearbeiten****Bearbeitung beenden** aus. In Abbildung 2 ist das benutzerdefinierte Feld **Proposal Cost** dargestellt, das der Projektdetailseite "Projektinformationen" hinzugefügt wurde. 

    **Abbildung 1. Bearbeiten des Projektfelder-Webparts auf einer Projektdetailseite**

    ![Bearbeiten der Felder für die Project-Webpart auf einer Projektdetailseite] (media/pj15_CreateWorkflowSPD_EditPDP.gif "Bearbeiten der Felder für die Project-Webpart auf einer Projektdetailseite")

    **Abbildung 2. Die bearbeitete Projektdetailseite enthält das benutzerdefinierte Feld "Vorschlagskosten"**

    ![Die bearbeitete PDP beinhaltet das Feld Vorschlagskosten] (media/pj15_CreateWorkflowSPD_EditedPDP.gif "Die bearbeitete PDP beinhaltet das Feld Vorschlagskosten")
  
4. **Workflowstufen** Erstellen Sie die Phasen, die für die einzelnen Phasen des Workflows erforderlich sind. Klicken Sie auf der Seite servereinstellungen wählen Sie **Workflowstufen aus**, und wählen Sie dann auf **Neue WORKFLOWSTUFE**. Abbildung 3 zeigt einen Teil der Seite Workflowstufe hinzufügen.
    
    **Abbildung 3. Hinzufügen einer Workflowstufe in Project Web App**

    ![Hinzufügen einer Workflowphase in Project Web App] (media/pj15_CreateWorkflowSPD_AddWorkflowStage.gif "Hinzufügen einer Workflowphase in Project Web App")
  
    Das Verzweigen Workflowbeispiel verwendet die vier Stufen, die in Tabelle 1 aufgeführt sind. Im Abschnitt **Zusätzliche Einstellungen für sichtbare Projektdetailseite** Seitenrand Workflowstufe hinzufügen (nicht in Abbildung 3 dargestellt) sind die Werte optional. Sie bieten weitere Informationen auf der Seite Workflowstatus. Beispielsweise, da die anfängliche Vorschlag Details PDP Benutzereingaben erforderlich sind, können Sie das Kontrollkästchen **der Projektdetailseite Aufmerksamkeit** , und fügen Sie eine bestimmte Beschreibung wie legen Sie den Namen des Projekts und Kosten für diese PDP.
    
    In Abbildung 4 sind die vier Stufen abgebildet, die auf der Seite "Workflowstufen" durchlaufen werden.
    
    **Tabelle 2. Stufen des Verzweigungsworkflows**

    |Name|Beschreibung|Beschreibung für Einreichung|Phase|Sichtbare PDPs|Benutzerdefinierte Felder|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |Ursprüngliche Vorschlagsdetails  <br/> |Legen Sie den Projektnamen und die Kosten fest.  <br/> |Reichen Sie das Projekt als Vorschlag ein.  <br/> |Erstellen  <br/> |Projektinformationen  <br/> Projektdetails  <br/> |Vorschlagskosten (erforderlich)  <br/> |
    |Projektdetails  <br/> |Geben Sie nähere Informationen zum vorgeschlagenen Projekt an.  <br/> |Senden Sie die Details ab, um mit dem Projekt fortzufahren.  <br/> |Erstellen  <br/> |Projektinformationen  <br/> Projektdetails  <br/> |Vorschlagskosten (schreibgeschützt)  <br/> |
    |Automatische Ablehnung  <br/> |Der Vorschlag wird auf Grundlage der angegebenen Informationen abgelehnt.  <br/> | <br/> |Erstellen  <br/> |Projektinformationen  <br/> |Vorschlagskosten (schreibgeschützt)  <br/> |
    |Ausführung  <br/> |Der Vorschlag wurde angenommen und ist bereit für das Projektmanagement.  <br/> | <br/> |Verwalten  <br/> |Projektinformationen  <br/> Projektdetails  <br/> |Vorschlagskosten (schreibgeschützt)  <br/> |
   
    **Abbildung 4. Liste der Workflowstufen in Project Web App**

    ![Liste der Workflowphasen in Project Web App] (media/pj15_CreateWorkflowSPD_WorkflowStages.gif "Liste der Workflowphasen in Project Web App")
  
#### <a name="3-construct-the-workflow-in-the-text-based-designer"></a>3. erstellen Sie den Workflow im textbasierten Designer.

Erstellen Sie den Workflow in SharePoint Designer 2013 mithilfe deklarative Anweisungen im textbasierten Designer. Starten Sie Sie an die orangefarbene Einfügelinie abzurufenden kontextbezogene AutoVervollständigen-Anweisungen für die Workflowlogik und Schritte eingeben, oder Sie können die Logik und die Schritte in der Gruppe **Einfügen** auf der Registerkarte **WORKFLOW** des Menübands mithilfe von Inhaltssteuerelementen einfügen. 
    
1. Wählen Sie in der Backstage-Ansicht von SharePoint Designer 2013 **Website öffnen**. Öffnen Sie beispielsweise `https://ServerName/pwa`. Wählen Sie im **Navigationsbereich** **Workflows**aus. Wählen Sie dann auf der Registerkarte **WORKFLOWS** des Menübands in der Gruppe **neu** **Website-Workflow**. In diesem Beispiel nennen Sie den Workflow Verzweigung Workflow. Stellen Sie sicher, dass **SharePoint 2013-Workflow - Project Server** in der Dropdownliste **Plattformtyp** aktiviert ist (siehe Abbildung 5). 
    
    **Abbildung 5. Erstellen eines Project Server-Websiteworkflows**

    ![Erstellen eines Project Server-Website-Workflows] (media/pj15_CreateWorkflowSPD_CreateSiteWorkflow.gif "Erstellen eines Project Server-Website-Workflows")
  
2. Wählen Sie die Registerkarte **Verzweigungsworkflow** aus. Wählen Sie dann im Menüband auf der Registerkarte **WORKFLOW** in der Gruppe **Verwalten** in der Dropdownliste **Ansichten****Textbasierter Designer** aus. Klicken Sie in die Ansicht, um die Ansicht mit der blinkenden orangefarbenen Einfügelinie anzuzeigen (siehe Abbildung 6).
    
    **Abbildung 6. Verwenden der Ansicht "Textbasierter Designer" für den Workflow**

    ![Verwenden der textbasierten Designer-Ansicht] (media/pj15_CreateWorkflowSPD_TextBasedDesigner.gif "Verwenden der textbasierten Designer-Ansicht")
  
3. Fügen Sie in der Ansicht **Textbasierter Designer** die Stufen hinzu, die im Workflow verwendet werden. Wählen Sie im Menüband auf der Registerkarte **WORKFLOW** in der Gruppe **Einfügen** in der Dropdownliste **Stufe** unter **Erstellen****Ursprüngliche Vorschlagsdetails** aus.
    
    Platzieren Sie die orangefarbene Einfügelinie entsprechend unterhalb des Felds **Stufe: Ursprüngliche Vorschlagsdetails**, und fügen Sie die anderen Stufen hinzu, die vom Workflow verwendet werden: **Projektdetails**, **Automatische Ablehnung** und **Ausführung** (siehe Abbildung 7). 
    
    **Abbildung 7. Hinzufügen einer Stufe zu einem Workflow in SharePoint Designer**

    ![Hinzufügen einer Stufe zu einem Workflow in SPD] (media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Hinzufügen einer Stufe zu einem Workflow in SPD")
  
4. Fügen Sie in jeder Phase die Workflowschritte und die Workflowlogik hinzu: 
    
    1. Platzieren Sie in der Phase **Ursprüngliche Vorschlagsdetails** die orangefarbene Einfügelinie über dem Phasentext. Wählen Sie im Menüband in der Gruppe **Einfügen****Aktion** aus, blättern Sie nach unten zu **Project Web App-Aktionen**, und wählen Sie dann **Auf Projektereignis warten** aus. Wählen Sie **Dieses Projektereignis** und dann in der Dropdownliste **Ereignis: Wenn ein Projekt eingereicht wird** aus. 
    
    2. Fügen Sie im Abschnitt **Übergang in Phase** der Phase **Ursprüngliche Vorschlagsdetails****Wenn ein beliebiger Wert gleich dem Wert ist** ein. Sie können mit der Eingabe der Anweisung beginnen oder auf dem Menüband in der Gruppe **Einfügen** das Steuerelement **Bedingung** verwenden. 
    
    3. Wählen Sie das erste **value**-Steuerelement und dann **fx** aus, um das Dialogfeld **Workflow-Nachschlagevorgang definieren** anzuzeigen (siehe Abbildung 8). Wählen Sie in der Dropdownliste **Datenquelle****Projektdaten** aus. Wählen Sie in der Dropdownliste **Quellenfeld****Vorschlagskosten** aus.
    
       **Abbildung 8. Definieren eines Nachschlagewerts im Workflow**

       ![Definieren eines Suchwerts im workflow] (media/pj15_CreateWorkflowSPD_DefineWorkflowLookup.gif "Definieren eines Suchwerts im workflow")
  
    4. Führen Sie die `If` Anweisung, sodass dieser Folgendes angezeigt wird: **Wenn Project Projektdaten: Vorschlagskosten höher sind als 25000**
    
       > [!NOTE]
       > Alternativ könnten Sie eine Workflowvariable erstellen, die Variable auf den benutzerdefinierten Feldwert festlegen und dann die Variable mit einem Wert vergleichen. Erstellen Sie z. B. aus der Dropdownliste **Lokale Variablen** auf dem Menüband eine Variable mit der Bezeichnung **TotalCost** (keine Leerzeichen) des Typs **Number**. Wählen Sie im Dialogfeld **Workflow-Nachschlagevorgang definieren** für die Datenquelle **Workflowvariablen und -parameter** aus, und wählen Sie dann als das Feld **Variable: Gesamtkosten** aus. Die **If**-Anweisung würde dann lauten: **Wenn Variable: Gesamtkosten höher sind als 25000**
  
    5. Platzieren Sie die orangefarbene Einfügelinie innerhalb der `If` verzweigen, und fügen Sie dann mithilfe des **Aktion** -Steuerelements in der Gruppe " **Einfügen** " auf dem Menüband **eine Stufe** . Wählen Sie das **Stufen** Dropdown-Steuerelement, und wählen Sie die Phase der **Automatischen Ablehnung** . 
    
       In ähnlicher Weise in der `Else` verzweigen, **Wechseln Sie zur Projektdetails** -Anweisung einfügen. Abbildung 9 zeigt die abgeschlossene **Ursprüngliche Vorschlagsdetails** Phase. 
    
       **Abbildung 9. Fertige Logik für Phase "Ursprüngliche Vorschlagsdetails"**

       ![Abgeschlossene Logik für ursprüngliche Vorschlagsdetails] (media/pj15_CreateWorkflowSPD_InitialStageLogic.gif "Abgeschlossene Logik für ursprüngliche Vorschlagsdetails")
  
    6. Lassen Sie in der Phase **Automatische Ablehnung** den ersten Abschnitt leer, es sei denn, Sie möchten den Workflow anhalten und einige Daten auf einer Projektdetailseite anzeigen. Der Abschnitt **Übergang in Phase** muss einen Übergang enthalten. Da auf eine Ablehnung keine weitere Phase folgt, geben Sie als Anweisung Zum Ende des Workflows wechseln ein. 
    
    7. Fügen Sie im Abschnitt **Übergang in Phase** in der Phase **Projektdetails**Zur Ausführung wechseln hinzu. Es ist nicht erforderlich zu warten, bis ein Ereignis übermittelt wurde, es sei denn, es müssen zusätzliche Daten hinzugefügt werden, oder Sie möchten den Workflow anhalten. 
    
    8. Lassen Sie in der Phase **Ausführung** den Abschnitt mit der Phasenaktion leer, es sei denn, Sie möchten den Workflow anhalten. Fügen Sie im Abschnitt **Übergang in Phase****Zum Ende des Workflows wechseln** hinzu.
    
5. Wählen Sie auf dem Menüband in der Gruppe **Speichern****Auf Fehler prüfen** aus, um auf Workflowfehler zu prüfen (siehe Abbildung 10). Beheben Sie alle Fehler, und wählen Sie dann **Speichern** aus.
    
    **Abbildung 10. Prüfen des Workflows auf Fehler im SharePoint Designer**

    ![Überprüfen der Fehler im workflow] (media/pj15_CreateWorkflowSPD_SPDCheckForErrors.gif "Überprüfen der Fehler im workflow")
  
6. (Optional) Wählen Sie auf dem Menüband in der Gruppe **Verwalten** im Dropdownmenü **Ansichten****Visual Designer** aus. In Abbildung 11 ist die Ansicht auf 50 % verkleinert.
    
    Sie können Elemente im Workflow mit dem Visual Designer bearbeiten. Wählen Sie z. B. die Bedingung **Wenn ein beliebiger Wert gleich dem Wert ist** aus, wählen Sie unten rechts neben der Bedingung das Extras-Symbol aus, und wählen Sie dann **Wert** aus, um die Vergleichsbedingungen im Dialogfeld **Eigenschaften** anzuzeigen. 
    
    **Abbildung 11. Verwenden des Visual Designer für einen Workflow**

    ![Verwenden Sie die Visio-Entwurfsansicht des Workflows] (media/pj15_CreateWorkflowSPD_SwitchView.gif "Verwenden Sie die Visio-Entwurfsansicht des Workflows")
  
    Wenn der Workflow in der Visual Designer angezeigt wird, um speichern Sie den Workflow in einer Datei Visio 2013 (.vsdx) als Sicherung oder höher für zu verwenden, können Sie **nach Visio exportieren**.
    
7. Veröffentlichen des Workflows. Wenn Sie SharePoint Designer 2013 verwenden, um den Workflow auf der aktiven Project Web App-Website veröffentlichen, wird der Workflow für die SharePoint-Website oder in Azure registriert ist und für neue EPTs in Project Web App verfügbar wird.

#### <a name="4-create-an-ept-for-the-workflow-and-then-test-the-workflow"></a>4. erstellen ein EPT für den Workflow, und Testen Sie den Workflow.

Klicken Sie in Project Web App erstellen Sie eine EPT für den Workflow, und Testen Sie den Workflow, indem Sie einen Projektvorschlag erstellen:
    
1. Klicken Sie auf der Seite Einstellungen für PWA wählen Sie **Enterprise-Projekttypen**, und erstellen Sie eine EPT mit dem Namen Verzweigen Testen des Workflows. Deaktivieren Sie das Kontrollkästchen **neue Projekte als SharePoint-Aufgabenlistenprojekte erstellen** , sodass Project Server wird Vollzugriff auf Projekte verwalten, die mithilfe des EPT erstellt werden. Wählen Sie in der Dropdownliste **Website-Workflowzuordnung** **Verzweigungsworkflow** aus, und wählen Sie dann in der Dropdown-Liste **Neue Projektseite** auf der ersten Seite sein, die der Workflow zeigt die **Projektinformationen** PDP aus. 
    
    **Abbildung 12. Hinzufügen einer EPT für den Workflow**

    ![Hinzufügen eines EPT für den workflow] (media/pj15_CreateWorkflowSPD_EPTs.gif "Hinzufügen eines EPT für den workflow")
  
    > [!NOTE]
    > Ein **Ja**-Wert in der Spalte **SharePoint-Vorgangslistenprojekt** in der Tabelle der Enterprise-Projekttypen bezieht sich auf eine EPT, mit der eine SharePoint-Aufgabenliste erstellt wird, wobei die Aufgabenliste in Project Web App sichtbar ist, SharePoint aber die Kontrolle über das Projekt behält. Weitere Informationen zum Verwalten von Projekten als SharePoint-Aufgabenlisten finden Sie unter [Project Server 2013 architecture](project-server-2013-architecture.md). 
  
2. Öffnen Sie auf der Seite Projekte in Project Web App, und erstellen Sie ein Projekt mithilfe des neuen EPT (siehe Abbildung 13). Da **Verzweigen Testen des Workflows** **Verzweigungsworkflow**zugeordnet ist, wird unter Kontrolle des Workflows Erstellen eines Projekts gestartet.
    
    **Abbildung 13. Erstellen eines Projekts mit der EPT "Verzweigungsworkflow – Test"**

    ![Erstellen eines Projekts mithilfe des EPT] (media/pj15_CreateWorkflowSPD_NewProject.gif "Erstellen eines Projekts mithilfe des EPT")
  
3. Wenn der Workflow die PDP **Projektinformationen** angezeigt wird, fügen Sie die Projektfelder Daten hinzu. Geben Sie beispielsweise den **Vorschlagskosten** Wert 30000. Die englischen Version von Project Server ändert das Feld, um 30.000 $ anzeigen (siehe Abbildung 14).
    
    **Abbildung 14. Verwenden der bearbeiteten Projektdetailseite "Projektinformationen"**

    ![Verwenden der bearbeiteten Projektinformationen] (media/pj15_CreateWorkflowSPD_NewProjectStage1.gif "Verwenden der bearbeiteten Projektinformationen")
  
4. Wählen Sie im Menüband auf der Registerkarte **PROJEKT** in der Gruppe **Projekt****Speichern** aus. Project Server fügt dem Projekt die Daten auf der Projektdetailseite hinzu und zeigt dann die Seite "Workflowstatus" an (siehe Abbildung 15). Um die vollständige Beschreibung der Phase "Ursprüngliche Vorschlagsdetails" im Workflowstatusdiagramm anzuzeigen, bewegen Sie den Mauszeiger im Workflowvisualisierungsdiagramm über die Phase.
    
    Im Raster **Alle Workflowphasen** wird mithilfe eines grünen Pfeils angegeben, dass für die Phase "Ursprüngliche Vorschlagsdetails" eine Benutzereingabe erwartet wird. Der Grund dafür ist, dass der Workflow in der Phase "Ursprüngliche Vorschlagsdetails" auf ein Einreichereignis wartet. Wenn der Workflow nicht auf ein Einreichereignis warten würde, könnten Sie in der Gruppe **Seite****Weiter** auswählen, um zur nächsten Projektdetailseite zu wechseln. 
    
    **Abbildung 15. Verwenden der Seite "Workflowstatus" in der Phase "Ursprüngliche Vorschlagsdetails"**

    ![Workflow-Statusseite nach der ersten Stufe] (media/pj15_CreateWorkflowSPD_NewProjectStage1Status.gif "Workflow-Statusseite nach der ersten Stufe")
  
    Im Workflowvisualisierungsdiagramm wird die aktuelle Phase in grün angezeigt. In der Phase **Erstellen** stellt die Phase "Ursprüngliche Vorschlagsdetails" die aktuelle Phase dar. 
    
5. Wählen Sie auf dem Menüband in der Gruppe **Workflow****Einreichen** aus.
    
    > [!TIP]
    > Aktualisieren Sie die Seite, wenn das Steuerelement **Einreichen** deaktiviert ist. 
  
    Wenn der Wert **Vorschlagskosten** höher ist als 25.000 USD, wechselt der Workflow zur Phase "Automatische Ablehnung". In Abbildung 16 ist der Status "Automatische Ablehnung" dargestellt, wenn Sie erneut **Einreichen** auswählen. Wenn die **Vorschlagskosten** 25.000 USD oder weniger betragen, wechselt der Workflow zur Phase "Projektdetails" (siehe Abbildung 17). 
    
    **Abbildung 16. Der Workflow ist in der Phase "Automatische Ablehnung" abgeschlossen**

    ![Der Workflow ist in automatischer Ablehnung abgeschlossen] (media/pj15_CreateWorkflowSPD_AutomatedRejectionCompleted.gif "Der Workflow ist in automatischer Ablehnung abgeschlossen")
  
    Abbildung 17 zeigt einen weiteren Test mit einen Projektvorschlag mit dem Namen **Test 2 - Verzweigung**, wobei der Stufe ' Projektdetails ' in der Phase erstellen aktuell ist. Der Verwaltungsphase zeigt in einem Licht blauer Farbe, die angibt, Phase noch nicht aktiv ist.
    
    **Abbildung 17. Der Workflow wechselt zur Phase "Projektdetails", wenn die Kosten niedriger als 25.000 USD sind**

    ![Workflowstatus in der Stufe ' Projektdetails '] (media/pj15_CreateWorkflowSPD_ProjectDetailsStage.gif "Workflowstatus in der Stufe ' Projektdetails '")
  
6. Wenn Sie mit der Phase "Projektdetails" fortfahren, müssen auf der Standardseite keine zusätzlichen Daten hinzugefügt werden. Wählen Sie erneut **Einreichen** aus, um mit der Ausführungsphase fortzufahren (siehe Abbildung 18). 
    
    **Abbildung 18. Der Workflow ist bereit zur Verwaltung in der Ausführungsphase**

    ![Workflowstatus in der Ausführungsphase] (media/pj15_CreateWorkflowSPD_ExecutionStage.gif "Workflowstatus in der Ausführungsphase")
  
Der Workflow wartet in der Phase "Projektdetails" nicht auf ein Einreichereignis. Wenn die Projektdetailseite "Projektdetails" zusätzliche Pflichtfelder enthält, wartet Project Server, bis Sie den Feldern Daten hinzufügen, bevor zur Ausführungsphase gewechselt wird. Wie im Verzweigungsworkflow definiert, wartet auch die Ausführungsphase nicht auf ein Einreichereignis. Als Projektmanager können Sie das Projekt in der Ausführungsphase bearbeiten oder im Menüband auf der Registerkarte **PROJEKT****Schließen** auswählen. Wenn Sie **Schließen** auswählen, können Sie das Projekt einchecken und es später bearbeiten oder das Projekt ausgecheckt lassen.

Das Projekt **Verzweigungsworkflow** ist ein einfaches Beispiel mit nur einem Vergleichstest. Der Workflow umfasst in der Phase "Erstellen" drei Stufen und in der Phase "Verwalten" des Bedarfsmanagements eine Stufe. Um einen Workflow sorgfältig zu testen, sollten Sie alle Verzweigungen des Workflows testen und extreme und typische Werte verwenden, um zu sehen, ob das erwartete Verhalten auftritt. 

<a name="pj15_CreateWorkflowSPD_ImportingVromVisio"> </a>

## <a name="importing-a-workflow-from-visio"></a>Importieren eines Workflows aus Visio

Um den Workflow zu ändern, können Sie erstellen oder Ändern von Workflow gesteuerte, benutzerdefinierte Felder und erstellen oder ändern Workflowphasen und-Stufen. SharePoint Designer 2013 können Sie das Hinzufügen von Bedingungen, Aktionen, Schleifen und Phasen, und klicken Sie dann speichern und erneutes Veröffentlichen des Workflows. Um wiederverwenden, oder behalten Sie eine Sicherung eines Workflows, können Sie es in Visio 2013-Datei exportieren. 
  
Sie können auch erstellen oder bearbeiten den Workflow in Visio 2013 und die Datei für die Verwendung von Project Web App in SharePoint Designer 2013 importieren. Um eine unveränderte Workflow zu verwenden, muss die Project Web App-Instanz Phase Workfloweigenschaften enthalten, die die gleichen, die in der ursprünglichen Project Web App-Instanz sind. Weitere Informationen zur Verwendung von Visio zum von Workflows erstellen können finden Sie unter [Entwickeln von Workflows in SharePoint Designer 2013 und Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx).
  
> [!NOTE]
> Beim Importieren einer Visio 2013-Datei in eine andere Instanz von Project Web App haben die Phasen verschiedenen Phasen GUIDs, auch wenn die Phase Namen identisch sind. Nachdem Sie den Workflow importiert haben, müssen Sie die Eigenschaften Stufe und Aktion um Werte verwenden, die speziell für die Project Web App-Instanz konfigurieren. 
> 
> Wenn Sie einen Workflow in Visio 2013 erstellen, haben die Phasen und Aktionen keine Eigenschaften, die spezifisch für eine Project Web App-Instanz sind, weil Visio keine Verbindung mit Project Web App hergestellt wird. Beim Verbinden von SharePoint Designer 2013 mit Project Web App erstellen Sie einen Workflow, und klicken Sie dann die VSDX-Datei importieren, überschreiben Sie den aktiven Workflow. Sie müssen die Eigenschaften Stufe und Aktion um den Werten entsprechen, die SharePoint Designer 2013 aus Project Web App ruft konfigurieren. 
  
### <a name="to-import-a-workflow-from-visio-to-sharepoint-designer"></a>So importieren Sie einen Workflow aus Visio in SharePoint Designer

1. Erstellen Sie einen einfachen Workflow in Visio 2013. Führen Sie beispielsweise die folgenden Schritte aus:
    
   1. Öffnen Sie Visio, und erstellen Sie dann einen Workflow. Wählen Sie den Bereich **KATEGORIEN** für einen neuen Workflow aus. Wählen Sie **Flussdiagramm** aus, wählen Sie im Bereich **Neu** die **Microsoft SharePoint 2013-Workflow**-Vorlage aus, und wählen Sie dann **Erstellen** aus. Der Workflow wird mit einem Phasen-Shape mit der Bezeichnung **Phase 1** geöffnet. Der Workflow umfasst eine Startkomponente und als Bestandteil des Phasen-Shapes ein Eingangs-Shape und ein Ausgangs-Shape.
    
      Wenn Sie mit dem Mauszeiger des Phasen-Shapes, und wählen Sie das Symbol **Eigenschaften** , wird die Auswahl deaktiviert. Sie können die Eigenschaften Stufe und Aktion festlegen, nachdem Sie das Workflowdiagramm in SharePoint Designer 2013 importieren. 
    
      > [!NOTE]
      >  Sie sollten nur die folgenden Shape-Schablonen in der Liste der Flussdiagramm-Shapes verwenden: 
      > - **Aktionen – SharePoint 2013-Workflow**
      > - **Komponenten – SharePoint 2013-Workflow**
      > - **Bedingungen – SharePoint 2013-Workflow**
  
   2. Wählen Sie im Bereich **Shapes****Quick-Shapes** aus, und ziehen Sie das Bedingungs-Shape mit der Bezeichnung **Wenn ein beliebiger Wert gleich dem Wert ist** dann rechts neben das Phasen-Shape. 
    
   3. Wählen Sie auf dem Menüband auf der Registerkarte **HOME** das **Verbinder**-Tool aus, und verbinden Sie dann das Ausgangs-Shape in der Phase mit dem Bedingungs-Shape (siehe Abbildung 19). 
    
      **Abbildung 19. Verbinden eines Phasen-Shapes mit einem Bedingungs-Shape in einem Visio-Workflowdiagramm**

      ![Erstellen eines Workflowdiagramms in Visio] (media/pj15_CreateWorkflowSPD_NewVisioWorkflow.gif "Erstellen eines Workflowdiagramms in Visio")
  
   4. Ziehen Sie zwei weitere Phasen-Shapes rechts neben das Bedingungs-Shape. Die Shapes heißen **Phase 2** und **Phase 3**.
    
   5. Verbinden Sie im rechten Teil der Form ' Bedingung ' über das **Verbinder** -Tool mit der EINGABETASTE Form der **Stufe 2**. Wählen Sie **das Zeigertool** , doppelklicken Sie auf die Verbindung zum Anzeigen eines TextBox-Objekts für den Namen, und nennen Sie die Verbindung Ja.
    
   6. Verbinden Sie die Unterseite des Bedingungs-Shapes mit dem Eingangs-Shape von **Phase 3**. Rechtsklicken Sie mit dem **Zeigertool** auf die Verbindung, und wählen Sie dann **Nein** aus. Beide Methoden können verwendet werden, um die Verbinder mit **Ja** oder **Nein** zu benennen.
    
   7. Klicken Sie im Bereich **Shapes** shapesaktionen **– SharePoint 2013-Workflow**aus, und ziehen Sie dann die Aktion zum **Warten auf Projektereignis** in der Mitte des Shapes für **Phase 1** (siehe Abbildung 20). 
    
      **Abbildung 20. Abschließen des Workflows in Visio**

      ![Abschließen des Workflows in Visio] (media/pj15_CreateWorkflowSPD_CompletedVisioWorkflow.gif "Abschließen des Workflows in Visio")
  
   8. Wählen Sie auf der Registerkarte **Vorgang** im Menüband in der Gruppe **Diagrammüberprüfungdiagramm** **Überprüfen**aus. Beheben Sie alle Fehler, und speichern Sie die Zeichnung. Nennen Sie beispielsweise die Datei Testen des Workflows aus Visio.vsdx.
    
      Informationen zum Beheben von workflowfehlern finden Sie unter [Problembehandlung bei SharePoint Server 2013-workflowvalidierungsfehlern in Visio 2013](https://msdn.microsoft.com/library/jj163971%28v=office.15%29.aspx).
    
2. Öffnen Sie SharePoint Designer 2013, und öffnen Sie die gleiche Project Web App-Website, die Sie für das **Verzweigungsworkflow** -Beispiel verwendet. 
    
3. Wählen Sie im **Navigationsbereich** **Workflows** aus, und erstellen Sie einen Website-Workflow (Wählen Sie auf der Registerkarte **WORKFLOWS** des Menübands **Website-Workflow** ). Nennen Sie beispielsweise den Workflow einfacher Workflow aus Visio.
    
   Im Dialogfeld **Website-Workflow erstellen** stellen Sie sicher, dass der Plattformtyp **SharePoint 2013-Workflow - Project Server**ist. Wählen Sie **Erstellen**aus, und SharePoint Designer wird geöffnet, den **textbasierten** Bereich für den neuen Workflow. 
    
4. Wählen Sie im Menüband auf der Registerkarte **WORKFLOW** in der Gruppe **Verwalten****Workfloweinstellungen** aus.
    
5. Wählen Sie in der Gruppe **Verwalten** auf der Registerkarte **WORKFLOWEINSTELLUNGEN** des Menübands **aus Visio importieren**aus, und klicken Sie dann importieren Sie die **Testen des Workflows aus Visio.vsdx** -Datei, die Sie zuvor gespeichert haben. Ein **Microsoft SharePoint Designer** -Dialogfeld darauf hingewiesen, dass das zu importierende Diagramm keine Workfloweigenschaften enthält und gefragt, ob den aktuellen Workflow überschrieben werden. Wählen Sie auf **Ja**. SharePoint Designer importiert das Workflowdiagramm, generiert-Schablonen für Formen und zeigt den **Visual Designer** -Bereich, der des importierten Workflows enthält. 
    
6. Legen Sie die Eigenschaften jeder Form Phase im Workflow. Beispielsweise wird die erste Phase Form **Phase 1 (ungültig)**, mit der, da es keine gültige Phase in der verbundenen Project Web App-Instanz darstellt. Wenn Sie wählen oder bewegen Sie den Mauszeiger über die Phase, können Sie das Symbol **Eigenschaften** unten links der Phase Form anzeigen im Dialogfeld **Eigenschaften von Phase** im Feld (siehe Abbildung 21). Wählen Sie die **Ursprüngliche Vorschlagsdetails** Phase in der **Phase des** Dropdown-Liste, und wählen Sie dann auf **OK**. SharePoint Designer benennt die Phase an.
    
   **Abbildung 21. Festlegen der Phaseneigenschaft in SharePoint Designer**

   ![Festlegen von Eigenschaften in einem importierten workflow] (media/pj15_CreateWorkflowSPD_ImportFromVisio1.gif "Festlegen von Eigenschaften in einem importierten workflow")
  
   Legen Sie bei der zweiten Phase die Eigenschaft **Projektphase** auf **Automatische Ablehnung** fest. Legen Sie die Eigenschaft **Projektphase** bei der dritten Phase auf **Ausführung** fest.
    
7. Legen Sie entsprechend bei der Aktion **Auf Projektereignis warten** die Eigenschaft **Ereignisname** auf **Ereignis: Wenn ein Projekt eingereicht wird** fest.
    
8. In ähnlicher Weise Festlegen der Eigenschaften der Bedingung **Wenn beliebiger Wert gleich Wert ist** . Legen Sie beispielsweise die erste **Value** -Eigenschaft auf **Projekt Projektdaten: Vorschlagskosten**. Legen Sie die **Operator** -Eigenschaft auf **ist kleiner als**. Legen Sie die zweite **Value** -Eigenschaft auf 5000.
    
9. Prüfen Sie den Workflow auf Fehler, und speichern Sie dann den Workflow. Falls Fehler vorhanden sind, können Sie zur Ansicht **Textbasierter Designer** wechseln (siehe Abbildung 22). 
    
   **Abbildung 22. Anzeigen des importierten Workflows im textbasierten Designer**

   ![Anzeigen des importierten Workflows] (media/pj15_CreateWorkflowSPD_WorkflowFromVisio.gif "Anzeigen des importierten Workflows")
  
10. Veröffentlichen Sie den Workflow. Wenn Sie den Workflow speichern, aber nicht veröffentlichen, ist der Workflow nicht verfügbar, wenn Sie einen Enterprise-Projekttyp erstellen.
    
11. So testen Sie die importierten **einfacher Workflow aus Visio** in Project Web App erstellen Sie eine EPT, die vom Workflow verwendet, und klicken Sie dann erstellen Sie Projekte, die die neue EPT verwenden, wie Sie für das **Verzweigungsworkflow** -Beispiel. In diesem Fall werden, jedoch Projekte, die kleiner als 5.000 $ Kosten sind abgelehnt. 
    
In durcharbeiten in diesem Artikel, erstellt und getestet einen einfachen verzweigungsworkflow mithilfe von SharePoint Designer 2013 zum direkten Festlegen der Phasen, Bedingungen und Aktionen, die vom Workflow verwendet. Sie erstellt ein Diagramm für eine noch einfacher verzweigungsworkflow auch mithilfe von Visio 2013. Sie importiert das Visio-Workflowdiagramm in SharePoint Designer 2013, in dem Sie die Eigenschaften der einzelnen Phasen, Bedingung und Aktion aus die Verbindung mit Project Web App festlegen.
  
Visio 2013 und SharePoint Designer bieten zusammen komfortable Möglichkeiten für Entwickler, Projektmanager, Workflowentwickler und Tester erstellen, freigeben und Anpassen von Workflow-Entwürfe für die verschiedenen Installationen von Project Server 2013 und Project Online. Für Workflows, die programmgesteuerten Zugriff auf Project Server erforderlich, die SharePoint Designer nicht bereitstellt, können Sie mit dem clientseitigen Objektmodell (CSOM) Visual Studio 2012.
  
## <a name="see-also"></a>Siehe auch

- [Project Server 2013-Architektur](project-server-2013-architecture.md)
- [Start: Einrichten und Konfigurieren von SharePoint 2013-Workflow-Manager](https://msdn.microsoft.com/library/jj163276%28office.15%29.aspx)
- [Grundlegendes zu packen und POST von Workflows in SharePoint 2013](https://msdn.microsoft.com/library/jj819316%28office.15%29.aspx)
- [Workflows in SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx)
- [Workflowentwicklung in SharePoint Designer 2013 und Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
- [Problembehandlung bei SharePoint Server 2013-workflowvalidierungsfehlern in Visio 2013](https://msdn.microsoft.com/library/jj163971%28v=office.15%29.aspx)
- [Workflow- und Projektbedarfsmanagement](https://msdn.microsoft.com/library/cf7433a3-a531-4467-ac0c-df0c5d6881ae%28Office.15%29.aspx)

