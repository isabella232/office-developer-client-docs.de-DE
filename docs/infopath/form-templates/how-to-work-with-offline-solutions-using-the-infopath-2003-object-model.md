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
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a><span data-ttu-id="d5f33-105">Arbeiten Sie mit offlinelösungen mithilfe des InfoPath-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="d5f33-105">Work with offline solutions using the InfoPath object model</span></span>

<span data-ttu-id="d5f33-106">Das InfoPath 2003-kompatible Objektmodell bietet die [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) -Eigenschaft des [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) -Objekts ermöglicht Formularcode zu prüfen, ob es sich bei dem Computer des Benutzers mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d5f33-106">The InfoPath 2003-compatible object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) object which enables your form code to check whether the user's computer is connected to the network.</span></span> <span data-ttu-id="d5f33-107">Formularcode kann je nach Status der Verbindung verschiedene Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5f33-107">Your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="d5f33-108">Mithilfe der MachineOnlineState-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d5f33-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="d5f33-109">Im folgenden Beispiel wird gezeigt, wie Sie dem Formularcode Logik hinzufügen können. Mit dieser wird anhand des Online- oder Offlinestatus des Benutzercomputers bestimmt, wie ein Formular gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5f33-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="d5f33-p103">Bei dem Beispiel wird davon ausgegangen, dass Sie ein Formular zum Senden eines Umsatzberichts erstellt haben, das ein Feld mit der Bezeichnung "period" (Zeitraum) zur Angabe des im Bericht behandelten Monats und Jahres enthält. Außerdem wird vorausgesetzt, dass Sie bereits eine Datenverbindung und die Logik zum Senden des Berichts, wenn der Benutzer online ist, definiert haben.</span><span class="sxs-lookup"><span data-stu-id="d5f33-p103">This example assumes that you have created a form for submitting a sales report that contains a field named "period" that specifies the month and year covered in the report. It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span>
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="d5f33-112">Hinzufügen einer Datenverbindung, die das Formular als Anlage einer e-Mail-Nachricht sendet</span><span class="sxs-lookup"><span data-stu-id="d5f33-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="d5f33-113">Erstellen oder öffnen Sie eine InfoPath-Formularvorlage mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="d5f33-113">Create or open an InfoPath managed-code form template.</span></span>
    
2. <span data-ttu-id="d5f33-114">Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Datenverbindungen**.</span><span class="sxs-lookup"><span data-stu-id="d5f33-114">In InfoPath design mode, on the **Data** tab, click **Data Connections**.</span></span>
    
