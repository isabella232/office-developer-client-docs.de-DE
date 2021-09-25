---
title: Erstellen eines Project Server-Workflows für das Bedarfsmanagement
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: b0e4a3b3-d1df-454d-b74c-b980b0b456f6
description: In diesem Artikel wird beschrieben, wie Sie mithilfe von SharePoint Designer 2013 einen einfachen Workflow erstellen.
ms.openlocfilehash: a4aa2dc748976b3f6f5710e3ab8e90c057e52702
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616222"
---
# <a name="create-a-project-server-workflow-for-demand-management"></a>Erstellen eines Project Server-Workflows für das Bedarfsmanagement

In diesem Artikel wird beschrieben, wie Sie mithilfe von SharePoint Designer 2013 einen einfachen Workflow erstellen. Sie können den Workflow zur Visualisierung und Bearbeitung in Visio 2013 exportieren oder Visio 2013 verwenden, um Project Server 2013-Workflows zu entwerfen und das Design in SharePoint Designer 2013 zur Veröffentlichung in Project Web App zu importieren. Weitere Informationen zur SharePoint Workflowplattform und zum Erstellen von Workflows mit Visio 2013 und SharePoint Designer 2013 finden Sie in den Artikeln [zu Workflows in SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx) in der Entwicklerdokumentation SharePoint 2013. 
  
