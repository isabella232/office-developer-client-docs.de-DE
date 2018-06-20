---
title: Arbeiten Sie mit offlinelösungen mithilfe des InfoPath-Objektmodells
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Lösungen [Infopath 2007], offline, offline Lösungen [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen, InfoPath 2003-kompatible Formularvorlagen, offlinelösungen
localization_priority: Normal
ms.assetid: 634ccd8c-0b5f-4161-875c-0e546a517377
description: Das InfoPath 2003-kompatible Objektmodell bietet die MachineOnlineState-Eigenschaft des Application-Objekts ermöglicht Formularcode zu prüfen, ob es sich bei dem Computer des Benutzers mit dem Netzwerk verbunden ist. Formularcode kann je nach Status der Verbindung verschiedene Aktionen ausführen.
ms.openlocfilehash: 858b5d317cf5245dbfb447fa9e118a11ecbe7eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790743"
---
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a>Arbeiten Sie mit offlinelösungen mithilfe des InfoPath-Objektmodells

Das InfoPath 2003-kompatible Objektmodell bietet die [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) -Eigenschaft des [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) -Objekts ermöglicht Formularcode zu prüfen, ob es sich bei dem Computer des Benutzers mit dem Netzwerk verbunden ist. Formularcode kann je nach Status der Verbindung verschiedene Aktionen ausführen. 
  
## <a name="using-the-machineonlinestate-property"></a>Mithilfe der MachineOnlineState-Eigenschaft

Im folgenden Beispiel wird gezeigt, wie Sie dem Formularcode Logik hinzufügen können. Mit dieser wird anhand des Online- oder Offlinestatus des Benutzercomputers bestimmt, wie ein Formular gesendet werden soll.
  
Bei dem Beispiel wird davon ausgegangen, dass Sie ein Formular zum Senden eines Umsatzberichts erstellt haben, das ein Feld mit der Bezeichnung "period" (Zeitraum) zur Angabe des im Bericht behandelten Monats und Jahres enthält. Außerdem wird vorausgesetzt, dass Sie bereits eine Datenverbindung und die Logik zum Senden des Berichts, wenn der Benutzer online ist, definiert haben.
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Hinzufügen einer Datenverbindung, die das Formular als Anlage einer e-Mail-Nachricht sendet

1. Erstellen oder öffnen Sie eine InfoPath-Formularvorlage mit verwaltetem Code.
    
2. Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Datenverbindungen**.
    
3. Klicken Sie im Dialogfeld **Datenverbindungen** auf **Hinzufügen**.
    
4. Klicken Sie im **Datenverbindungs-Assistenten**klicken Sie auf **Daten senden**, und klicken Sie dann auf **Weiter**.
    
5. Klicken Sie auf der nächsten Seite des Assistenten klicken Sie auf **als e-Mail-Nachricht**, und klicken Sie dann auf **Weiter**.
    
6. Geben Sie auf der nächsten Seite des Assistenten Ihre e-Mail-Adresse in das Feld **an** . 
    
7. Führen Sie im Feld **Betreff** Folgendes ein, um den Umsatzzeitraum mit dem Text Umsatzbericht kombinieren: 
    
   1. Klicken Sie auf die Schaltfläche **Formel** neben dem Feld **Betreff** . 
      
   2. Klicken Sie im Dialogfeld **Formel einfügen** auf **Funktion einfügen**.
      
   3. Klicken Sie in der Liste **Kategorien** auf **Text** , und doppelklicken Sie dann auf **Concat** in der Liste **Funktionen** , klicken Sie im Dialogfeld **Funktion einfügen** . 
      
   4. Ersetzen Sie die erste Instanz von **doppelklicken, um Feld einzufügen** durch den folgenden (einschließlich der einfachen Anführungszeichen): ' Umsatzbericht: ' 
      
   5. Doppelklicken Sie auf die zweite Instanz von **doppelklicken, um Feld einzufügen**.
      
   6. Wählen Sie im Dialogfeld **Feld oder Gruppe auswählen** das Feld Periode. 
      
   7. Löschen Sie die letzte Instanz von **doppelklicken, um Feld einzufügen**, und klicken Sie dann auf **OK**.
    
8. Klicken Sie im Assistenten auf **Weiter**.
    
9. Klicken Sie auf der nächsten Seite des Assistenten geben Sie 'E-Mail Submit' im Feld **Geben Sie einen Namen für diese Datenverbindung** , und klicken Sie dann auf **Fertig stellen**.
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Hinzufügen von Logik zum Senden des Formulars je nach dem Verbindungsstatus eines Benutzercomputers

1. Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Absendeoptionen**.
    
2. Klicken Sie im Dialogfeld **Absendeoptionen** auf **Übermitteln dieses Formulars durch Benutzer zulassen**und wählen Sie dann **benutzerdefinierte Aktion mithilfe von Code ausführen**.
    
3. Klicken Sie auf die Schaltfläche **Code bearbeiten** . 
    
4. Fügen Sie die folgenden beiden Funktionen unter dem [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) -Ereignishandler hinzu: 
    
   ```cs
    public void OnlineSubmit(DocReturnEvent e)
    {
      // Logic for submitting online goes here.
    }
    public void OfflineSubmitX(DocReturnEvent e)
    {
      // Access and submit to the email adapter.
      DataAdaptersCollection myDataAdapters = 
          thisXDocument.DataAdapters;
      EmailAdapterObject submitAdapter = 
          (EmailAdapterObject) myDataAdapters["Email Submit"];
      submitAdapter.Submit();
      // Notify the user that the form was submitted offline.
      System.Text.StringBuilder message = 
      new System.Text.StringBuilder();
      message.Append("You submitted your Sales Report offline. ");
      message.Append("Your Sales Report is in your outbox ");
      message.Append("and will be submitted when you connect to ");
      message.Append("the network.");
        thisXDocument.UI.Alert(message.ToString());
      // The submission was successful.
      e.ReturnStatus = true;
    }
   ```

5. Der **OnSubmitRequest** -Ereignishandlerfunktion die folgende **if** -Anweisung hinzugefügt. 
    
   ```cs
    // Check the computer's connection state.
    if (thisApplication.MachineOnlineState==XdMachineOnlineState.xdOnline)
    {
        OnlineSubmit(e);
    }
    else
    {
        OfflineSubmit(e);
    }
   ```

### <a name="test-the-code"></a>Testen des Codes

1. Klicken Sie im InfoPath-Designer auf der Registerkarte **Start** auf **Vorschau** . 
    
2. Füllen Sie das Formular aus.
    
3. Starten Sie Microsoft Internet Explorer.
    
4. Klicken Sie in Internet Explorer im Menü **Datei** auf **offline arbeiten** . 
    
5. Klicken Sie in InfoPath auf **Senden**. Sie sollte eine Meldung angezeigt, dass das Formular als e-Mail-Nachricht gesendet werden soll.
    
6. Klicken Sie auf **Senden**. Eine Meldung, dass das Formular offline übermittelt wurde sollte angezeigt werden.
    