3. <span data-ttu-id="d5f33-115">Klicken Sie im Dialogfeld **Datenverbindungen** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="d5f33-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="d5f33-116">Klicken Sie im **Datenverbindungs-Assistenten**klicken Sie auf **Daten senden**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="d5f33-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="d5f33-117">Klicken Sie auf der nächsten Seite des Assistenten klicken Sie auf **als e-Mail-Nachricht**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="d5f33-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="d5f33-118">Geben Sie auf der nächsten Seite des Assistenten Ihre e-Mail-Adresse in das Feld **an** .</span><span class="sxs-lookup"><span data-stu-id="d5f33-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="d5f33-119">Führen Sie im Feld **Betreff** Folgendes ein, um den Umsatzzeitraum mit dem Text Umsatzbericht kombinieren:</span><span class="sxs-lookup"><span data-stu-id="d5f33-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="d5f33-120">Klicken Sie auf die Schaltfläche **Formel** neben dem Feld **Betreff** .</span><span class="sxs-lookup"><span data-stu-id="d5f33-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="d5f33-121">Klicken Sie im Dialogfeld **Formel einfügen** auf **Funktion einfügen**.</span><span class="sxs-lookup"><span data-stu-id="d5f33-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="d5f33-122">Klicken Sie in der Liste **Kategorien** auf **Text** , und doppelklicken Sie dann auf **Concat** in der Liste **Funktionen** , klicken Sie im Dialogfeld **Funktion einfügen** .</span><span class="sxs-lookup"><span data-stu-id="d5f33-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="d5f33-123">Ersetzen Sie die erste Instanz von **doppelklicken, um Feld einzufügen** durch den folgenden (einschließlich der einfachen Anführungszeichen): ' Umsatzbericht: '</span><span class="sxs-lookup"><span data-stu-id="d5f33-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="d5f33-124">Doppelklicken Sie auf die zweite Instanz von **doppelklicken, um Feld einzufügen**.</span><span class="sxs-lookup"><span data-stu-id="d5f33-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="d5f33-125">Wählen Sie im Dialogfeld **Feld oder Gruppe auswählen** das Feld Periode.</span><span class="sxs-lookup"><span data-stu-id="d5f33-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="d5f33-126">Löschen Sie die letzte Instanz von **doppelklicken, um Feld einzufügen**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5f33-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="d5f33-127">Klicken Sie im Assistenten auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="d5f33-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="d5f33-128">Klicken Sie auf der nächsten Seite des Assistenten geben Sie 'E-Mail Submit' im Feld **Geben Sie einen Namen für diese Datenverbindung** , und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="d5f33-128">On the next page of the wizard, type 'Email Submit' in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="d5f33-129">Hinzufügen von Logik zum Senden des Formulars je nach dem Verbindungsstatus eines Benutzercomputers</span><span class="sxs-lookup"><span data-stu-id="d5f33-129">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="d5f33-130">Klicken Sie im InfoPath-Entwurfsmodus auf der Registerkarte **Daten** auf **Absendeoptionen**.</span><span class="sxs-lookup"><span data-stu-id="d5f33-130">In InfoPath design mode, on the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="d5f33-131">Klicken Sie im Dialogfeld **Absendeoptionen** auf **Übermitteln dieses Formulars durch Benutzer zulassen**und wählen Sie dann **benutzerdefinierte Aktion mithilfe von Code ausführen**.</span><span class="sxs-lookup"><span data-stu-id="d5f33-131">In the **Submit Options** dialog box, click **Allow users to submit this form**, and then select **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="d5f33-132">Klicken Sie auf die Schaltfläche **Code bearbeiten** .</span><span class="sxs-lookup"><span data-stu-id="d5f33-132">Click the **Edit Code** button.</span></span> 
    
4. <span data-ttu-id="d5f33-133">Fügen Sie die folgenden beiden Funktionen unter dem [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) -Ereignishandler hinzu:</span><span class="sxs-lookup"><span data-stu-id="d5f33-133">Add the following two functions below the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event handler:</span></span> 
    
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

5. <span data-ttu-id="d5f33-134">Der **OnSubmitRequest** -Ereignishandlerfunktion die folgende **if** -Anweisung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d5f33-134">Add the following **if** statement to the **OnSubmitRequest** event handler function.</span></span> 
    
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

### <a name="test-the-code"></a><span data-ttu-id="d5f33-135">Testen des Codes</span><span class="sxs-lookup"><span data-stu-id="d5f33-135">Test the code</span></span>

1. <span data-ttu-id="d5f33-136">Klicken Sie im InfoPath-Designer auf der Registerkarte **Start** auf **Vorschau** .</span><span class="sxs-lookup"><span data-stu-id="d5f33-136">In the InfoPath designer, click **Preview** on the **Home** tab.</span></span> 
    
2. <span data-ttu-id="d5f33-137">Füllen Sie das Formular aus.</span><span class="sxs-lookup"><span data-stu-id="d5f33-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="d5f33-138">Starten Sie Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d5f33-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="d5f33-139">Klicken Sie in Internet Explorer im Menü **Datei** auf **offline arbeiten** .</span><span class="sxs-lookup"><span data-stu-id="d5f33-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="d5f33-140">Klicken Sie in InfoPath auf **Senden**.</span><span class="sxs-lookup"><span data-stu-id="d5f33-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="d5f33-141">Sie sollte eine Meldung angezeigt, dass das Formular als e-Mail-Nachricht gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5f33-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="d5f33-142">Klicken Sie auf **Senden**.</span><span class="sxs-lookup"><span data-stu-id="d5f33-142">Click **Send**.</span></span> <span data-ttu-id="d5f33-143">Eine Meldung, dass das Formular offline übermittelt wurde sollte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d5f33-143">You should see a message stating that the form has been submitted offline.</span></span>
    

