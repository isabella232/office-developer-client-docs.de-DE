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
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a><span data-ttu-id="8fe0d-105">Arbeiten mit Offlinelösungen mithilfe des InfoPath-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="8fe0d-105">Work with offline solutions using the InfoPath object model</span></span>

<span data-ttu-id="8fe0d-106">Das InfoPath 2003-kompatible Objektmodell stellt die [MachineOnlineState-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) des [Application-Objekts](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) zur Verfügung, mit der Der Formularcode überprüfen kann, ob der Computer des Benutzers mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-106">The InfoPath 2003-compatible object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) object which enables your form code to check whether the user's computer is connected to the network.</span></span> <span data-ttu-id="8fe0d-107">Je nach dem Status der Verbindung können vom Formularcode verschiedene Aktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-107">Your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="8fe0d-108">Verwenden der MachineOnlineState-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8fe0d-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="8fe0d-109">Im folgenden Beispiel wird gezeigt, wie Sie dem Formularcode Logik hinzufügen können. Mit dieser wird anhand des Online- oder Offlinestatus des Benutzercomputers bestimmt, wie ein Formular gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="8fe0d-p103">Bei dem Beispiel wird davon ausgegangen, dass Sie ein Formular zum Senden eines Umsatzberichts erstellt haben, das ein Feld mit der Bezeichnung "period" (Zeitraum) zur Angabe des im Bericht behandelten Monats und Jahres enthält. Außerdem wird vorausgesetzt, dass Sie bereits eine Datenverbindung und die Logik zum Senden des Berichts, wenn der Benutzer online ist, definiert haben.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-p103">This example assumes that you have created a form for submitting a sales report that contains a field named "period" that specifies the month and year covered in the report. It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span>
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="8fe0d-112">Hinzufügen einer Datenverbindung, die das Formular als Anlage an eine E-Mail-Nachricht sendet</span><span class="sxs-lookup"><span data-stu-id="8fe0d-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="8fe0d-113">Erstellen oder öffnen Sie eine InfoPath-Formularvorlage mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-113">Create or open an InfoPath managed-code form template.</span></span>
    
2. <span data-ttu-id="8fe0d-114">Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Datenverbindungen**.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-114">In InfoPath design mode, on the **Data** tab, click **Data Connections**.</span></span>
    
3. <span data-ttu-id="8fe0d-115">Klicken Sie im Dialogfeld **Datenverbindungen** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="8fe0d-116">Klicken Sie **im Assistenten für Datenverbindung** auf **Daten übermitteln,** und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="8fe0d-117">Klicken Sie auf der nächsten Seite des Assistenten auf Als E-Mail-Nachricht, und klicken Sie dann auf **Weiter**. </span><span class="sxs-lookup"><span data-stu-id="8fe0d-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="8fe0d-118">Geben Sie auf der nächsten Seite des Assistenten Ihre E-Mail-Adresse in das Feld **An** ein.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="8fe0d-119">Führen Sie im Feld **Betreff** die folgenden Schritte aus, um den Umsatzzeitraum mit dem Text "Sales Report" (Umsatzbericht) zu kombinieren:</span><span class="sxs-lookup"><span data-stu-id="8fe0d-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="8fe0d-120">Klicken Sie **neben** dem Feld Betreff auf die Schaltfläche **Formel.**</span><span class="sxs-lookup"><span data-stu-id="8fe0d-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="8fe0d-121">Klicken Sie im Dialogfeld **Formel einfügen** auf **Funktion einfügen**.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="8fe0d-122">Klicken Sie im Dialogfeld **Funktion einfügen** in der Liste **Kategorien** auf **Text**, und doppelklicken Sie dann in der Liste **Funktionen** auf **concat**.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="8fe0d-123">Ersetzen Sie die erste Instanz von **Doppelklicken, um Feld einzufügen** durch den folgenden Text (einschließlich der einfachen Anführungszeichen): 'Umsatzbericht: '</span><span class="sxs-lookup"><span data-stu-id="8fe0d-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="8fe0d-124">Doppelklicken Sie auf die zweite Instanz von **Doppelklicken, um Feld einzufügen**.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="8fe0d-125">Klicken Sie im Dialogfeld **Feld oder Gruppe auswählen** auf das Feld period.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="8fe0d-126">Löschen Sie die letzte Instanz von **Doppelklicken, um Feld einzufügen**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="8fe0d-127">Klicken Sie im Assistenten auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="8fe0d-128">Geben Sie auf der nächsten Seite des Assistenten  im Feld Geben Sie einen Namen für diese Datenverbindung ein, und klicken Sie dann auf **Fertig stellen.**</span><span class="sxs-lookup"><span data-stu-id="8fe0d-128">On the next page of the wizard, type 'Email Submit' in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="8fe0d-129">Hinzufügen von Logik zum Senden des Formulars je nach dem Verbindungsstatus eines Benutzercomputers</span><span class="sxs-lookup"><span data-stu-id="8fe0d-129">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="8fe0d-130">Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Absendeoptionen**.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-130">In InfoPath design mode, on the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="8fe0d-131">Klicken Sie im Dialogfeld **Absendeoptionen** auf **Übermitteln dieses Formulars durch Benutzer zulassen**, und wählen Sie dann **Benutzerdefinierte Aktion mithilfe von Code ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-131">In the **Submit Options** dialog box, click **Allow users to submit this form**, and then select **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="8fe0d-132">Klicken Sie auf die Schaltfläche **Code bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-132">Click the **Edit Code** button.</span></span> 
    
4. <span data-ttu-id="8fe0d-133">Fügen Sie die folgenden beiden Funktionen unterhalb des [OnSubmitRequest-Ereignishandlers](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) hinzu:</span><span class="sxs-lookup"><span data-stu-id="8fe0d-133">Add the following two functions below the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event handler:</span></span> 
    
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

5. <span data-ttu-id="8fe0d-134">Fügen Sie der **OnSubmitRequest**-Ereignishandlerfunktion die folgende **if**-Anweisung hinzu.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-134">Add the following **if** statement to the **OnSubmitRequest** event handler function.</span></span> 
    
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

### <a name="test-the-code"></a><span data-ttu-id="8fe0d-135">Testen des Codes</span><span class="sxs-lookup"><span data-stu-id="8fe0d-135">Test the code</span></span>

1. <span data-ttu-id="8fe0d-136">Klicken Sie im InfoPath-Designer auf der Registerkarte **Start** auf **Vorschau**.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-136">In the InfoPath designer, click **Preview** on the **Home** tab.</span></span> 
    
2. <span data-ttu-id="8fe0d-137">Füllen Sie das Formular aus.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="8fe0d-138">Starten Sie Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="8fe0d-139">Klicken Sie in Internet Explorer im Menü **Datei** auf **Offline arbeiten**.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="8fe0d-140">Klicken Sie in InfoPath auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="8fe0d-141">Es sollte eine Meldung angezeigt werden, dass das Formular als E-Mail-Nachricht übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="8fe0d-p105">Klicken Sie auf **Senden**. Eine Meldung sollte mitteilen, dass das Formular offline abgesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8fe0d-p105">Click **Send**. You should see a message stating that the form has been submitted offline.</span></span>
    

