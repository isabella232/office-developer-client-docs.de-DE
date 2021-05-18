---
title: 'Exemplarische Vorgehensweise: Erstellen und Debuggen einer einfachen Formularvorlage mithilfe des InfoPath-Objektmodells'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- Formularvorlagen [infopath 2007], exemplarische Vorgehensweisen,Formularvorlagen [InfoPath 2007], Erstellen von InfoPath 2003-kompatiblen,InfoPath 2003-kompatiblen Formularvorlagen, exemplarische Vorgehensweisen
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: Dieses Thema enthält eine exemplarische Vorgehensweise zum Erstellen einer grundlegenden Formularvorlage für verwalteten InfoPath-Code, die mit dem infoPath 2003-kompatiblen Objektmodell von Microsoft funktioniert. Office.Interop.InfoPath.SemiTrust-Namespace.
ms.openlocfilehash: c559aedad5c62134c796196c63c1a84f70c4dc3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414340"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a><span data-ttu-id="e13f3-104">Exemplarische Vorgehensweise: Erstellen und Debuggen einer einfachen Formularvorlage mithilfe des InfoPath-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="e13f3-104">Walkthrough: Create and debug a basic form template using the InfoPath object model</span></span>

<span data-ttu-id="e13f3-105">In diesem Thema wird eine exemplarische Vorgehensweise zum Erstellen einer einfachen Formularvorlage für verwalteten InfoPath-Code bereitgestellt, die mit dem InfoPath 2003-kompatiblen Objektmodell arbeitet, das vom [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e13f3-105">This topic provides a walkthrough of creating a basic InfoPath managed code form template that works with the InfoPath 2003-compatible object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
## <a name="hello-world"></a><span data-ttu-id="e13f3-106">Hello World</span><span class="sxs-lookup"><span data-stu-id="e13f3-106">Hello World</span></span>

<span data-ttu-id="e13f3-107">Im folgenden Beispiel erfahren Sie, wie Sie mithilfe der [Alert-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) des InfoPath 2003-kompatiblen Objektmodells ein einfaches Warnungsdialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e13f3-107">In the following example, you will learn how to display a simple alert dialog box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the InfoPath 2003-compatible object model.</span></span> 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a><span data-ttu-id="e13f3-108">Erstellen einer neuen InfoPath-Formularvorlage, die das InfoPath 2003-kompatible Objektmodell verwendet</span><span class="sxs-lookup"><span data-stu-id="e13f3-108">Create a new InfoPath form template that works with the InfoPath 2003-compatible object model</span></span>

1. <span data-ttu-id="e13f3-109">Erstellen Sie eine neue Formularvorlage, die mit dem InfoPath 2003-kompatiblen Objektmodell funktioniert, wie unter [Create a Form Template Using the InfoPath 2003 Object Model beschrieben.](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)</span><span class="sxs-lookup"><span data-stu-id="e13f3-109">Create a new form template that works with the InfoPath 2003-compatible object model, as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).</span></span>
    
2. <span data-ttu-id="e13f3-110">Geben Sie dem Formularvorlagenprojekt den Namen HelloWorld, und speichern Sie es.</span><span class="sxs-lookup"><span data-stu-id="e13f3-110">Name the form template project HelloWorld and save it.</span></span> 
    
   <span data-ttu-id="e13f3-p101">Das Projektsystem erstellt Code- und Projektdateien und öffnet dann eine leere Formularvorlage im InfoPath-Entwurfsmodus. Jetzt können Sie Ereignishandler hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e13f3-p101">The project system creates code and project files, and then opens a blank form template in InfoPath design mode. You are now ready to add event handlers.</span></span>
    
### <a name="add-a-button-with-an-onclick-event-handler"></a><span data-ttu-id="e13f3-113">Hinzufügen einer Schaltfläche mit einem OnClick-Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="e13f3-113">Add a button with an OnClick event handler</span></span>