Informationen zum Vorbereiten Project Servers für Workflows finden Sie unter [Start: Einrichten und Konfigurieren SharePoint 2013 Workflow-Manager.](https://msdn.microsoft.com/library/jj163276%28office.15%29.aspx)

<a name="pj15_CreateWorkflowSPD_General"> </a>

## <a name="creating-a-general-workflow"></a>Erstellen eines allgemeinen Workflows

Führen Sie die folgenden Schritte aus, um einen Project Server 2013-Workflow mithilfe von SharePoint Designer 2013 zu erstellen. Der Workflow ist auf das Bedarfsmanagement von Projektvorschlägen ausgelegt.
  
Ausführliche Schritte finden Sie im Abschnitt ["Erstellen eines Verzweigungsworkflows".](#pj15_CreateWorkflowSPD_Detailed) 
  
### <a name="to-create-a-project-server-workflow-general-procedure"></a>So erstellen Sie einen Project Server-Workflow (allgemeines Verfahren)

1. Ermitteln Sie die Anforderungen, und entwerfen Sie dann den Workflow. Unterteilen Sie ihn in Phasen und Stufen, und ermitteln Sie die benutzerdefinierten Felder, die vom Workflow verwendet werden.
    
2. Erstellen Sie in Project Web App die Entitäten, die für den Workflow erforderlich sind:
    
    1. Prüfen Sie die vorhandenen Workflowphasen; erstellen Sie Phasen nach Bedarf.
        
    2. Erstellen Sie die benutzerdefinierten Enterprise-Felder, die der Workflow verwendet. Damit ein benutzerdefiniertes Feld in einer Workflowphase verfügbar ist, muss es von einem Workflow gesteuert sein.
        
    3. Bearbeiten oder erstellen Sie die Projektdetailseiten (Project Detail Pages, PDPs), die von Ihren Workflowphasen zum Sammeln von Informationen für das Projekt verwendet werden. In diesem Fall werden von den Phasen Standard-Projektdetailseiten verwendet, die so bearbeitet werden, dass sie ein neues benutzerdefiniertes Feld enthalten.
        
    4. Erstellen Sie die erforderlichen Workflowphasen, und verknüpfen Sie dann jede Workflowphase mit der korrekten Phase.
    
3. Erstellen Sie in SharePoint Designer 2013 den Workflow mithilfe deklarativer Anweisungen im **textbasierten Designer:**
    
    > [!NOTE]
    > Sie können auch in SharePoint Designer 2013 zum **Visual Designer** wechseln oder einen vorhandenen Workflow aus Visio 2013 importieren. Befolgen Sie diese Schritte, um den **textbasierten Designer** zu verwenden: 
    > 
    > 1. Öffnen Sie die Project Web App-Website, und erstellen Sie dann einen Websiteworkflow, der SharePoint **2013 Workflow - Project** Server-Workflowplattform verwendet. 
    > 2. Fügen Sie die Phasen hinzu, die vom Workflow verwendet werden.
    > 3. Fügen Sie die Schritte, Bedingungen, Aktionen und Schleifen des Workflows hinzu, die in jeder Phase erforderlich sind.
    > 4. Prüfen Sie auf Workflowfehler, und beheben Sie diese.
    > 5. (Optional) Wechseln Sie die Ansicht zum **Visual Designer,** oder exportieren Sie den Workflow in eine Visio 2013-Datei. Sie können die Visio-Ansicht ändern und Änderungen im aktuellen Workflow speichern. Sie können die Visio Datei bearbeiten und in SharePoint Designer 2013 importieren, um weitere Workflows zu erstellen.
    > 6. Veröffentlichen Sie den Workflow. Nach der Veröffentlichung wird der Workflow in der Liste der Workflows für die Project Web App-Website angezeigt.
    
4. Verwenden Sie in Project Web App den Workflow für das Bedarfsmanagement von Projektvorschlägen:
    
    1. Erstellen Sie eine Enterprise-Projektvorlage (Enterprise Project Template, EPT), die den Workflow verwendet.
        
    2. Erstellen Sie auf der Project Center-Seite ein Projekt, das die EPT für den Workflow verwendet, und wechseln Sie dann durch die Workflowphasen.
        
    3. Testen Sie den Workflow sorgfältig.
        
    4. Stellen Sie den Workflow auf einem Produktionsserver bereit.

<a name="pj15_CreateWorkflowSPD_Detailed"> </a>

## <a name="creating-a-branching-workflow"></a>Erstellen eines Verzweigungsworkflows

Bevor Sie SharePoint Designer 2013 zum Erstellen eines Project Serverworkflows verwenden können, muss der Workflow-Manager Client 1.0-Dienst für die Verwendung der Project Server 2013-Workflowaktivitäten konfiguriert werden. Informationen zum Konfigurieren von Workflow-Manager Client 1.0 finden Sie in den Artikeln zu [Workflows in SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx) in der SharePoint Server 2013-Entwicklerdokumentation. 
  
Das folgende detaillierte Verfahren enthält die gleichen Schritte wie im Abschnitt ["Erstellen eines allgemeinen Workflows".](#pj15_CreateWorkflowSPD_General) 
  
### <a name="to-create-a-project-server-branching-workflow-detailed-procedure"></a>So erstellen Sie einen Project Server-Verzweigungsworkflow (ausführliches Verfahren)

#### <a name="1-plan-and-design-the-workflow"></a>1. Planen und Entwerfen des Workflows.

Ein Project Serverworkflow kann in mehrere Phasen und Phasen in einem Bedarfsmanagementprozess integriert werden. Da Workflows komplex sein können, müssen Sie die Geschäftsanforderungen verstehen und einen Workflow sorgfältig planen. Entwerfen Sie für ein einfaches Beispiel einen Verzweigungsworkflow, der die geschätzten Kosten eines Projektvorschlags verwendet, um zu bestimmen, ob der Vorschlag angenommen wird. Wenn die geschätzten Kosten größer als 25.000 USD sind, weisen Sie den Vorschlag zurück. andernfalls akzeptieren Sie den Vorschlag, und erstellen Sie das Projekt.
    
Da Sie Visio 2013 und SharePoint Designer 2013 zum Entwerfen und Erstellen von Workflows für Project Server 2013 verwenden können, können Sie einfacher mit Workflows experimentieren, als mit Project Server 2010 möglich ist. Der Beispielworkflowentwurf in diesem Artikel ist identisch mit dem Artikel ["Erstellen eines Verzweigungsworkflows"](https://msdn.microsoft.com/library/a02cafdc-d881-4271-b446-d8b2cd456a52%28Office.15%29.aspx) im Project 2010 SDK. Sie können einen Testworkflow auf einem Remotecomputer mithilfe einer Testinstanz von Project Web App entwerfen und erstellen– Sie müssen Workflows nicht direkt auf einem Computer mit Project Server 2013 erstellen. 
    
#### <a name="2-create-the-entities-that-your-workflow-requires"></a>2. Erstellen Sie die Entitäten, die Ihr Workflow erfordert.

Überprüfen Sie in Project Web App die verfügbaren Workflowphasen und -stufen sowie die verfügbaren benutzerdefinierten Enterprise-Felder. Erstellen Sie bei Bedarf, wie in den folgenden Schritten gezeigt, die Entitäten, die für Ihren Workflow erforderlich sind:
    
1. **Workflowphasen** Die Standardinstallation von Project Web App umfasst die Phasen "Erstellen", "Auswählen", "Planen", "Verwalten" und "Fertig stellen". Für das Beispiel mit dem Verzweigungsworkflow müssen Sie keine anderen Phasen erstellen. 
        
2. **Enterprise benutzerdefinierter Felder** Der Verzweigungsworkflow erfordert ein benutzerdefiniertes Projektkostenfeld, das workflowgesteuert ist. Der Wert eines workflowgesteuerten benutzerdefinierten Felds wird auf einer Projektdetailseite festgelegt, die der Workflow verwendet. Wählen Sie beispielsweise oben rechts auf einer Project Web App-Seite das **Symbol** Einstellungen aus, wählen Sie **PWA Einstellungen** und dann **Enterprise benutzerdefinierte Felder und Nachschlagetabellen** aus.
        
   Erstellen Sie für die Entität Projekt  ein benutzerdefiniertes Feld mit dem Namen **Vorschlagskosten**, und wählen Sie den Typ **Kosten** aus. Geben Sie als Beschreibung Geschätzte Kosten eines Projektvorschlags ein. Wählen Sie im Abschnitt **Verhalten****Verhalten vom Workflow gesteuert** aus.
        
3. **Project Detailseiten** Bearbeiten oder erstellen Sie die PDPs, die von den Workflowphasen verwendet werden. Führen Sie beispielsweise die folgenden Schritte aus: 
        
    1. Wählen Sie auf der Seite mit den Servereinstellungen **Projektdetailseiten** und dann die Projektdetailseite **ProjectInformation** aus. 
            
    2. Wählen Sie im Menüband auf der Registerkarte **SEITE** in der Gruppe **Bearbeiten****Seite bearbeiten** aus.
            
    3. Klicken Sie oben rechts im Webpart **"Grundlegende Informationen"** auf den Pfeil nach unten, und klicken Sie dann auf **"Webpart bearbeiten".** Oder wählen Sie auf der Registerkarte **"WEBPART"** des Menübands in der Gruppe **"Eigenschaften"** **die Webparteigenschaften** aus, um das Editorpart anzuzeigen. 
            
    4. Wählen Sie im Abschnitt **Angezeigte Projektfelder** des Bearbeitungs-Webparts (siehe Abbildung 1) **Ändern** aus.
            
    5. Fügen Sie das benutzerdefinierte Feld **"Vorschlagskosten"** hinzu, verschieben Sie es über das **Feld "Besitzer"** in der Liste **"Ausgewählte Project Felder",** und wählen Sie dann **"OK"** aus (siehe Abbildung 1).
      
    6. Wählen Sie im Bearbeitungs-Webpart **OK** und dann im Menüband auf der Registerkarte **SEITE** in der Gruppe **Bearbeiten****Bearbeitung beenden** aus. In Abbildung 2 ist das benutzerdefinierte Feld **Proposal Cost** dargestellt, das der Projektdetailseite "Projektinformationen" hinzugefügt wurde. 

    **Abbildung 1. Bearbeiten des Project Fields-Webparts in einem PDP**

    ![Bearbeiten des Project Fields-Webparts in einem PDP](media/pj15_CreateWorkflowSPD_EditPDP.gif "Bearbeiten des Project Fields-Webparts in einem PDP")

    **Abbildung 2. Die bearbeitete Projektdetailseite enthält das benutzerdefinierte Feld "Vorschlagskosten"**

    ![Die bearbeitete PDP beinhaltet das Feld "Vorschlagskosten"](media/pj15_CreateWorkflowSPD_EditedPDP.gif "Die bearbeitete PDP beinhaltet das Feld &quot;Vorschlagskosten&quot;")
  
4. **Workflowphasen** Erstellen Sie die Phasen, die für jede Phase des Workflows erforderlich sind. Wählen Sie auf der Seite mit den Servereinstellungen **Workflowstufen** und dann **NEUE WORKFLOWSTUFE** aus. In Abbildung 3 ist ein Teil der Seite "Workflowstufe hinzufügen" dargestellt.
    
    **Abbildung 3. Hinzufügen einer Workflowstufe in Project Web App**

    ![Hinzufügen einer Workflowphase in Project Web App](media/pj15_CreateWorkflowSPD_AddWorkflowStage.gif "Hinzufügen einer Workflowphase in Project Web App")
  
    Im Verzweigungsworkflow-Beispiel werden vier Stufen verwendet, die in Tabelle 1 dargestellt sind. Auf der Seite "Workflowstufe hinzufügen" im Abschnitt **Weitere Einstellungen für die ''sichtbare Projektdetailseite''** (in Abbildung 3 nicht dargestellt) sind Werte optional; sie bieten auf der Seite "Workflowstatus" mehr Informationen. Da z. B. die PDP für ursprüngliche Vorschlagsdetails Benutzereingaben erfordert, können Sie das Kontrollkästchen **"Die Project Detailseite erfordert Aufmerksamkeit"** aktivieren und dann eine bestimmte Beschreibung hinzufügen, z. B. "Projektnamen und Kosten für diesen PDP festlegen".
    
    In Abbildung 4 sind die vier Stufen abgebildet, die auf der Seite "Workflowstufen" durchlaufen werden.
    
    **Tabelle 2. Stufen des Verzweigungsworkflows**

    |Name|Beschreibung|Beschreibung für Einreichung|Phase|Sichtbare PDPs|Benutzerdefinierte Felder|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |Ursprüngliche Vorschlagsdetails  <br/> |Legen Sie den Projektnamen und die Kosten fest.  <br/> |Reichen Sie das Projekt als Vorschlag ein.  <br/> |Erstellen  <br/> |Projektinformationen  <br/> Projektdetails  <br/> |Vorschlagskosten (erforderlich)  <br/> |
    |Projektdetails  <br/> |Geben Sie nähere Informationen zum vorgeschlagenen Projekt an.  <br/> |Senden Sie die Details ab, um mit dem Projekt fortzufahren.  <br/> |Erstellen  <br/> |Projektinformationen  <br/> Projektdetails  <br/> |Vorschlagskosten (schreibgeschützt)  <br/> |
    |Automatische Ablehnung  <br/> |Der Vorschlag wird auf Grundlage der angegebenen Informationen abgelehnt.  <br/> | <br/> |Erstellen  <br/> |Projektinformationen  <br/> |Vorschlagskosten (schreibgeschützt)  <br/> |
    |Ausführung  <br/> |Der Vorschlag wurde angenommen und ist bereit für das Projektmanagement.  <br/> | <br/> |Verwalten  <br/> |Projektinformationen  <br/> Projektdetails  <br/> |Vorschlagskosten (schreibgeschützt)  <br/> |
   
    **Abbildung 4. Liste der Workflowstufen in Project Web App**

    ![Liste der Workflowphasen in Project Web App](media/pj15_CreateWorkflowSPD_WorkflowStages.gif "Liste der Workflowphasen in Project Web App")
  
#### <a name="3-construct-the-workflow-in-the-text-based-designer"></a>3. Erstellen Sie den Workflow im Text-Based Designer.

Erstellen Sie in SharePoint Designer 2013 den Workflow mithilfe deklarativer Anweisungen im Text-Based Designer. Sie können mit der Eingabe an der orangefarbenen Einfügezeile beginnen, um kontextabhängige AutoVervollständigungsanweisungen für die Workflowlogik und die Schritte abzurufen, oder Sie können die Logik und die Schritte mithilfe von Steuerelementen in der Gruppe **"Einfügen"** auf der Registerkarte **"WORKFLOW"** des Menübands einfügen. 
    
1. Wählen Sie in der Backstage-Ansicht von SharePoint Designer 2013 die Option **"Website öffnen"** aus. Öffnen Sie beispielsweise  `https://ServerName/pwa` . Wählen Sie im Bereich **Navigation****Workflows** aus. Wählen Sie dann im Menüband auf der Registerkarte **WORKFLOWS** in der Gruppe **Neu****Websiteworkflow** aus. Benennen Sie den Workflow in diesem Beispiel Verzweigungsworkflow. Stellen Sie sicher, dass **SharePoint 2013 Workflow – Project Server** in der Dropdownliste **"Plattformtyp"** ausgewählt ist (siehe Abbildung 5). 
    
    **Abbildung 5. Erstellen eines Project Server-Websiteworkflows**

    ![Erstellen eines Project Server-Websiteworkflows](media/pj15_CreateWorkflowSPD_CreateSiteWorkflow.gif "Erstellen eines Project Server-Websiteworkflows")
  
2. Wählen Sie die Registerkarte **Verzweigungsworkflow** aus. Wählen Sie dann im Menüband auf der Registerkarte **WORKFLOW** in der Gruppe **Verwalten** in der Dropdownliste **Ansichten****Textbasierter Designer** aus. Klicken Sie in die Ansicht, um die Ansicht mit der blinkenden orangefarbenen Einfügelinie anzuzeigen (siehe Abbildung 6).
    
    **Abbildung 6. Verwenden der Ansicht "Textbasierter Designer" für den Workflow**

    ![Verwenden der textbasierten Entwurfsansicht](media/pj15_CreateWorkflowSPD_TextBasedDesigner.gif "Verwenden der textbasierten Entwurfsansicht")
  
3. Fügen Sie in der Ansicht **Textbasierter Designer** die Stufen hinzu, die im Workflow verwendet werden. Wählen Sie im Menüband auf der Registerkarte **WORKFLOW** in der Gruppe **Einfügen** in der Dropdownliste **Stufe** unter **Erstellen****Ursprüngliche Vorschlagsdetails** aus.
    
    Platzieren Sie die orangefarbene Einfügelinie entsprechend unterhalb des Felds **Stufe: Ursprüngliche Vorschlagsdetails**, und fügen Sie die anderen Stufen hinzu, die vom Workflow verwendet werden: **Projektdetails**, **Automatische Ablehnung** und **Ausführung** (siehe Abbildung 7). 
    
    **Abbildung 7. Hinzufügen einer Stufe zu einem Workflow in SharePoint Designer**

    ![Hinzufügen einer Phase zu einem Workflow in SPD](media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Hinzufügen einer Phase zu einem Workflow in SPD")
  
4. Fügen Sie in jeder Phase die Workflowschritte und die Workflowlogik hinzu: 
    
    1. Platzieren Sie in der Phase **Ursprüngliche Vorschlagsdetails** die orangefarbene Einfügelinie über dem Phasentext. Wählen Sie im Menüband in der Gruppe **Einfügen****Aktion** aus, blättern Sie nach unten zu **Project Web App-Aktionen**, und wählen Sie dann **Auf Projektereignis warten** aus. Wählen Sie **Dieses Projektereignis** und dann in der Dropdownliste **Ereignis: Wenn ein Projekt eingereicht wird** aus. 
    
    2. Fügen Sie im Abschnitt **Übergang in Phase** der Phase **Ursprüngliche Vorschlagsdetails****Wenn ein beliebiger Wert gleich dem Wert ist** ein. Sie können mit der Eingabe der Anweisung beginnen oder auf dem Menüband in der Gruppe **Einfügen** das Steuerelement **Bedingung** verwenden. 
    
    3. Wählen Sie das erste **value**-Steuerelement und dann **fx** aus, um das Dialogfeld **Workflow-Nachschlagevorgang definieren** anzuzeigen (siehe Abbildung 8). Wählen Sie in der Dropdownliste **Datenquelle****Projektdaten** aus. Wählen Sie in der Dropdownliste **Quellenfeld****Vorschlagskosten** aus.
    
       **Abbildung 8. Definieren eines Nachschlagewerts im Workflow**

       ![Definieren eines Nachschlagewertes im Workflow](media/pj15_CreateWorkflowSPD_DefineWorkflowLookup.gif "Definieren eines Nachschlagewertes im Workflow")
  
    4. Schließen Sie die `If` Anweisung ab, damit Folgendes angezeigt wird: **Wenn Project Data:Proposal Cost größer als 25000 ist**
    
       > [!NOTE]
       > Alternativ könnten Sie eine Workflowvariable erstellen, die Variable auf den benutzerdefinierten Feldwert festlegen und dann die Variable mit einem Wert vergleichen. Erstellen Sie z. B. aus der Dropdownliste **Lokale Variablen** auf dem Menüband eine Variable mit der Bezeichnung **TotalCost** (keine Leerzeichen) des Typs **Number**. Wählen Sie im Dialogfeld **Workflow-Nachschlagevorgang definieren** für die Datenquelle **Workflowvariablen und -parameter** aus, und wählen Sie dann als das Feld **Variable: Gesamtkosten** aus. Die **If**-Anweisung würde dann lauten: **Wenn Variable: Gesamtkosten höher sind als 25000**
  
    5. Platzieren Sie die orangefarbene Einfügelinie innerhalb der `If` Verzweigung, und fügen Sie dann mithilfe des Aktionssteuerelements in der Gruppe **"Einfügen"** im Menüband eine **Phase** ein.  Wählen Sie das Dropdownfeld **eine Phase** und dann die Phase **Automatische Ablehnung** aus. 
    
       Fügen Sie entsprechend in der `Else` Verzweigung die Anweisung **Gehe zu Project Details** ein. In Abbildung 9 ist die abgeschlossene Phase **Ursprüngliche Vorschlagsdetails** abgebildet. 
    
       **Abbildung 9. Fertige Logik für Phase "Ursprüngliche Vorschlagsdetails"**

       ![Abgeschlossene Logik für ursprüngliche Vorschlagsdetails](media/pj15_CreateWorkflowSPD_InitialStageLogic.gif "Abgeschlossene Logik für ursprüngliche Vorschlagsdetails")
  
    6. Lassen Sie in der Phase **Automatische Ablehnung** den ersten Abschnitt leer, es sei denn, Sie möchten den Workflow anhalten und einige Daten auf einer Projektdetailseite anzeigen. Der Abschnitt **Übergang in Phase** muss einen Übergang enthalten. Da auf eine Ablehnung keine weitere Phase folgt, geben Sie als Anweisung Zum Ende des Workflows wechseln ein. 
    
    7. Fügen Sie im Abschnitt **Übergang in Phase** in der Phase Projektdetails **Zur Ausführung wechseln** hinzu. Es ist nicht erforderlich zu warten, bis ein Ereignis übermittelt wurde, es sei denn, es müssen zusätzliche Daten hinzugefügt werden, oder Sie möchten den Workflow anhalten. 
    
    8. Lassen Sie in der Phase **Ausführung** den Abschnitt mit der Phasenaktion leer, es sei denn, Sie möchten den Workflow anhalten. Fügen Sie im Abschnitt **Übergang in Phase****Zum Ende des Workflows wechseln** hinzu.
    
5. Wählen Sie auf dem Menüband in der Gruppe **Speichern****Auf Fehler prüfen** aus, um auf Workflowfehler zu prüfen (siehe Abbildung 10). Beheben Sie alle Fehler, und wählen Sie dann **Speichern** aus.
    
    **Abbildung 10. Prüfen des Workflows auf Fehler im SharePoint Designer**

    ![Überprüfen auf Fehler im Workflow](media/pj15_CreateWorkflowSPD_SPDCheckForErrors.gif "Überprüfen auf Fehler im Workflow")
  
6. (Optional) Wählen Sie auf dem Menüband in der Gruppe **Verwalten** im Dropdownmenü **Ansichten****Visual Designer** aus. In Abbildung 11 ist die Ansicht auf 50 % verkleinert.
    
    Sie können Elemente im Workflow mit dem Visual Designer bearbeiten. Wählen Sie z. B. die Bedingung **Wenn ein beliebiger Wert gleich dem Wert ist** aus, wählen Sie unten rechts neben der Bedingung das Extras-Symbol aus, und wählen Sie dann **Wert** aus, um die Vergleichsbedingungen im Dialogfeld **Eigenschaften** anzuzeigen. 
    
    **Abbildung 11. Verwenden des Visual Designer für einen Workflow**

    ![Verwenden der Visio-Entwurfsansicht des Workflows](media/pj15_CreateWorkflowSPD_SwitchView.gif "Verwenden der Visio-Entwurfsansicht des Workflows")
  
    Wenn sich der Workflow in der Ansicht Visual Designer befindet, können Sie zum Speichern des Workflows in einer Visio 2013-Datei (VSDX) als Sicherung oder zur späteren Verwendung export **to Visio** auswählen.
    
7. Veröffentlichen Sie den Workflow. Wenn Sie SharePoint Designer 2013 verwenden, um den Workflow auf der aktiven Project Web App-Website zu veröffentlichen, wird der Workflow auf der SharePoint Website oder in Azure registriert und in Project Web App für neue EPTs verfügbar.

#### <a name="4-create-an-ept-for-the-workflow-and-then-test-the-workflow"></a>4. Erstellen Sie eine EPT für den Workflow, und testen Sie dann den Workflow.

Erstellen Sie in Project Web App eine EPT für den Workflow, und testen Sie dann den Workflow, indem Sie einen Projektvorschlag erstellen:
    
1. Wählen Sie auf der Seite PWA Einstellungen **Enterprise Project Typen aus,** und erstellen Sie dann eine EPT mit dem Namen "Test Branching Workflow". Deaktivieren Sie das Kontrollkästchen **Neue Projekte als SharePoint-Vorgangslistenprojekte erstellen**, sodass Project Server die vollständige Kontrolle über Projekte behält, die von der EPT erstellt werden. Wählen Sie in der Dropdownliste **Website-Workflowzuordnung****Verzweigungsworkflow** aus, und wählen Sie dann in der Dropdownliste **Neue Projektseite** die Projektdetailseite **Projektinformationen** als die erste Seite aus, die im Workflow angezeigt wird. 
    
    **Abbildung 12. Hinzufügen einer EPT für den Workflow**

    ![Hinzufügen einer EPT für den Workflow](media/pj15_CreateWorkflowSPD_EPTs.gif "Hinzufügen einer EPT für den Workflow")
  
    > [!NOTE]
    > Ein **Ja**-Wert in der Spalte **SharePoint-Vorgangslistenprojekt** in der Tabelle der Enterprise-Projekttypen bezieht sich auf eine EPT, mit der eine SharePoint-Aufgabenliste erstellt wird, wobei die Aufgabenliste in Project Web App sichtbar ist, SharePoint aber die Kontrolle über das Projekt behält. Weitere Informationen zum Verwalten von Projekten als SharePoint-Aufgabenlisten finden Sie unter [Project Server 2013 architecture](project-server-2013-architecture.md). 
  
2. Öffnen Sie die Seite "Projekte" in Project Web App, und erstellen Sie dann ein Projekt mithilfe der neuen EPT (siehe Abbildung 13). Da **Verzweigungsworkflow – Test** mit **Verzweigungsworkflow** verknüpft ist, beginnt die Projekterstellung unter der Kontrolle des Workflows.
    
    **Abbildung 13. Erstellen eines Projekts mit der EPT "Verzweigungsworkflow – Test"**

    ![Erstellen eines Projekts mit der EPT](media/pj15_CreateWorkflowSPD_NewProject.gif "Erstellen eines Projekts mit der EPT")
  
3. Wenn der Workflow die Projektdetailseite **Projektinformationen** anzeigt, fügen Sie den Projektfeldern Daten hinzu. Geben Sie beispielsweise einen **Vorschlagskostenwert** von 30000 ein. In der Englischversion (USA) von Project Server wird die Eingabe im Feld in "$30,000" geändert (siehe Abbildung 14).
    
    **Abbildung 14. Verwenden der bearbeiteten Projektdetailseite "Projektinformationen"**

    ![Verwenden der bearbeiteten PDP mit Projektinformationen](media/pj15_CreateWorkflowSPD_NewProjectStage1.gif "Verwenden der bearbeiteten PDP mit Projektinformationen")
  
4. Wählen Sie im Menüband auf der Registerkarte **PROJEKT** in der Gruppe **Projekt****Speichern** aus. Project Server fügt dem Projekt die Daten auf der Projektdetailseite hinzu und zeigt dann die Seite "Workflowstatus" an (siehe Abbildung 15). Um die vollständige Beschreibung der Phase "Ursprüngliche Vorschlagsdetails" im Workflowstatusdiagramm anzuzeigen, bewegen Sie den Mauszeiger im Workflowvisualisierungsdiagramm über die Phase.
    
    Im Raster **Alle Workflowphasen** wird mithilfe eines grünen Pfeils angegeben, dass für die Phase "Ursprüngliche Vorschlagsdetails" eine Benutzereingabe erwartet wird. Der Grund dafür ist, dass der Workflow in der Phase "Ursprüngliche Vorschlagsdetails" auf ein Einreichereignis wartet. Wenn der Workflow nicht auf ein Einreichereignis warten würde, könnten Sie in der Gruppe **Seite****Weiter** auswählen, um zur nächsten Projektdetailseite zu wechseln. 
    
    **Abbildung 15. Verwenden der Seite "Workflowstatus" in der Phase "Ursprüngliche Vorschlagsdetails"**

    ![Workflowstatusseite nach der ersten Phase](media/pj15_CreateWorkflowSPD_NewProjectStage1Status.gif "Workflowstatusseite nach der ersten Phase")
  
    Im Workflowvisualisierungsdiagramm wird die aktuelle Phase in grün angezeigt. In der Phase **Erstellen** stellt die Phase "Ursprüngliche Vorschlagsdetails" die aktuelle Phase dar. 
    
5. Wählen Sie auf dem Menüband in der Gruppe **Workflow****Einreichen** aus.
    
    > [!TIP]
    > Aktualisieren Sie die Seite, wenn das Steuerelement **Einreichen** deaktiviert ist. 
  
    Wenn der Wert **Vorschlagskosten** höher ist als 25.000 USD, wechselt der Workflow zur Phase "Automatische Ablehnung". In Abbildung 16 ist der Status "Automatische Ablehnung" dargestellt, wenn Sie erneut **Einreichen** auswählen. Wenn die **Vorschlagskosten** 25.000 USD oder weniger betragen, wechselt der Workflow zur Phase "Projektdetails" (siehe Abbildung 17). 
    
    **Abbildung 16. Der Workflow ist in der Phase "Automatische Ablehnung" abgeschlossen**

    ![Der Workflow ist in automatischer Ablehnung abgeschlossen](media/pj15_CreateWorkflowSPD_AutomatedRejectionCompleted.gif "Der Workflow ist in automatischer Ablehnung abgeschlossen")
  
    Abbildung 17 zeigt einen weiteren Test mit einem Projektvorschlag namens **"Test 2 – Verzweigung",** wobei die Phase Project Details in der Erstellungsphase aktuell ist. Die Verwaltungsphase wird in hellblauer Farbe angezeigt, was darauf hinweist, dass die Phase noch nicht aktiv ist.
    
    **Abbildung 17. Der Workflow wechselt zur Phase "Projektdetails", wenn die Kosten niedriger als 25.000 USD sind**

    ![Workflowstatus in der Projektdetailphase](media/pj15_CreateWorkflowSPD_ProjectDetailsStage.gif "Workflowstatus in der Projektdetailphase")
  
6. Wenn Sie mit der Phase "Projektdetails" fortfahren, müssen auf der Standardseite keine zusätzlichen Daten hinzugefügt werden. Wählen Sie erneut **Einreichen** aus, um mit der Ausführungsphase fortzufahren (siehe Abbildung 18). 
    
    **Abbildung 18. Der Workflow ist bereit zur Verwaltung in der Ausführungsphase**

    ![Workflowstatus in der Ausführungsphase](media/pj15_CreateWorkflowSPD_ExecutionStage.gif "Workflowstatus in der Ausführungsphase")
  
Der Workflow wartet in der Phase "Projektdetails" nicht auf ein Einreichereignis. Wenn die Projektdetailseite "Projektdetails" zusätzliche Pflichtfelder enthält, wartet Project Server, bis Sie den Feldern Daten hinzufügen, bevor zur Ausführungsphase gewechselt wird. Wie im Verzweigungsworkflow definiert, wartet auch die Ausführungsphase nicht auf ein Einreichereignis. Als Projektmanager können Sie das Projekt in der Ausführungsphase bearbeiten oder im Menüband auf der Registerkarte **PROJEKT****Schließen** auswählen. Wenn Sie **Schließen** auswählen, können Sie das Projekt einchecken und es später bearbeiten oder das Projekt ausgecheckt lassen.

Das Projekt **Verzweigungsworkflow** ist ein einfaches Beispiel mit nur einem Vergleichstest. Der Workflow umfasst in der Phase "Erstellen" drei Stufen und in der Phase "Verwalten" des Bedarfsmanagements eine Stufe. Um einen Workflow sorgfältig zu testen, sollten Sie alle Verzweigungen des Workflows testen und extreme und typische Werte verwenden, um zu sehen, ob das erwartete Verhalten auftritt. 

<a name="pj15_CreateWorkflowSPD_ImportingVromVisio"> </a>

## <a name="importing-a-workflow-from-visio"></a>Importieren eines Workflows aus Visio

Um den Workflow zu ändern, können Sie workflowgesteuerte benutzerdefinierte Felder erstellen oder ändern und Workflowphasen und -stufen erstellen oder ändern. Sie können SharePoint Designer 2013 verwenden, um Bedingungen, Aktionen, Schleifen und Phasen hinzuzufügen und dann den Workflow zu speichern und erneut zu veröffentlichen. Um eine Sicherung eines Workflows wiederzuverwenden oder beizubehalten, können Sie sie in eine Visio 2013-Datei exportieren. 
  
Sie können den Workflow auch in Visio 2013 erstellen oder bearbeiten und die Datei zur Verwendung durch Project Web App in SharePoint Designer 2013 importieren. Um einen unveränderten Workflow zu verwenden, muss die Project Web App-Instanz Workflowphaseneigenschaften enthalten, die mit denen in der ursprünglichen Project Web App-Instanz identisch sind. Weitere Informationen zur Verwendung von Visio zum Erstellen von Workflows finden Sie [unter Workflowentwicklung in SharePoint Designer 2013 und Visio 2013.](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
> [!NOTE]
> Wenn Sie eine Visio 2013-Datei in eine andere Instanz von Project Web App importieren, haben die Phasen unterschiedliche Phasen-GUIDs, auch wenn die Phasennamen identisch sind. Nachdem Sie den Workflow importiert haben, müssen Sie die Phasen- und Aktionseigenschaften so konfigurieren, dass sie für die Project Web App-Instanz spezifische Werte verwenden. 
> 
> Wenn Sie in Visio 2013 einen Workflow erstellen, weisen die Phasen und Aktionen keine spezifischen Eigenschaften für eine Project Web App-Instanz auf, da Visio keine Verbindung mit Project Web App herstellt. Wenn Sie SharePoint Designer 2013 mit Project Web App verbinden, einen Workflow erstellen und dann die VSDX-Datei importieren, überschreiben Sie den aktiven Workflow. Anschließend müssen Sie die Phasen- und Aktionseigenschaften so konfigurieren, dass sie den Werten entsprechen, die SharePoint Designer 2013 aus Project Web App abruft. 
  
### <a name="to-import-a-workflow-from-visio-to-sharepoint-designer"></a>So importieren Sie einen Workflow aus Visio in SharePoint Designer

1. Erstellen Sie in Visio 2013 einen einfachen Workflow. Führen Sie beispielsweise die folgenden Schritte aus:
    
   1. Öffnen Sie Visio, und erstellen Sie dann einen Workflow. Wählen Sie den Bereich **KATEGORIEN** für einen neuen Workflow aus. Wählen Sie **Flussdiagramm** aus, wählen Sie im Bereich **Neu** die **Microsoft SharePoint 2013-Workflow**-Vorlage aus, und wählen Sie dann **Erstellen** aus. Der Workflow wird mit einem Phasen-Shape mit der Bezeichnung **Phase 1** geöffnet. Der Workflow umfasst eine Startkomponente und als Bestandteil des Phasen-Shapes ein Eingangs-Shape und ein Ausgangs-Shape.
    
      Wenn Sie den Mauszeiger über das Phasen-Shape bewegen und das Symbol **Eigenschaften**  auswählen, wird die Auswahl deaktiviert. Sie können die Phasen- und Aktionseigenschaften festlegen, nachdem Sie das Workflowdiagramm in SharePoint Designer 2013 importiert haben. 
    
      > [!NOTE]
      >  Sie sollten nur die folgenden Shape-Schablonen in der Liste der Flussdiagramm-Shapes verwenden: 
      > - **Aktionen – SharePoint 2013-Workflow**
      > - **Komponenten – SharePoint 2013-Workflow**
      > - **Bedingungen – SharePoint 2013-Workflow**
  
   2. Wählen Sie im Bereich **Shapes****Quick-Shapes** aus, und ziehen Sie das Bedingungs-Shape mit der Bezeichnung **Wenn ein beliebiger Wert gleich dem Wert ist** dann rechts neben das Phasen-Shape. 
    
   3. Wählen Sie auf dem Menüband auf der Registerkarte **HOME** das **Verbinder**-Tool aus, und verbinden Sie dann das Ausgangs-Shape in der Phase mit dem Bedingungs-Shape (siehe Abbildung 19). 
    
      **Abbildung 19. Verbinden eines Phasen-Shapes mit einem Bedingungs-Shape in einem Visio-Workflowdiagramm**

      ![Erstellen eines Workflowdiagramms in Visio](media/pj15_CreateWorkflowSPD_NewVisioWorkflow.gif "Erstellen eines Workflowdiagramms in Visio")
  
   4. Ziehen Sie zwei weitere Phasen-Shapes rechts neben das Bedingungs-Shape. Die Shapes heißen **Phase 2** und **Phase 3**.
    
   5. Verbinden Sie mithilfe des **Verbinder**-Tools die rechte Seite des Bedingungs-Shapes mit dem Eingangs-Shape von **Phase 2**. Wählen Sie das **Zeigertool aus,** doppelklicken Sie auf die Verbindung, um ein Textfeld für den Namen anzuzeigen, und nennen Sie dann die Verbindung "Ja".
    
   6. Verbinden Sie die Unterseite des Bedingungs-Shapes mit dem Eingangs-Shape von **Phase 3**. Rechtsklicken Sie mit dem **Zeigertool** auf die Verbindung, und wählen Sie dann **Nein** aus. Beide Methoden können verwendet werden, um die Verbinder mit **Ja** oder **Nein** zu benennen.
    
   7. Wählen Sie im Bereich **"Shapes"** die Option "Aktionen – **SharePoint 2013-Workflow"** aus, und ziehen Sie dann die **Aktion "Auf Projekt warten"** in die Mitte des Shapes für **Phase 1** (siehe Abbildung 20). 
    
      **Abbildung 20. Abschließen des Workflows in Visio**

      ![Abschließen des Workflows in Visio](media/pj15_CreateWorkflowSPD_CompletedVisioWorkflow.gif "Abschließen des Workflows in Visio")
  
   8. Wählen Sie im Menüband auf der Registerkarte **PROZESS** in der Gruppe **Diagrammüberprüfung****Diagramm prüfen** aus. Beheben Sie Fehler, und speichern Sie dann die Zeichnung. Nennen Sie die Datei z. B. Testworkflow aus Visio.vsdx.
    
      Informationen zum Beheben von Workflowfehlern finden Sie [unter Troubleshooting SharePoint Server 2013 workflow validation errors in Visio 2013.](https://msdn.microsoft.com/library/jj163971%28v=office.15%29.aspx)
    
2. Öffnen Sie SharePoint Designer 2013, und öffnen Sie dann dieselbe Project Web App-Website, die Sie für das **Verzweigungsworkflow-Beispiel** verwendet haben. 
    
3. Wählen Sie im Bereich **Navigation****Workflows** aus, und erstellen Sie dann einen Websiteworkflow (wählen Sie im Menüband auf der Registerkarte **WORKFLOWS****Websiteworkflow** aus). Nennen Sie den Workflow z. B. Einfacher Workflow aus Visio.
    
   Stellen Sie im Dialogfeld **Websiteworkflow erstellen** sicher, dass der Plattformtyp **SharePoint 2013 Workflow - Project Server** ist. Wählen Sie **"Erstellen"** aus, und SharePoint Designer den **Textbasierten Designerbereich** für den neuen Workflow öffnet. 
    
4. Wählen Sie im Menüband auf der Registerkarte **WORKFLOW** in der Gruppe **Verwalten****Workfloweinstellungen** aus.
    
5. Wählen Sie im Menüband auf der Registerkarte **"WORKFLOWEINSTELLUNGEN"** in der Gruppe **"Verwalten"** die Option **"Aus Visio importieren" aus,** und importieren Sie dann den **Testworkflow aus Visio.vsdx-Datei,** die Sie zuvor gespeichert haben. Ein Microsoft **SharePoint Designer-Dialogfeld** warnt, dass das diagramm, das Sie importieren, keine Workfloweigenschaften enthält, und fragt, ob der aktuelle Workflow überschrieben werden soll. Wählen Sie **"Ja"** aus; SharePoint Designer importiert das Workflowdiagramm, generiert Schablonen für die Shapes und zeigt den **Visual Designer-Bereich** an, der den importierten Workflow enthält. 
    
6. Legen Sie die Eigenschaften jedes Phasen-Shapes im Workflow fest. Das Shape der ersten Phase heißt beispielsweise **Phase 1 (Ungültig),** da es keine gültige Phase in der verbundenen Project Web App-Instanz darstellt. Wenn Sie die Phase auswählen oder mit dem Mauszeiger darauf zeigen, können Sie links unten neben dem Phasen-Shape das Symbol **Eigenschaften** auswählen, um das Dialogfeld **Phaseneigenschaften** anzuzeigen (siehe Abbildung 21). Wählen Sie die Phase **Ursprüngliche Vorschlagsdetails** in der Dropdownliste **Projektphase** aus, und wählen Sie dann **OK** aus. SharePoint Designer benennt die Phase um.
    
   **Abbildung 21. Festlegen der Phaseneigenschaft in SharePoint Designer**

   ![Festlegen von Eigenschaften in einem importierten Workflow](media/pj15_CreateWorkflowSPD_ImportFromVisio1.gif "Festlegen von Eigenschaften in einem importierten Workflow")
  
   Legen Sie bei der zweiten Phase die Eigenschaft **Projektphase** auf **Automatische Ablehnung** fest. Legen Sie die Eigenschaft **Projektphase** bei der dritten Phase auf **Ausführung** fest.
    
7. Legen Sie entsprechend bei der Aktion **Auf Projektereignis warten** die Eigenschaft **Ereignisname** auf **Ereignis: Wenn ein Projekt eingereicht wird** fest.
    
8. Legen Sie entsprechend die Eigenschaften der Bedingung **Wenn ein beliebiger Wert gleich dem Wert ist** fest. Legen Sie z. B. die erste **Wert**-Eigenschaft auf **Projektdaten:Vorschlagskosten** fest. Legen Sie die **Operator**-Eigenschaft auf **ist kleiner als** fest. Legen Sie die zweite **Value-Eigenschaft** auf 5000 fest.
    
9. Prüfen Sie den Workflow auf Fehler, und speichern Sie dann den Workflow. Falls Fehler vorhanden sind, können Sie zur Ansicht **Textbasierter Designer** wechseln (siehe Abbildung 22). 
    
   **Abbildung 22. Anzeigen des importierten Workflows im textbasierten Designer**

   ![Anzeigen des importierten Workflows](media/pj15_CreateWorkflowSPD_WorkflowFromVisio.gif "Anzeigen des importierten Workflows")
  
10. Veröffentlichen Sie den Workflow. Wenn Sie den Workflow speichern, aber nicht veröffentlichen, ist der Workflow nicht verfügbar, wenn Sie einen Enterprise-Projekttyp erstellen.
    
11. Um den importierten **einfachen Workflow aus Visio** in Project Web App zu testen, erstellen Sie eine EPT, die den Workflow verwendet, und erstellen Sie dann Projekte, die die neue EPT wie im Beispiel für den **Verzweigungsworkflow** verwenden. In diesem Fall werden allerdings Projekte, die weniger als 5.000 USD kosten, abgelehnt. 
    
Beim Durcharbeiten dieses Artikels haben Sie einen einfachen Verzweigungsworkflow mithilfe von SharePoint Designer 2013 erstellt und getestet, um die Phasen, Bedingungen und Aktionen, die der Workflow verwendet, direkt festzulegen. Außerdem haben Sie mithilfe von Visio 2013 ein Diagramm für einen noch einfacheren Verzweigungsworkflow erstellt. Sie haben das Visio Workflowdiagramm in SharePoint Designer 2013 importiert, in dem Sie die Eigenschaften der einzelnen Phasen, Bedingungen und Aktionen aus der Verbindung mit Project Web App festgelegt haben.
  
Visio 2013 und SharePoint Designer zusammen bieten Designern, Projektmanagern, Workflowentwicklern und Testern bequeme Möglichkeiten zum Erstellen, Freigeben und Anpassen von Workflowdesigns für verschiedene Installationen von Project Server 2013 und Project Online. Für Workflows, die programmgesteuerten Zugriff auf Project Server benötigen, den SharePoint Designer nicht bereitstellt, können Sie Visual Studio 2012 mit dem clientseitigen Objektmodell (CSOM) verwenden.
  
## <a name="see-also"></a>Siehe auch

- [Project Server 2013-Architektur](project-server-2013-architecture.md)
- [Start: Einrichten und Konfigurieren von SharePoint 2013-Workflow-Manager](https://msdn.microsoft.com/library/jj163276%28office.15%29.aspx)
- [Grundlegendes zum Packen und Bereitstellen von Workflows in SharePoint 2013](https://msdn.microsoft.com/library/jj819316%28office.15%29.aspx)
- [Workflows in SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx)
- [Entwickeln von Workflows in SharePoint Designer 2013 und Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
- [Problembehandlung bei SharePoint Server 2013-Workflowüberprüfungsfehlern in Visio 2013](https://msdn.microsoft.com/library/jj163971%28v=office.15%29.aspx)
- [Workflow- und Bedarfsmanagement](https://msdn.microsoft.com/library/cf7433a3-a531-4467-ac0c-df0c5d6881ae%28Office.15%29.aspx)

