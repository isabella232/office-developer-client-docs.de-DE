---
title: Arbeiten mit offlinelösungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- offlinelösungen [Infopath 2007] Lösungen [InfoPath 2007], offline, InfoPath 2007, offlinelösungen
localization_priority: Normal
ms.assetid: 108f9bd0-c80f-4790-a572-da2f571a7d85
description: Das InfoPath-Objektmodell enthält die MachineOnlineState-Eigenschaft des Application-Klasse, mit die können Formularcode zu prüfen, ob es sich bei dem Computer des Benutzers mit dem Netzwerk verbunden ist. Überprüfen Sie den Wert der MachineOnlineState-Eigenschaft, kann Ihre Formularcode verschiedene Aktionen je nach Status der Verbindung ausführen.
ms.openlocfilehash: ab149b488d2b2df1e91ba2cb435960c6749ecefb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574559"
---
# <a name="work-with-offline-solutions"></a>Arbeiten mit offlinelösungen

Das InfoPath-Objektmodell enthält die [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) -Eigenschaft des [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse, mit die können Formularcode zu prüfen, ob es sich bei dem Computer des Benutzers mit dem Netzwerk verbunden ist. Überprüfen Sie den Wert der **MachineOnlineState** -Eigenschaft, kann Ihre Formularcode verschiedene Aktionen je nach Status der Verbindung ausführen. 
  
## <a name="using-the-machineonlinestate-property"></a>Mithilfe der MachineOnlineState-Eigenschaft

Im folgenden Beispiel wird gezeigt, wie Sie dem Formularcode Logik hinzufügen können. Mit dieser wird anhand des Online- oder Offlinestatus des Benutzercomputers bestimmt, wie ein Formular gesendet werden soll.
  
In diesem Beispiel wird davon ausgegangen, dass Sie ein Formular zum Senden von einem Umsatzbericht, die enthält ein Feld mit dem Namen an, in dem gibt an, den Monat und Jahr, die im Bericht angezeigte erstellt haben. Es wird davon ausgegangen, dass Sie bereits definiert haben, eine Verbindung von Daten und der Logik zum Senden des Berichts, wenn der Benutzer online ist. 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Hinzufügen einer Datenverbindung, die das Formular als Anlage einer e-Mail-Nachricht sendet

1. Erstellen Sie eine InfoPath-Formularvorlage mithilfe der Vorlage **Leer (InfoPath Editor)**. 
    
2. Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Datenverbindungen**. 
    
3. Klicken Sie im Dialogfeld **Datenverbindungen** auf **Hinzufügen**.
    
4. Klicken Sie im **Datenverbindungs-Assistenten**klicken Sie auf **Daten senden**, und klicken Sie dann auf **Weiter**.
    
5. Klicken Sie auf der nächsten Seite des Assistenten klicken Sie auf **als e-Mail-Nachricht**, und klicken Sie dann auf **Weiter**.
    
6. Geben Sie auf der nächsten Seite des Assistenten Ihre e-Mail-Adresse in das Feld **an** . 
    
7. Führen Sie im Feld **Betreff** die folgenden Schritte aus, um den Umsatzzeitraum mit dem Text "Sales Report" (Umsatzbericht) zu kombinieren: 
    
   1. Klicken Sie auf die Schaltfläche **Formel** neben dem Feld **Betreff** . 
      
   2. Klicken Sie im Dialogfeld **Formel einfügen** auf **Funktion einfügen**.
      
   3. Klicken Sie im Dialogfeld **Funktion einfügen** in der Liste **Kategorien** auf **Text**, und doppelklicken Sie dann in der Liste **Funktionen** auf **verketten**. 
      
   4. Ersetzen Sie die erste Instanz von **Feld mit Doppelklick einfügen** durch den folgenden Text (einschließlich der einfachen Anführungszeichen): 'Sales Report: ' 
      
   5. Doppelklicken Sie auf die zweite Instanz von **Feld mit Doppelklick einfügen**.
      
   6. Klicken Sie im Dialogfeld **Feld oder Gruppe auswählen** auf das Feld für den Zeitraum (period). 
      
   7. Löschen Sie die letzte Instanz von **Feld mit Doppelklick einfügen**, und klicken Sie dann auf **OK**.
    
8. Klicken Sie im Assistenten auf **Weiter**.
    
9. Klicken Sie auf der nächsten Seite des Assistenten klicken Sie auf die Schaltfläche **Formel** neben dem Feld **Name der Anlage** , und wiederholen Sie die oben beschriebenen Schritte zum Erstellen der Formel verketten ("Sales Report"-, Zeitraum), und klicken Sie dann auf **Weiter**.
    
10. Geben Sie auf der letzten Seite des Assistenten im Feld **Geben Sie einen Namen für diese Datenverbindung** E-Mail zu senden, und klicken Sie dann auf **Fertig stellen**.
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Hinzufügen von Logik zum Senden des Formulars je nach dem Verbindungsstatus eines Benutzercomputers

1. Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Absendeoptionen**. 
    
2. Klicken Sie im Dialogfeld **Absendeoptionen** auf **Übermitteln dieses Formulars durch Benutzer zulassen**, wählen Sie **Benutzerdefinierte Aktion mithilfe von Code ausführen** aus, und klicken Sie auf **Code bearbeiten**.
    
3. Fügen Sie die folgenden beiden Funktionen unter dem [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) -Ereignishandler hinzu: 
    
   ```cs
    public void OnlineSubmit(SubmitEventArgs e)
    {
      // Logic for submitting online goes here.
    }
    public void OfflineSubmit(SubmitEventArgs e)
    {
      // Access and submit to the email connection.
      DataConnectionCollection myDataConnections =
          this.DataConnections;
      EmailSubmitConnection submitConnection =
          (EmailSubmitConnection)myDataConnections["Email Submit"];
      submitConnection.Execute();
      // Notify the user that the form was submitted offline.
      System.Text.StringBuilder myMessage = 
          new System.Text.StringBuilder();
      myMessage.Append("You submitted your Sales Report offline. ");
      myMessage.Append("Your Sales Report is in your outbox ");
      myMessage.Append("and will be submitted when you connect to ");
      myMessage.Append("the network.");
        MessageBox.Show(myMessage.ToString());
      // The submission was successful.
      e.CancelableArgs.Cancel = false;
    }
   ```

   ```vb
    Public Sub OnlineSubmit(ByVal e As SubmitEventArgs)
      ' Logic for submitting online goes here.
    End Sub
    Public Sub OfflineSubmit(ByVal e As SubmitEventArgs)
      ' Access and submit to the email connection.
      Dim myDataConnections As DataConnectionCollection = _
          Me.DataConnections
      Dim submitConnection As EmailSubmitConnection = _
          DirectCast(myDataConnections("Email Submit"), _
          EmailSubmitConnection)
      submitConnection.Execute
      ' Notify the user that the form was submitted offline.
      Dim myMessage As System.Text.StringBuilder = _
          New System.Text.StringBuilder()
      myMessage.Append("You submitted your Sales Report offline. ")
      myMessage.Append("Your Sales Report is in your outbox ")
      myMessage.Append("and will be submitted when you connect to ")
      myMessage.Append("the network.")
        MessageBox.Show(myMessage.ToString())
      ' The submission was successful.
      e.CancelableArgs.Cancel = False
    End Sub
   ```

4. Der [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) -Ereignishandlerfunktion die folgende **if** -Anweisung hinzugefügt. 
    
   ```cs
    // Check the computer's connection state.
    if (this.Application.MachineOnlineState == MachineState.Online)
    {
      OnlineSubmit(e);
    }
    else
    {
      OfflineSubmit(e);
    }
   ```

   ```vb
    ' Check the computer's connection state.
    If (Me.Application.MachineOnlineState = MachineState.Online) Then
      OnlineSubmit(e)
    Else
    {
      OfflineSubmit(e)
    End If
   ```

### <a name="test-the-code"></a>Testen des Codes

1. Klicken Sie im Menü **Debuggen** auf **Debuggen starten**.
    
2. Füllen Sie das Formular aus.
    
3. Starten Sie Microsoft Internet Explorer.
    
4. Klicken Sie in Internet Explorer im Menü **Datei** auf **Offlinebetrieb**. 
    
5. Klicken Sie in InfoPath auf **Senden**. Sie sollte eine Meldung angezeigt, dass das Formular als e-Mail-Nachricht gesendet werden soll.
    
6. Klicken Sie auf **Senden**. Eine Meldung sollte mitteilen, dass das Formular offline gesendet wurde und gesendet wird, wenn Sie eine Verbindung mit dem Netzwerk herstellen.
    
## <a name="see-also"></a>Siehe auch

- [Entwerfen einer Formularvorlage für die Offlineverwendung](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)