1. <span data-ttu-id="e13f3-114">Klicken Sie auf der Registerkarte **Start** im Abschnitt **Steuerelemente** auf das Steuerelement **Schaltfläche**, um dieses in die Ansicht einzufügen.</span><span class="sxs-lookup"><span data-stu-id="e13f3-114">In the **Controls** section on the **Home** tab, click the **Button** control to insert it into the view.</span></span> 
    
2. <span data-ttu-id="e13f3-115">Klicken Sie mit der rechten Maustaste auf das Steuerelement, und klicken Sie dann auf **Schaltflächeneigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="e13f3-115">Right-click the control, and then click **Button Properties**.</span></span>
    
3. <span data-ttu-id="e13f3-116">Ändern Sie **die Bezeichnung** in Warnung.</span><span class="sxs-lookup"><span data-stu-id="e13f3-116">Change the **Label** to Alert.</span></span>
    
4. <span data-ttu-id="e13f3-117">Ändern Sie die **ID** in AlertID.</span><span class="sxs-lookup"><span data-stu-id="e13f3-117">Change the **ID** to AlertID.</span></span>
    
5. <span data-ttu-id="e13f3-118">Klicken Sie auf **Formularcode bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="e13f3-118">Click **Edit Form Code**.</span></span>
    
   <span data-ttu-id="e13f3-119">Ein Ereignishandlergerüst für das [OnClick-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) wird erstellt, und der Fokus wird in Visual Studio 2012 in den Code-Editor verlagert.</span><span class="sxs-lookup"><span data-stu-id="e13f3-119">An event handler skeleton for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event is created and the focus moves to the code editor in Visual Studio 2012.</span></span> <span data-ttu-id="e13f3-120">Weitere Informationen zum Arbeiten mit Ereignishandlern finden Sie unter [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="e13f3-120">For more information on working with event handlers, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span> 
    
   <span data-ttu-id="e13f3-121">Jetzt können Sie dem Ereignishandler für die Schaltfläche Formularcode hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e13f3-121">You are now ready to add form code to the event handler for the button.</span></span>
    
### <a name="add-form-code-to-the-event-handler"></a><span data-ttu-id="e13f3-122">Hinzufügen von Formularcode zum Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="e13f3-122">Add form code to the event handler</span></span>

1. <span data-ttu-id="e13f3-123">Geben Sie im **OnClick**-Ereignishandler den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="e13f3-123">In the **OnClick** event handler, type the following code:</span></span> 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="e13f3-p103">Beachten Sie, dass nach der Eingabe jedes Punktes in der Codezeile eine Microsoft IntelliSense-Dropdownliste angezeigt wird. Der gesamte Ereignishandler sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="e13f3-p103">Note that a Microsoft IntelliSense drop-down list is displayed after you type each period in the line of code. The entire event handler should look like the following:</span></span>
    
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
   > <span data-ttu-id="e13f3-126">Alternativ zur Verwendung der **Alert**-Methode können Sie die **MessageBox.Show**-Methode des **System.Windows.Forms**-Namespace verwenden, um ein Meldungsfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e13f3-126">As an alternative to using the **Alert** method, you can use the **MessageBox.Show** method of the **System.Windows.Forms** namespace to display a message box.</span></span> <span data-ttu-id="e13f3-127">Dazu müssen Sie einen Verweis auf das System hinzufügen. Windows. Formular assembly, hinzufügen oder zu den Direktiven am Anfang der Codedatei, und geben Sie dann eine Codezeile wie `using System.Windows.Forms;` `Imports System.Windows.Forms` die folgende ein:`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span><span class="sxs-lookup"><span data-stu-id="e13f3-127">To do so, you must add a reference to the System.Windows.Forms assembly, add  `using System.Windows.Forms;` or  `Imports System.Windows.Forms` to the directives at the beginning of your code file, and then type a line of code such as the following:  `MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span></span>
  
2. <span data-ttu-id="e13f3-128">Wechseln Sie zum InfoPath-Entwurfsmodusfenster, und klicken Sie dann auf der Registerkarte **Start** auf die Schaltfläche **Vorschau**.</span><span class="sxs-lookup"><span data-stu-id="e13f3-128">Switch to the InfoPath design mode window, and then click the **Preview** button on the **Home** tab.</span></span> 
    
3. <span data-ttu-id="e13f3-129">Klicken Sie imVorschaufenster auf die Schaltfläche **Alert**.</span><span class="sxs-lookup"><span data-stu-id="e13f3-129">In the **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="e13f3-130">Ein Meldungsfeld mit dem Text "Hello World!" wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e13f3-130">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="e13f3-131">Im nächsten Verfahren wird gezeigt, wie Sie dem Formularcode Haltepunkte für das Debuggen hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="e13f3-131">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="e13f3-132">Debuggen von Formularcode</span><span class="sxs-lookup"><span data-stu-id="e13f3-132">Debug form code</span></span>

1. <span data-ttu-id="e13f3-133">Klicken Sie im Code-Editor auf die graue Leiste links neben der Zeile:</span><span class="sxs-lookup"><span data-stu-id="e13f3-133">In the code editor, click the grey bar to the left of the line:</span></span>
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="e13f3-134">Ein roter Kreis wird angezeigt, und die Codezeile wird hervorgehoben, um darauf hinzuweisen, dass die Laufzeit an diesem Haltepunkt im Formularcode angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="e13f3-134">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
2. <span data-ttu-id="e13f3-135">Klicken Sie im Menü **Debuggen** auf **Debuggen starten** (oder drücken Sie F5).</span><span class="sxs-lookup"><span data-stu-id="e13f3-135">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
3. <span data-ttu-id="e13f3-136">Klicken Sie imVorschaufenster von InfoPath auf die Schaltfläche **Alert**.</span><span class="sxs-lookup"><span data-stu-id="e13f3-136">In the InfoPath **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="e13f3-137">Der Fokus wechselt zum Code-Editor, und die Haltepunktlinie wird hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="e13f3-137">The code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
4. <span data-ttu-id="e13f3-138">Klicken Sie im Menü **Debuggen** auf **Prozedurschritt** (oder drücken Sie UMSCHALT+F8), um das schrittweise Durchlaufen des Codes fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="e13f3-138">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
   <span data-ttu-id="e13f3-139">Der Code der **Alert-Methode** wird ausgeführt, und die "Hello World!"</span><span class="sxs-lookup"><span data-stu-id="e13f3-139">The **Alert** method code is executed, and the "Hello World!"</span></span> <span data-ttu-id="e13f3-140">warnung wird im InfoPath **Preview-Fenster** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e13f3-140">alert is displayed in the InfoPath **Preview** window.</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="e13f3-141">Abrufen des aktuellen Benutzernamens</span><span class="sxs-lookup"><span data-stu-id="e13f3-141">Getting the Current User's Name</span></span>

<span data-ttu-id="e13f3-p106">Mithilfe der .NET Framework-Klassen können Sie auf Funktionalität zugreifen, die in Skripts nicht ohne weiteres verfügbar war. In diesem Beispiel erfahren Sie, wie der Name des aktuellen Benutzers über die .NET Framework-Klassen abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e13f3-p106">By using the .NET Framework classes, you can get access to functionality that was not easily available in script. In this example, you will learn how use the .NET Framework classes to retrieve the name of the current user.</span></span>
  
### <a name="add-an-onload-event-handler"></a><span data-ttu-id="e13f3-144">Hinzufügen eines OnLoad-Ereignishandlers</span><span class="sxs-lookup"><span data-stu-id="e13f3-144">Add an OnLoad event handler</span></span>

1. <span data-ttu-id="e13f3-145">Öffnen Sie das InfoPath-Projekt "HelloWorld", das Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="e13f3-145">Open the InfoPath HelloWorld project that you created earlier.</span></span>
    
2. <span data-ttu-id="e13f3-146">Klicken Sie auf der Registerkarte **Ansicht** auf **Felder anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="e13f3-146">On the **View** tab, click **Show Fields**.</span></span>
    
3. <span data-ttu-id="e13f3-147">Klicken Sie mit der rechten Maustaste auf den Knoten **myFields**, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="e13f3-147">Right-click the **myFields** node, and then click **Add**.</span></span>
    
4. <span data-ttu-id="e13f3-148">Geben Sie **employee** im Feld **Name** ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e13f3-148">In **Name**, type **employee**, then click **OK**.</span></span>
    
5. <span data-ttu-id="e13f3-149">Ziehen Sie den Knoten **employee** in die Ansicht.</span><span class="sxs-lookup"><span data-stu-id="e13f3-149">Drag the **employee** node into the view.</span></span> 
    
6. <span data-ttu-id="e13f3-150">Klicken Sie auf der Registerkarte **Entwicklertools** auf **On Load-Ereignis**.</span><span class="sxs-lookup"><span data-stu-id="e13f3-150">On the **Developer** tab, click **On Load Event**.</span></span>
    
   <span data-ttu-id="e13f3-151">Dadurch wird ein Ereignishandler für das [OnLoad-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) erstellt, und der Fokus wird in den Code-Editor verlagert.</span><span class="sxs-lookup"><span data-stu-id="e13f3-151">This will create an event handler for the [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) event, and focus moves to the code editor.</span></span> <span data-ttu-id="e13f3-152">Der Code in diesem Ereignishandler wird bei jedem Laden des Formulars aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e13f3-152">The code in this event handler will be called each time the form is loaded.</span></span> <span data-ttu-id="e13f3-153">Im nächsten Verfahren wird gezeigt, wie dem Ereignishandler Formularcode zum Abrufen des Benutzernamens hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e13f3-153">The next procedure shows how to add form code that retrieves the user's name to the event handler.</span></span> 
    
### <a name="add-form-code"></a><span data-ttu-id="e13f3-154">Hinzufügen von Formularcode </span><span class="sxs-lookup"><span data-stu-id="e13f3-154">Add form code</span></span>

1. <span data-ttu-id="e13f3-155">Geben Sie im **OnLoad**-Ereignishandler den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="e13f3-155">In the **OnLoad** event handler, type the following code:</span></span> 
    
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

2. <span data-ttu-id="e13f3-156">Kompilieren Sie das Formular, und zeigen Sie eine Vorschau davon an.</span><span class="sxs-lookup"><span data-stu-id="e13f3-156">Compile and preview the form.</span></span>
    
   <span data-ttu-id="e13f3-157">Das Textfeld employee sollte jetzt mit Ihrem Benutzername aufgefüllt sein.</span><span class="sxs-lookup"><span data-stu-id="e13f3-157">The employee text box should now be populated with your username.</span></span> 
    
<span data-ttu-id="e13f3-158">Informationen zum Bereitstellen einer Formularvorlage für verwalteten Code finden Sie unter [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="e13f3-158">For information about how to deploy a managed code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> <span data-ttu-id="e13f3-159">Informationen zum InfoPath-Objektmodell und zu allgemeinen Programmieraufgaben in Formularvorlagen für verwalteten Code, die mit dem InfoPath 2003-kompatiblen Objektmodell funktionieren, finden Sie unter [Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="e13f3-159">For information on the InfoPath object model and common programming tasks in managed code form templates that work with the InfoPath 2003-compatible object model, see [Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e13f3-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e13f3-160">See also</span></span>

- [<span data-ttu-id="e13f3-161">Initialisierungs- und Bereinigungscode mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="e13f3-161">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [<span data-ttu-id="e13f3-162">InfoPath 2003-kompatible Objektmodelle</span><span class="sxs-lookup"><span data-stu-id="e13f3-162">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
- [<span data-ttu-id="e13f3-163">Hinzufügen eines Ereignishandlers mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="e13f3-163">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

