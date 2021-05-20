---
title: Arbeiten mit Offlinelösungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- offline solutions [infopath 2007],solutions [InfoPath 2007], offline,InfoPath 2007, offline solutions
localization_priority: Normal
ms.assetid: 108f9bd0-c80f-4790-a572-da2f571a7d85
description: Das InfoPath-Objektmodell stellt die MachineOnlineState-Eigenschaft der Application-Klasse zur Verfügung, mit der Der Formularcode überprüfen kann, ob der Computer des Benutzers mit dem Netzwerk verbunden ist. Durch das Überprüfen des Werts der MachineOnlineState-Eigenschaft kann der Formularcode verschiedene Aktionen ausführen, je nach Status der Verbindung.
ms.openlocfilehash: eb2903c2445a61be803c0d7a2f5ddd7ac7a912ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436139"
---
# <a name="work-with-offline-solutions"></a>Arbeiten mit Offlinelösungen

Das InfoPath-Objektmodell stellt die [MachineOnlineState-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) zur Verfügung, mit der Der Formularcode überprüfen kann, ob der Computer des Benutzers mit dem Netzwerk verbunden ist. Durch das Überprüfen des Werts der **MachineOnlineState**-Eigenschaft kann der Formularcode verschiedene Aktionen ausführen, je nach Status der Verbindung. 
  
## <a name="using-the-machineonlinestate-property"></a>Verwenden der MachineOnlineState-Eigenschaft

Im folgenden Beispiel wird gezeigt, wie Sie dem Formularcode Logik hinzufügen können. Mit dieser wird anhand des Online- oder Offlinestatus des Benutzercomputers bestimmt, wie ein Formular gesendet werden soll.
  
Bei dem Beispiel wird davon ausgegangen, dass Sie ein Formular zum Senden eines Umsatzberichts erstellt haben, das ein Feld mit der Bezeichnung period (Zeitraum) zur Angabe des im Bericht behandelten Monats und Jahres enthält. Außerdem wird vorausgesetzt, dass Sie bereits eine Datenverbindung und die Logik zum Senden des Berichts, wenn der Benutzer online ist, definiert haben. 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Hinzufügen einer Datenverbindung, die das Formular als Anlage an eine E-Mail-Nachricht sendet

1. Erstellen Sie eine InfoPath-Formularvorlage mithilfe der Vorlage **Leer (InfoPath Editor)**. 
    
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
    
9. Klicken Sie auf der nächsten  Seite des Assistenten  neben dem Feld Anlagenname auf die Schaltfläche Formel, und wiederholen Sie dann die oben aufgeführten Schritte, um die Formelverkettung ("Vertriebsbericht - ", Zeitraum") zu erstellen, und klicken Sie dann auf **Weiter**.
    
10. Geben Sie auf der letzten Seite des  Assistenten im Feld Geben Sie einen Namen für diese Datenverbindung ein, und klicken Sie dann auf **Fertig stellen.**
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Hinzufügen von Logik zum Senden des Formulars je nach dem Verbindungsstatus eines Benutzercomputers

1. Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Absendeoptionen**. 
    
2. Klicken Sie im Dialogfeld **Absendeoptionen** auf **Übermitteln dieses Formulars durch Benutzer zulassen**, wählen Sie **Benutzerdefinierte Aktion mithilfe von Code ausführen** aus, und klicken Sie auf **Code bearbeiten**.
    
3. Fügen Sie die folgenden beiden Funktionen unterhalb des [Submit-Ereignishandlers](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) hinzu: 
    
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

4. Fügen Sie der Submit-Ereignishandlerfunktion die folgende **if-Anweisung** hinzu. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) 
    
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
    
4. Klicken Sie in Internet Explorer im Menü **Datei** auf **Offline arbeiten**. 
    
5. Klicken Sie in InfoPath auf **Absenden**. Es sollte eine Meldung angezeigt werden, dass das Formular als E-Mail-Nachricht übermittelt wird.
    
6. Klicken Sie auf **Senden**. Eine Meldung sollte mitteilen, dass das Formular offline gesendet wurde und gesendet wird, wenn Sie eine Verbindung mit dem Netzwerk herstellen.
    
## <a name="see-also"></a>Siehe auch

- [Entwerfen einer Formularvorlage für die Offlineverwendung](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)

