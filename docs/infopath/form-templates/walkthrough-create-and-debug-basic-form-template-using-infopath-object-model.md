---
title: 'Exemplarische vorGehensWeise: Erstellen und Debuggen einer einfachen Formularvorlage mit dem InfoPath-Objektmodell'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- Formularvorlagen [InfoPath 2007], Exemplarische Vorgehensweisen, Formularvorlagen [InfoPath 2007], Erstellen von InfoPath 2003-kompatiblen, InfoPath 2003-kompatiblen Formularvorlagen, Exemplarische Vorgehensweisen
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: Dieses Thema bietet eine exemplarische Vorgehensweise zum Erstellen einer einfachen InfoPath-Formularvorlage mit verwaltetem Code, die mit dem InfoPath 2003-kompatiblen Objektmodell verwendet wird, das vom Microsoft. Office. Interop. InfoPath. SemiTrust-Namespace bereitgestellt wird.
ms.openlocfilehash: c559aedad5c62134c796196c63c1a84f70c4dc3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303199"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a><span data-ttu-id="18e60-104">Exemplarische vorGehensWeise: Erstellen und Debuggen einer einfachen Formularvorlage mit dem InfoPath-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="18e60-104">Walkthrough: Create and debug a basic form template using the InfoPath object model</span></span>

