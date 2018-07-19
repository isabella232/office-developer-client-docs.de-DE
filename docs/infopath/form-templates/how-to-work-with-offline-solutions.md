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
ms.openlocfilehash: fcdaae31dd6a0c76cf1c453f267be430a2b34bba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790747"
---
# <a name="work-with-offline-solutions"></a><span data-ttu-id="c6c17-105">Arbeiten mit offlinelösungen</span><span class="sxs-lookup"><span data-stu-id="c6c17-105">Work with offline solutions</span></span>

<span data-ttu-id="c6c17-106">Das InfoPath-Objektmodell enthält die [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) -Eigenschaft des [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse, mit die können Formularcode zu prüfen, ob es sich bei dem Computer des Benutzers mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c6c17-106">The InfoPath object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that enables your form code to check whether the user's computer is connected to the network.</span></span> <span data-ttu-id="c6c17-107">Überprüfen Sie den Wert der **MachineOnlineState** -Eigenschaft, kann Ihre Formularcode verschiedene Aktionen je nach Status der Verbindung ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6c17-107">By checking the value of **MachineOnlineState** property, your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="c6c17-108">Mithilfe der MachineOnlineState-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c6c17-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="c6c17-109">Im folgenden Beispiel wird gezeigt, wie Sie dem Formularcode Logik hinzufügen können. Mit dieser wird anhand des Online- oder Offlinestatus des Benutzercomputers bestimmt, wie ein Formular gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6c17-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="c6c17-110">In diesem Beispiel wird davon ausgegangen, dass Sie ein Formular zum Senden von einem Umsatzbericht, die enthält ein Feld mit dem Namen an, in dem gibt an, den Monat und Jahr, die im Bericht angezeigte erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c6c17-110">This example assumes that you have created a form for submitting a sales report that contains a field named period that specifies the month and year covered in the report.</span></span> <span data-ttu-id="c6c17-111">Es wird davon ausgegangen, dass Sie bereits definiert haben, eine Verbindung von Daten und der Logik zum Senden des Berichts, wenn der Benutzer online ist.</span><span class="sxs-lookup"><span data-stu-id="c6c17-111">It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span> 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="c6c17-112">Hinzufügen einer Datenverbindung, die das Formular als Anlage einer e-Mail-Nachricht sendet</span><span class="sxs-lookup"><span data-stu-id="c6c17-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="c6c17-113">Erstellen einer InfoPath-Formularvorlage mithilfe der Vorlage **leer (InfoPath Editor)** .</span><span class="sxs-lookup"><span data-stu-id="c6c17-113">Create an InfoPath form template using the **Blank (InfoPath Editor)** template.</span></span> 
    
2. <span data-ttu-id="c6c17-114">Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Datenverbindungen** .</span><span class="sxs-lookup"><span data-stu-id="c6c17-114">In InfoPath design mode, click **Data Connections** on the **Data** tab.</span></span> 
    
3. <span data-ttu-id="c6c17-115">Klicken Sie im Dialogfeld **Datenverbindungen** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="c6c17-116">Klicken Sie im **Datenverbindungs-Assistenten**klicken Sie auf **Daten senden**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="c6c17-117">Klicken Sie auf der nächsten Seite des Assistenten klicken Sie auf **als e-Mail-Nachricht**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="c6c17-118">Geben Sie auf der nächsten Seite des Assistenten Ihre e-Mail-Adresse in das Feld **an** .</span><span class="sxs-lookup"><span data-stu-id="c6c17-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="c6c17-119">Führen Sie im Feld **Betreff** Folgendes ein, um den Umsatzzeitraum mit dem Text Umsatzbericht kombinieren:</span><span class="sxs-lookup"><span data-stu-id="c6c17-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="c6c17-120">Klicken Sie auf die Schaltfläche **Formel** neben dem Feld **Betreff** .</span><span class="sxs-lookup"><span data-stu-id="c6c17-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="c6c17-121">Klicken Sie im Dialogfeld **Formel einfügen** auf **Funktion einfügen**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="c6c17-122">Klicken Sie in der Liste **Kategorien** auf **Text** , und doppelklicken Sie dann auf **Concat** in der Liste **Funktionen** , klicken Sie im Dialogfeld **Funktion einfügen** .</span><span class="sxs-lookup"><span data-stu-id="c6c17-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="c6c17-123">Ersetzen Sie die erste Instanz von **doppelklicken, um Feld einzufügen** durch den folgenden (einschließlich der einfachen Anführungszeichen): ' Umsatzbericht: '</span><span class="sxs-lookup"><span data-stu-id="c6c17-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="c6c17-124">Doppelklicken Sie auf die zweite Instanz von **doppelklicken, um Feld einzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="c6c17-125">Wählen Sie im Dialogfeld **Feld oder Gruppe auswählen** das Feld Periode.</span><span class="sxs-lookup"><span data-stu-id="c6c17-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="c6c17-126">Löschen Sie die letzte Instanz von **doppelklicken, um Feld einzufügen**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="c6c17-127">Klicken Sie im Assistenten auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="c6c17-128">Klicken Sie auf der nächsten Seite des Assistenten klicken Sie auf die Schaltfläche **Formel** neben dem Feld **Name der Anlage** , und wiederholen Sie die oben beschriebenen Schritte zum Erstellen der Formel verketten ("Sales Report"-, Zeitraum), und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-128">On the next page of the wizard, click the **Formula** button next to the **Attachment Name** box, and then repeat the steps above to create the formula concat("Sales Report - ", period), and then click **Next**.</span></span>
    
10. <span data-ttu-id="c6c17-129">Geben Sie auf der letzten Seite des Assistenten im Feld **Geben Sie einen Namen für diese Datenverbindung** E-Mail zu senden, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-129">On the last page of the wizard, type Email Submit in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="c6c17-130">Hinzufügen von Logik zum Senden des Formulars je nach dem Verbindungsstatus eines Benutzercomputers</span><span class="sxs-lookup"><span data-stu-id="c6c17-130">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="c6c17-131">Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Absendeoptionen** .</span><span class="sxs-lookup"><span data-stu-id="c6c17-131">In InfoPath design mode, click **Submit Options** on the **Data** tab.</span></span> 
    
2. <span data-ttu-id="c6c17-132">Klicken Sie im Dialogfeld **Absendeoptionen** klicken Sie auf **Übermitteln dieses Formulars durch Benutzer zulassen**, wählen Sie **benutzerdefinierte Aktion mithilfe von Code ausführen**, klicken Sie auf **Code bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-132">In the **Submit Options** dialog box, click **Allow users to submit this form**, select **Perform custom action using Code**, click **Edit Code**.</span></span>
    
3. <span data-ttu-id="c6c17-133">Fügen Sie die folgenden beiden Funktionen unter dem [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) -Ereignishandler hinzu:</span><span class="sxs-lookup"><span data-stu-id="c6c17-133">Add the following two functions below the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler:</span></span> 
    
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

4. <span data-ttu-id="c6c17-134">Der [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) -Ereignishandlerfunktion die folgende **if** -Anweisung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c6c17-134">Add the following **if** statement to the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler function.</span></span> 
    
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

### <a name="test-the-code"></a><span data-ttu-id="c6c17-135">Testen des Codes</span><span class="sxs-lookup"><span data-stu-id="c6c17-135">Test the code</span></span>

1. <span data-ttu-id="c6c17-136">Klicken Sie im Menü **Debuggen** auf **Debuggen starten**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-136">On the **Debug** menu, click **Start Debugging**.</span></span>
    
2. <span data-ttu-id="c6c17-137">Füllen Sie das Formular aus.</span><span class="sxs-lookup"><span data-stu-id="c6c17-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="c6c17-138">Starten Sie Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c6c17-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="c6c17-139">Klicken Sie in Internet Explorer im Menü **Datei** auf **offline arbeiten** .</span><span class="sxs-lookup"><span data-stu-id="c6c17-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="c6c17-140">Klicken Sie in InfoPath auf **Senden**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="c6c17-141">Sie sollte eine Meldung angezeigt, dass das Formular als e-Mail-Nachricht gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6c17-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="c6c17-142">Klicken Sie auf **Senden**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-142">Click **Send**.</span></span> <span data-ttu-id="c6c17-143">Finden Sie unter eine Meldung angezeigt, dass das Formular offline übermittelt wurde und beim Herstellen einer Verbindung mit des Netzwerks gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6c17-143">You should see a message stating that the form has been submitted offline and will be submitted when you connect to the network.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6c17-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6c17-144">See also</span></span>

- [<span data-ttu-id="c6c17-145">Entwerfen einer Formularvorlage für die Offlineverwendung</span><span class="sxs-lookup"><span data-stu-id="c6c17-145">Design a form template for offline use</span></span>](http://office.microsoft.com/de-de/infopath/HA102117391033.aspx?pid=CH100341121033)

