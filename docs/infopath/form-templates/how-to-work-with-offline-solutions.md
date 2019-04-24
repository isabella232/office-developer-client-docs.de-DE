---
title: Arbeiten mit Offlinelösungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Offlinelösungen [InfoPath 2007], Lösungen [InfoPath 2007], offline, InfoPath 2007, Offlinelösungen
localization_priority: Normal
ms.assetid: 108f9bd0-c80f-4790-a572-da2f571a7d85
description: Das InfoPath-Objektmodell stellt die MachineOnlineState-Eigenschaft der Application-Klasse bereit, mit deren Hilfe der Formularcode überprüfen kann, ob der Computer des Benutzers mit dem Netzwerk verbunden ist. Durch das Überprüfen des Werts der MachineOnlineState-Eigenschaft kann der Formularcode verschiedene Aktionen ausführen, je nach Status der Verbindung.
ms.openlocfilehash: eb2903c2445a61be803c0d7a2f5ddd7ac7a912ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299818"
---
# <a name="work-with-offline-solutions"></a><span data-ttu-id="63eae-105">Arbeiten mit Offlinelösungen</span><span class="sxs-lookup"><span data-stu-id="63eae-105">Work with offline solutions</span></span>

<span data-ttu-id="63eae-106">Das InfoPath-Objektmodell stellt die [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) -Eigenschaft der [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse bereit, mit deren Hilfe der Formularcode überprüfen kann, ob der Computer des Benutzers mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="63eae-106">The InfoPath object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that enables your form code to check whether the user's computer is connected to the network.</span></span> <span data-ttu-id="63eae-107">Durch das Überprüfen des Werts der **MachineOnlineState**-Eigenschaft kann der Formularcode verschiedene Aktionen ausführen, je nach Status der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="63eae-107">By checking the value of **MachineOnlineState** property, your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="63eae-108">Verwenden der MachineOnlineState-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="63eae-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="63eae-109">Im folgenden Beispiel wird gezeigt, wie Sie dem Formularcode Logik hinzufügen können. Mit dieser wird anhand des Online- oder Offlinestatus des Benutzercomputers bestimmt, wie ein Formular gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63eae-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="63eae-110">Bei dem Beispiel wird davon ausgegangen, dass Sie ein Formular zum Senden eines Umsatzberichts erstellt haben, das ein Feld mit der Bezeichnung period (Zeitraum) zur Angabe des im Bericht behandelten Monats und Jahres enthält.</span><span class="sxs-lookup"><span data-stu-id="63eae-110">This example assumes that you have created a form for submitting a sales report that contains a field named period that specifies the month and year covered in the report.</span></span> <span data-ttu-id="63eae-111">Außerdem wird vorausgesetzt, dass Sie bereits eine Datenverbindung und die Logik zum Senden des Berichts, wenn der Benutzer online ist, definiert haben.</span><span class="sxs-lookup"><span data-stu-id="63eae-111">It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span> 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="63eae-112">Hinzufügen einer Datenverbindung, die das Formular als Anlage an eine e-Mail-Nachricht sendet</span><span class="sxs-lookup"><span data-stu-id="63eae-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="63eae-113">Erstellen Sie eine InfoPath-Formularvorlage mithilfe der Vorlage **Leer (InfoPath Editor)**.</span><span class="sxs-lookup"><span data-stu-id="63eae-113">Create an InfoPath form template using the **Blank (InfoPath Editor)** template.</span></span> 
    
2. <span data-ttu-id="63eae-114">Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Datenverbindungen**.</span><span class="sxs-lookup"><span data-stu-id="63eae-114">In InfoPath design mode, click **Data Connections** on the **Data** tab.</span></span> 
    
3. <span data-ttu-id="63eae-115">Klicken Sie im Dialogfeld **Datenverbindungen** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="63eae-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="63eae-116">Klicken Sie im datenVerbindungs- **Assistenten**auf **Daten senden**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="63eae-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="63eae-117">Klicken Sie auf der nächsten Seite des Assistenten auf **als e-Mail-Nachricht**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="63eae-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="63eae-118">Geben Sie auf der nächsten Seite des Assistenten im Feld **an** Ihre e-Mail-Adresse ein.</span><span class="sxs-lookup"><span data-stu-id="63eae-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="63eae-119">Führen Sie im Feld **Betreff** die folgenden Schritte aus, um den Umsatzzeitraum mit dem Text "Sales Report" (Umsatzbericht) zu kombinieren:</span><span class="sxs-lookup"><span data-stu-id="63eae-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="63eae-120">Klicken Sie neben dem Feld **Betreff** auf die Schaltfläche **Formel** .</span><span class="sxs-lookup"><span data-stu-id="63eae-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="63eae-121">Klicken Sie im Dialogfeld **Formel einfügen** auf **Funktion einfügen**.</span><span class="sxs-lookup"><span data-stu-id="63eae-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="63eae-122">Klicken Sie im Dialogfeld **Funktion einfügen** in der Liste **Kategorien** auf **Text**, und doppelklicken Sie dann in der Liste **Funktionen** auf **concat**.</span><span class="sxs-lookup"><span data-stu-id="63eae-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="63eae-123">Ersetzen Sie die erste Instanz von **Doppelklicken, um Feld einzufügen** durch den folgenden Text (einschließlich der einfachen Anführungszeichen): 'Umsatzbericht: '</span><span class="sxs-lookup"><span data-stu-id="63eae-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="63eae-124">Doppelklicken Sie auf die zweite Instanz von **Doppelklicken, um Feld einzufügen**.</span><span class="sxs-lookup"><span data-stu-id="63eae-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="63eae-125">Klicken Sie im Dialogfeld **Feld oder Gruppe auswählen** auf das Feld period.</span><span class="sxs-lookup"><span data-stu-id="63eae-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="63eae-126">Löschen Sie die letzte Instanz von **Doppelklicken, um Feld einzufügen**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="63eae-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="63eae-127">Klicken Sie im Assistenten auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="63eae-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="63eae-128">Klicken Sie auf der nächsten Seite des Assistenten auf die Schaltfläche **Formel** neben dem Feld **Anlagen Name** , und wiederholen Sie die Schritte oben, um die Formel Concat ("Umsatzbericht-", Zeitraum) zu erstellen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="63eae-128">On the next page of the wizard, click the **Formula** button next to the **Attachment Name** box, and then repeat the steps above to create the formula concat("Sales Report - ", period), and then click **Next**.</span></span>
    
10. <span data-ttu-id="63eae-129">Geben Sie auf der letzten Seite des Assistenten im Feld **Geben Sie einen Namen für diese Datenverbindung ein** die Option e-Mail-übermitteln ein ein, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="63eae-129">On the last page of the wizard, type Email Submit in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="63eae-130">Hinzufügen von Logik zum Senden des Formulars je nach dem Verbindungsstatus eines Benutzercomputers</span><span class="sxs-lookup"><span data-stu-id="63eae-130">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="63eae-131">Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Absendeoptionen**.</span><span class="sxs-lookup"><span data-stu-id="63eae-131">In InfoPath design mode, click **Submit Options** on the **Data** tab.</span></span> 
    
2. <span data-ttu-id="63eae-132">Klicken Sie im Dialogfeld **Absendeoptionen** auf **Übermitteln dieses Formulars durch Benutzer zulassen**, wählen Sie **Benutzerdefinierte Aktion mithilfe von Code ausführen** aus, und klicken Sie auf **Code bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="63eae-132">In the **Submit Options** dialog box, click **Allow users to submit this form**, select **Perform custom action using Code**, click **Edit Code**.</span></span>
    
3. <span data-ttu-id="63eae-133">Fügen Sie die folgenden beiden Funktionen unterhalb des [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) -Ereignishandlers hinzu:</span><span class="sxs-lookup"><span data-stu-id="63eae-133">Add the following two functions below the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler:</span></span> 
    
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

4. <span data-ttu-id="63eae-134">Fügen Sie der [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) -Ereignis Handlerfunktion die folgende **if** -Anweisung hinzu.</span><span class="sxs-lookup"><span data-stu-id="63eae-134">Add the following **if** statement to the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler function.</span></span> 
    
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

### <a name="test-the-code"></a><span data-ttu-id="63eae-135">Testen des Codes</span><span class="sxs-lookup"><span data-stu-id="63eae-135">Test the code</span></span>

1. <span data-ttu-id="63eae-136">Klicken Sie im Menü **Debuggen** auf **Debuggen starten**.</span><span class="sxs-lookup"><span data-stu-id="63eae-136">On the **Debug** menu, click **Start Debugging**.</span></span>
    
2. <span data-ttu-id="63eae-137">Füllen Sie das Formular aus.</span><span class="sxs-lookup"><span data-stu-id="63eae-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="63eae-138">Starten Sie Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="63eae-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="63eae-139">Klicken Sie in Internet Explorer im Menü **Datei** auf **Offline arbeiten**.</span><span class="sxs-lookup"><span data-stu-id="63eae-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="63eae-140">Klicken Sie in InfoPath auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="63eae-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="63eae-141">Es sollte eine Meldung angezeigt werden, dass das Formular als e-Mail-Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="63eae-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="63eae-p105">Klicken Sie auf **Senden**. Eine Meldung sollte mitteilen, dass das Formular offline gesendet wurde und gesendet wird, wenn Sie eine Verbindung mit dem Netzwerk herstellen.</span><span class="sxs-lookup"><span data-stu-id="63eae-p105">Click **Send**. You should see a message stating that the form has been submitted offline and will be submitted when you connect to the network.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63eae-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63eae-144">See also</span></span>

- [<span data-ttu-id="63eae-145">Entwerfen einer Formularvorlage für die Offlineverwendung</span><span class="sxs-lookup"><span data-stu-id="63eae-145">Design a form template for offline use</span></span>](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)