<span data-ttu-id="18e60-105">Dieses Thema bietet eine exemplarische Vorgehensweise zum Erstellen einer einfachen InfoPath-Formularvorlage mit verwaltetem Code, die mit dem InfoPath 2003-kompatiblen Objektmodell verwendet wird, das vom [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="18e60-105">This topic provides a walkthrough of creating a basic InfoPath managed code form template that works with the InfoPath 2003-compatible object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
## <a name="hello-world"></a><span data-ttu-id="18e60-106">Hello World</span><span class="sxs-lookup"><span data-stu-id="18e60-106">Hello World</span></span>

<span data-ttu-id="18e60-107">Im folgenden Beispiel erfahren Sie, wie Sie mithilfe der [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) -Methode des InfoPath 2003-kompatiblen Objektmodells ein einfaches Warnungsdialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="18e60-107">In the following example, you will learn how to display a simple alert dialog box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the InfoPath 2003-compatible object model.</span></span> 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a><span data-ttu-id="18e60-108">Erstellen einer neuen InfoPath-Formularvorlage, die das InfoPath 2003-kompatible Objektmodell verwendet</span><span class="sxs-lookup"><span data-stu-id="18e60-108">Create a new InfoPath form template that works with the InfoPath 2003-compatible object model</span></span>

1. <span data-ttu-id="18e60-109">Erstellen Sie eine neue Formularvorlage, die mit dem InfoPath 2003-kompatiblen Objektmodell verwendet werden kann, wie unter [Erstellen einer Formularvorlage mit dem infopath 2003-Objektmodell](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="18e60-109">Create a new form template that works with the InfoPath 2003-compatible object model, as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).</span></span>
    
2. <span data-ttu-id="18e60-110">Geben Sie dem Formularvorlagenprojekt den Namen HelloWorld, und speichern Sie es.</span><span class="sxs-lookup"><span data-stu-id="18e60-110">Name the form template project HelloWorld and save it.</span></span> 
    
   <span data-ttu-id="18e60-p101">Das Projektsystem erstellt Code- und Projektdateien und öffnet dann eine leere Formularvorlage im InfoPath-Entwurfsmodus. Jetzt können Sie Ereignishandler hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="18e60-p101">The project system creates code and project files, and then opens a blank form template in InfoPath design mode. You are now ready to add event handlers.</span></span>
    
### <a name="add-a-button-with-an-onclick-event-handler"></a><span data-ttu-id="18e60-113">Hinzufügen einer Schaltfläche mit einem OnClick-Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="18e60-113">Add a button with an OnClick event handler</span></span>

1. <span data-ttu-id="18e60-114">Klicken Sie auf der Registerkarte **Start** im Abschnitt **Steuerelemente** auf das Steuerelement **Schaltfläche**, um dieses in die Ansicht einzufügen.</span><span class="sxs-lookup"><span data-stu-id="18e60-114">In the **Controls** section on the **Home** tab, click the **Button** control to insert it into the view.</span></span> 
    
2. <span data-ttu-id="18e60-115">Klicken Sie mit der rechten Maustaste auf das Steuerelement, und klicken Sie dann auf **Schaltflächeneigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="18e60-115">Right-click the control, and then click **Button Properties**.</span></span>
    
3. <span data-ttu-id="18e60-116">Ändern Sie die **Bezeichnung** in Alert.</span><span class="sxs-lookup"><span data-stu-id="18e60-116">Change the **Label** to Alert.</span></span>
    
4. <span data-ttu-id="18e60-117">Ändern Sie die ID in die Warnungs **Kennung** .</span><span class="sxs-lookup"><span data-stu-id="18e60-117">Change the **ID** to AlertID.</span></span>
    
5. <span data-ttu-id="18e60-118">Klicken Sie auf **Formularcode bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="18e60-118">Click **Edit Form Code**.</span></span>
    
   <span data-ttu-id="18e60-119">Ein Ereignishandler-Skelett für [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) das OnClick-Ereignis wird erstellt, und der Fokus wechselt zum Code-Editor in Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="18e60-119">An event handler skeleton for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event is created and the focus moves to the code editor in Visual Studio 2012.</span></span> <span data-ttu-id="18e60-120">Weitere Informationen zum Arbeiten mit Ereignishandlern finden Sie unter [Hinzufügen eines Ereignishandlers mit dem InfoPath-Objektmodell 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="18e60-120">For more information on working with event handlers, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span> 
    
   <span data-ttu-id="18e60-121">Jetzt können Sie dem Ereignishandler für die Schaltfläche Formularcode hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="18e60-121">You are now ready to add form code to the event handler for the button.</span></span>
    
### <a name="add-form-code-to-the-event-handler"></a><span data-ttu-id="18e60-122">Hinzufügen von Formularcode zum Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="18e60-122">Add form code to the event handler</span></span>

1. <span data-ttu-id="18e60-123">Geben Sie im **OnClick**-Ereignishandler den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="18e60-123">In the **OnClick** event handler, type the following code:</span></span> 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="18e60-p103">Beachten Sie, dass nach der Eingabe jedes Punktes in der Codezeile eine Microsoft IntelliSense-Dropdownliste angezeigt wird. Der gesamte Ereignishandler sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="18e60-p103">Note that a Microsoft IntelliSense drop-down list is displayed after you type each period in the line of code. The entire event handler should look like the following:</span></span>
    
   ```cs
    [InfoPathEventHandler(MatchPath="AlertID", EventType=InfoPathEventType.OnClick)]
    public void AlertID_OnClick(DocActionEvent e)
    {
        thisXDocument.UI.Alert("Hello World!");
    }
   ```

   ```vb
    <InfoPathEventHandler(MatchPath:="AlertID", EventType:=InfoPathEventType.OnClick)>
    Public Sub AlertID_OnClick(ByVal e As DocActionEvent)
        thisXDocument.UI.Alert("Hello World!")
    End Sub
   ```

   > [!NOTE]
   > <span data-ttu-id="18e60-126">Alternativ zur Verwendung der **Alert**-Methode können Sie die **MessageBox.Show**-Methode des **System.Windows.Forms**-Namespace verwenden, um ein Meldungsfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="18e60-126">As an alternative to using the **Alert** method, you can use the **MessageBox.Show** method of the **System.Windows.Forms** namespace to display a message box.</span></span> <span data-ttu-id="18e60-127">Zu diesem Zweck müssen Sie einen Verweis auf die System. Windows. Forms-Assembly, hinzufügen `using System.Windows.Forms;` oder `Imports System.Windows.Forms` zu den Direktiven am Anfang der Codedatei hinzufügen und dann eine Codezeile wie die folgende eingeben:`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span><span class="sxs-lookup"><span data-stu-id="18e60-127">To do so, you must add a reference to the System.Windows.Forms assembly, add  `using System.Windows.Forms;` or  `Imports System.Windows.Forms` to the directives at the beginning of your code file, and then type a line of code such as the following:  `MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span></span>
  
2. <span data-ttu-id="18e60-128">Wechseln Sie zum InfoPath-Entwurfsmodusfenster, und klicken Sie dann auf der Registerkarte **Start** auf die Schaltfläche **Vorschau**.</span><span class="sxs-lookup"><span data-stu-id="18e60-128">Switch to the InfoPath design mode window, and then click the **Preview** button on the **Home** tab.</span></span> 
    
3. <span data-ttu-id="18e60-129">Klicken Sie im\*\*\*\* Vorschaufenster auf die Schaltfläche **Alert**.</span><span class="sxs-lookup"><span data-stu-id="18e60-129">In the **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="18e60-130">Ein Meldungsfeld mit dem Text "Hello World!" wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="18e60-130">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="18e60-131">Im nächsten Verfahren wird gezeigt, wie Sie dem Formularcode Haltepunkte für das Debuggen hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="18e60-131">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="18e60-132">Debuggen von Formularcode</span><span class="sxs-lookup"><span data-stu-id="18e60-132">Debug form code</span></span>

1. <span data-ttu-id="18e60-133">Klicken Sie im Code-Editor auf die graue Leiste links neben der Zeile:</span><span class="sxs-lookup"><span data-stu-id="18e60-133">In the code editor, click the grey bar to the left of the line:</span></span>
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="18e60-134">Ein roter Kreis wird angezeigt, und die Codezeile wird hervorgehoben, um darauf hinzuweisen, dass die Laufzeit an diesem Haltepunkt im Formularcode angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="18e60-134">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
2. <span data-ttu-id="18e60-135">Klicken Sie im Menü **Debuggen** auf **Debuggen starten** (oder drücken Sie F5).</span><span class="sxs-lookup"><span data-stu-id="18e60-135">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
3. <span data-ttu-id="18e60-136">Klicken Sie im\*\*\*\* Vorschaufenster von InfoPath auf die Schaltfläche **Alert**.</span><span class="sxs-lookup"><span data-stu-id="18e60-136">In the InfoPath **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="18e60-137">Der Fokus wechselt zum Code-Editor, und die Haltepunktlinie wird hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="18e60-137">The code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
4. <span data-ttu-id="18e60-138">Klicken Sie im Menü **Debuggen** auf **Prozedurschritt** (oder drücken Sie UMSCHALT+F8), um das schrittweise Durchlaufen des Codes fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="18e60-138">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
   <span data-ttu-id="18e60-139">Der Code der **Warnungs** Methode wird ausgeführt, und die "Hello World!"</span><span class="sxs-lookup"><span data-stu-id="18e60-139">The **Alert** method code is executed, and the "Hello World!"</span></span> <span data-ttu-id="18e60-140">Alert wird im InfoPath- **Vorschaufenster** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="18e60-140">alert is displayed in the InfoPath **Preview** window.</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="18e60-141">Abrufen des aktuellen Benutzernamens</span><span class="sxs-lookup"><span data-stu-id="18e60-141">Getting the Current User's Name</span></span>

<span data-ttu-id="18e60-p106">Mithilfe der .NET Framework-Klassen können Sie auf Funktionalität zugreifen, die in Skripts nicht ohne weiteres verfügbar war. In diesem Beispiel erfahren Sie, wie der Name des aktuellen Benutzers über die .NET Framework-Klassen abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="18e60-p106">By using the .NET Framework classes, you can get access to functionality that was not easily available in script. In this example, you will learn how use the .NET Framework classes to retrieve the name of the current user.</span></span>
  
### <a name="add-an-onload-event-handler"></a><span data-ttu-id="18e60-144">Hinzufügen eines OnLoad-Ereignishandlers</span><span class="sxs-lookup"><span data-stu-id="18e60-144">Add an OnLoad event handler</span></span>

1. <span data-ttu-id="18e60-145">Öffnen Sie das InfoPath-Projekt "HelloWorld", das Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="18e60-145">Open the InfoPath HelloWorld project that you created earlier.</span></span>
    
2. <span data-ttu-id="18e60-146">Klicken Sie auf der Registerkarte **Ansicht** auf **Felder anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="18e60-146">On the **View** tab, click **Show Fields**.</span></span>
    
3. <span data-ttu-id="18e60-147">Klicken Sie mit der rechten Maustaste auf den Knoten **myFields**, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="18e60-147">Right-click the **myFields** node, and then click **Add**.</span></span>
    
4. <span data-ttu-id="18e60-148">Geben Sie **employee** im Feld **Name** ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="18e60-148">In **Name**, type **employee**, then click **OK**.</span></span>
    
5. <span data-ttu-id="18e60-149">Ziehen Sie den Knoten **employee** in die Ansicht.</span><span class="sxs-lookup"><span data-stu-id="18e60-149">Drag the **employee** node into the view.</span></span> 
    
6. <span data-ttu-id="18e60-150">Klicken Sie auf der Registerkarte **Entwicklertools** auf **On Load-Ereignis**.</span><span class="sxs-lookup"><span data-stu-id="18e60-150">On the **Developer** tab, click **On Load Event**.</span></span>
    
   <span data-ttu-id="18e60-151">Dadurch wird ein Ereignishandler für das [Onlade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) -Ereignis erstellt, und der Fokus wechselt zum Code-Editor.</span><span class="sxs-lookup"><span data-stu-id="18e60-151">This will create an event handler for the [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) event, and focus moves to the code editor.</span></span> <span data-ttu-id="18e60-152">Der Code in diesem Ereignishandler wird bei jedem Laden des Formulars aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="18e60-152">The code in this event handler will be called each time the form is loaded.</span></span> <span data-ttu-id="18e60-153">Im nächsten Verfahren wird gezeigt, wie dem Ereignishandler Formularcode zum Abrufen des Benutzernamens hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="18e60-153">The next procedure shows how to add form code that retrieves the user's name to the event handler.</span></span> 
    
### <a name="add-form-code"></a><span data-ttu-id="18e60-154">Hinzufügen von Formularcode </span><span class="sxs-lookup"><span data-stu-id="18e60-154">Add form code</span></span>

1. <span data-ttu-id="18e60-155">Geben Sie im **OnLoad**-Ereignishandler den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="18e60-155">In the **OnLoad** event handler, type the following code:</span></span> 
    
   ```cs
    // Store an XML DOM node as a local variable.
    IXMLDOMNode nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    if(nodeEmployee != null)
    {
        if(nodeEmployee.text == "")
        {
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName;
        }
    }
   ```

   ```vb
    // Store an XML DOM node as a local variable.
    Dim nodeEmployee As IXMLDOMNode
    nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    If Not(nodeEmployee Is Nothing) Then
        If(nodeEmployee.text = "") Then
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName
        End If
    End If
   ```

2. <span data-ttu-id="18e60-156">Kompilieren Sie das Formular, und zeigen Sie eine Vorschau davon an.</span><span class="sxs-lookup"><span data-stu-id="18e60-156">Compile and preview the form.</span></span>
    
   <span data-ttu-id="18e60-157">Das Textfeld employee sollte jetzt mit Ihrem Benutzername aufgefüllt sein.</span><span class="sxs-lookup"><span data-stu-id="18e60-157">The employee text box should now be populated with your username.</span></span> 
    
<span data-ttu-id="18e60-158">Informationen zum Bereitstelleneiner Formularvorlage mit verwaltetem Code finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="18e60-158">For information about how to deploy a managed code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> <span data-ttu-id="18e60-159">Informationen zum InfoPath-Objektmodell und zu allgemeinen Programmieraufgaben in Formularvorlagen mit verwaltetem Code, die mit dem InfoPath 2003-kompatiblen Objektmodell arbeiten, finden Sie unter [Understanding the infopath 2003 Object Model](understanding-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="18e60-159">For information on the InfoPath object model and common programming tasks in managed code form templates that work with the InfoPath 2003-compatible object model, see [Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="18e60-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18e60-160">See also</span></span>

- [<span data-ttu-id="18e60-161">Initialisierungs- und Bereinigungscode mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="18e60-161">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [<span data-ttu-id="18e60-162">InfoPath 2003-kompatible Objektmodelle</span><span class="sxs-lookup"><span data-stu-id="18e60-162">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
- [<span data-ttu-id="18e60-163">Hinzufügen eines Ereignishandlers mit dem InfoPath-Objektmodell 2003</span><span class="sxs-lookup"><span data-stu-id="18e60-163">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

