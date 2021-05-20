---
title: Arbeiten mit Offlinelösungen mithilfe des InfoPath-Objektmodells
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- solutions [infopath 2007], offline,offline solutions [InfoPath 2007], InfoPath 2003-compatible form templates,InfoPath 2003-compatible form templates, offline solutions
localization_priority: Normal
ms.assetid: 634ccd8c-0b5f-4161-875c-0e546a517377
description: Das InfoPath 2003-kompatible Objektmodell stellt die MachineOnlineState-Eigenschaft des Application-Objekts zur Verfügung, mit der Der Formularcode überprüfen kann, ob der Computer des Benutzers mit dem Netzwerk verbunden ist. Je nach dem Status der Verbindung können vom Formularcode verschiedene Aktionen ausgeführt werden.
ms.openlocfilehash: 452eb0d92b09dc0c3f9b2c247f7cda243dc8eb13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429243"
---
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a>Arbeiten mit Offlinelösungen mithilfe des InfoPath-Objektmodells

Das InfoPath 2003-kompatible Objektmodell stellt die [MachineOnlineState-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) des [Application-Objekts](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) zur Verfügung, mit der Der Formularcode überprüfen kann, ob der Computer des Benutzers mit dem Netzwerk verbunden ist. Je nach dem Status der Verbindung können vom Formularcode verschiedene Aktionen ausgeführt werden. 
  
## <a name="using-the-machineonlinestate-property"></a>Verwenden der MachineOnlineState-Eigenschaft

Im folgenden Beispiel wird gezeigt, wie Sie dem Formularcode Logik hinzufügen können. Mit dieser wird anhand des Online- oder Offlinestatus des Benutzercomputers bestimmt, wie ein Formular gesendet werden soll.
  
Bei dem Beispiel wird davon ausgegangen, dass Sie ein Formular zum Senden eines Umsatzberichts erstellt haben, das ein Feld mit der Bezeichnung "period" (Zeitraum) zur Angabe des im Bericht behandelten Monats und Jahres enthält. Außerdem wird vorausgesetzt, dass Sie bereits eine Datenverbindung und die Logik zum Senden des Berichts, wenn der Benutzer online ist, definiert haben.
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Hinzufügen einer Datenverbindung, die das Formular als Anlage an eine E-Mail-Nachricht sendet

1. Erstellen oder öffnen Sie eine InfoPath-Formularvorlage mit verwaltetem Code.
    
2. Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Datenverbindungen**.
    
3. Klicken Sie im Dialogfeld **Datenverbindungen** auf **Hinzufügen**.
    
4. Klicken Sie **im Assistenten für Datenverbindung** auf **Daten übermitteln,** und klicken Sie dann auf **Weiter**.
    
5. Klicken Sie auf der nächsten Seite des Assistenten auf Als E-Mail-Nachricht, und klicken Sie dann auf **Weiter**. 
    
6. Geben Sie auf der nächsten Seite des Assistenten Ihre E-Mail-Adresse in das Feld **An** ein. 
    
7. Führen Sie im Feld **Betreff** die folgenden Schritte aus, um den Umsatzzeitraum mit dem Text "Sales Report" (Umsatzbericht) zu kombinieren: 
    
   1. Klicken Sie **neben** dem Feld Betreff auf die Schaltfläche **Formel.** 
      
   2. Klicken Sie im Dialogfeld **Formel einfügen** auf **Funktion einfügen**.
      
   3. Klicken Sie im Dialogfeld **Funktion einfügen** in der Liste **Kategorien** auf **Text**, und doppelklicken Sie dann in der Liste **Funktionen** auf **concat**. 
      
   4. Ersetzen Sie die erste Instanz von **Doppelklicken, um Feld einzufügen** durch den folgenden Text (einschließlich der einfachen Anführungszeichen): 'Umsatzbericht: ' 
      
   5. Doppelklicken Sie auf die zweite Instanz von **Doppelklicken, um Feld einzufügen**.
      
   6. Klicken Sie im Dialogfeld **Feld oder Gruppe auswählen** auf das Feld period. 
      
   7. Löschen Sie die letzte Instanz von **Doppelklicken, um Feld einzufügen**, und klicken Sie dann auf **OK**.
    
8. Klicken Sie im Assistenten auf **Weiter**.
    
9. Geben Sie auf der nächsten Seite des Assistenten  im Feld Geben Sie einen Namen für diese Datenverbindung ein, und klicken Sie dann auf **Fertig stellen.**
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Hinzufügen von Logik zum Senden des Formulars je nach dem Verbindungsstatus eines Benutzercomputers

1. Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Absendeoptionen**.
    
2. Klicken Sie im Dialogfeld **Absendeoptionen** auf **Übermitteln dieses Formulars durch Benutzer zulassen**, und wählen Sie dann **Benutzerdefinierte Aktion mithilfe von Code ausführen** aus.
    
3. Klicken Sie auf die Schaltfläche **Code bearbeiten**. 
    
4. Fügen Sie die folgenden beiden Funktionen unterhalb des [OnSubmitRequest-Ereignishandlers](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) hinzu: 
    
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

5. Fügen Sie der **OnSubmitRequest**-Ereignishandlerfunktion die folgende **if**-Anweisung hinzu. 
    
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

1. Klicken Sie im InfoPath-Designer auf der Registerkarte **Start** auf **Vorschau**. 
    
2. Füllen Sie das Formular aus.
    
3. Starten Sie Microsoft Internet Explorer.
    
4. Klicken Sie in Internet Explorer im Menü **Datei** auf **Offline arbeiten**. 
    
5. Klicken Sie in InfoPath auf **Absenden**. Es sollte eine Meldung angezeigt werden, dass das Formular als E-Mail-Nachricht übermittelt wird.
    
6. Klicken Sie auf **Senden**. Eine Meldung sollte mitteilen, dass das Formular offline abgesendet wurde.
    

