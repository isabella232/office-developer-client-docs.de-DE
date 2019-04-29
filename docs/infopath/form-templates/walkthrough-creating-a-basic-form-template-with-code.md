---
title: 'Exemplarische vorGehensWeise: Erstellen einer einfachen Formularvorlage mit Code'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- Formularvorlagen [InfoPath 2007], Erstellen von verwaltetem Code, Formularvorlagen für verwalteten Code [InfoPath 2007], erstellen, Formularvorlagen [InfoPath 2007], Exemplarische Vorgehensweisen, InfoPath 2007, Exemplarische Vorgehensweisen
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: In Microsoft InfoPath können Sie Geschäftslogik in Visual Basic oder C# schreiben, indem Sie eine Formularvorlage im InfoPath-Designer öffnen und dann einen der Benutzeroberflächenbefehle verwenden, um einen Ereignishandler hinzuzufügen, der die Entwicklungsumgebung von Visual Studio 2012 öffnet. Schreiben des Codes.
ms.openlocfilehash: cc09856750ced28d35c8da172a08a31c4e3cd4a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420647"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a><span data-ttu-id="1a70a-104">Exemplarische vorGehensWeise: Erstellen einer einfachen Formularvorlage mit Code</span><span class="sxs-lookup"><span data-stu-id="1a70a-104">Walkthrough: Create a basic form template with code</span></span>

<span data-ttu-id="1a70a-105">In Microsoft InfoPath können Sie Geschäftslogik in Visual Basic oder C# schreiben, indem Sie eine Formularvorlage im InfoPath-Designer öffnen und dann einen der Benutzeroberflächenbefehle verwenden, um einen Ereignishandler hinzuzufügen, der die Entwicklungsumgebung von Visual Studio 2012 öffnet. Schreiben des Codes.</span><span class="sxs-lookup"><span data-stu-id="1a70a-105">In Microsoft InfoPath, you can write business logic in Visual Basic or C# by opening a form template in the InfoPath designer, and then using one of the user interface commands to add an event handler, which will open the Visual Studio 2012 development environment for writing your code.</span></span> <span data-ttu-id="1a70a-106">Standardmäßig arbeiten Formularvorlagenprojekte, die mit Visual Studio 2012 erstellt wurden, mit dem vom [Microsoft. Office. InfoPath-](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) Namespace bereitgestellten Objektmodell mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="1a70a-106">By default, form template projects created using Visual Studio 2012 work against the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
<span data-ttu-id="1a70a-107">In dieser exemplarischen Vorgehensweise wird zunächst gezeigt, wie Sie eine einfache Hello World-Anwendung mit C# oder Visual Basic in der Visual Studio 2012-Entwicklungsumgebung erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a70a-107">This walkthrough first shows you how to create a simple Hello World application using C# or Visual Basic in the Visual Studio 2012 development environment.</span></span> <span data-ttu-id="1a70a-108">Die exemplarische Vorgehensweise endet mit einem Codebeispiel, in dem gezeigt wird, wie die [username](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) -Eigenschaft der [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) -Klasse verwendet wird, um den Namen des aktuellen Benutzers abzurufen und ein **Textfeld** -Steuerelement mit diesem Wert aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="1a70a-108">The walkthrough concludes with a code sample that shows you how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the current user's name and populate a **Text Box** control with that value.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="1a70a-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1a70a-109">Prerequisites</span></span>

<span data-ttu-id="1a70a-110">Zum Ausführen dieser exemplarischen Vorgehensweise mithilfe der Visual Studio 2012-Entwicklungsumgebung benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1a70a-110">In order to complete this walkthrough using the Visual Studio 2012 development environment, you will need:</span></span>
  
- <span data-ttu-id="1a70a-111">Microsoft InfoPath mit Visual Studio 2012 installiert.</span><span class="sxs-lookup"><span data-stu-id="1a70a-111">Microsoft InfoPath with Visual Studio 2012 installed.</span></span>
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a><span data-ttu-id="1a70a-112">Hello World in Visual Studio-Tools für Anwendungen</span><span class="sxs-lookup"><span data-stu-id="1a70a-112">Hello World in Visual Studio Tools for Applications</span></span>

<span data-ttu-id="1a70a-113">In der folgenden exemplarischen Vorgehensweise erfahren Sie, wie Sie in der Visual Studio 2012-Entwicklungsumgebung Code schreiben, um ein einfaches Warnungsdialogfeld anzuzeigen, indem [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) Sie einen Ereignishandler für das Clicked-Ereignis der [Button Event](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) -Klasse schreiben, das zugeordnet ist mit dem **Schaltflächen** -Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="1a70a-113">In the following walkthrough, you will learn how to write code in the Visual Studio 2012 development environment to display a simple alert dialog box by writing an event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of the [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) class, which is associated with the **Button** control.</span></span> 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a><span data-ttu-id="1a70a-114">Erstellen eines neuen Projekts und Angeben der Programmiersprache</span><span class="sxs-lookup"><span data-stu-id="1a70a-114">Create a new project and specify the programming language</span></span>

1. <span data-ttu-id="1a70a-115">Starten Sie den InfoPath-Designer, und doppelklicken Sie auf die Formularvorlage **Leer (InfoPath Editor)**.</span><span class="sxs-lookup"><span data-stu-id="1a70a-115">Start the InfoPath designer, and then double-click the **Blank (InfoPath Editor)** form template.</span></span> 
    
2. <span data-ttu-id="1a70a-116">Um anzugeben, welche Programmiersprache verwendet werden soll, klicken Sie auf die **Office-Schaltfläche**, klicken Sie auf **Formularoptionen**, klicken Sie in der Liste **Kategorie** auf **Programmierung** , und wählen Sie dann in der Formularvorlage entweder **Visual Basic** oder **C#** aus. \*\* Dropdownliste Codesprache\*\* .</span><span class="sxs-lookup"><span data-stu-id="1a70a-116">To specify which programming language to use, click the **Office Button**, click **Form Options**, click **Programming** in the **Category** list, and then select either **Visual Basic** or **C#** from the **Form template code language** drop-down list.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="1a70a-117">Die anderen Optionen für die Programmiersprache in der Dropdownliste **Codesprache der Formularvorlage** dienen der Kompatibilität mit früheren Versionen von InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1a70a-117">The other programming language options in the **Form template code language** drop-down list provide compatibility with previous versions of InfoPath.</span></span> <span data-ttu-id="1a70a-118">Die Optionen **C# (InfoPath 2007-kompatibel)** und **Visual Basic (InfoPath 2007-kompatibel)** können Sie für die Vorgehensweisen in diesem Thema verwenden.</span><span class="sxs-lookup"><span data-stu-id="1a70a-118">The **C# (InfoPath 2007 Compatible)** and **Visual Basic (InfoPath 2007 Compatible)** options will work with the procedures in this topic.</span></span> <span data-ttu-id="1a70a-119">Wenn Sie die Optionen **C# (InfoPath 2003-kompatibel)** und **Visual Basic (InfoPath 2003-kompatibel)** verwenden möchten, lesen Sie bitte die Informationen unter [Exemplarische Vorgehensweise: Erstellen und Debuggen einer einfachen Formularvorlage mit dem InfoPath 2003-Objektmodell](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="1a70a-119">However, to use the **C# (InfoPath 2003 Compatible)** and **Visual Basic (InfoPath 2003 Compatible)** options, see [Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md).</span></span> 
  
    <span data-ttu-id="1a70a-120">Jetzt können Sie ein Steuerelement vom Typ **Schaltfläche** hinzufügen und dessen Ereignishandler erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a70a-120">You are now ready to add a **Button** control and create its event handler.</span></span> 
    
### <a name="add-a-button-control-and-event-handler"></a><span data-ttu-id="1a70a-121">Hinzufügen eines Steuerelements vom Typ "Schaltfläche" und eines Ereignishandlers</span><span class="sxs-lookup"><span data-stu-id="1a70a-121">Add a Button control and event handler</span></span>

1. <span data-ttu-id="1a70a-122">Klicken Sie in der Gruppe **Steuerelemente** auf das Steuerelement **Schaltfläche**, um dieses dem Formular hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1a70a-122">In the **Controls** group, click the **Button** control to add it the form.</span></span> 
    
2. <span data-ttu-id="1a70a-123">Doppelklicken Sie auf das Steuerelement **Schaltfläche**, geben Sie auf der Registerkarte Eigenschaften des Menübands den Text **Hallo** für die Eigenschaft **Etikett** ein, und klicken Sie dann auf **Benutzerdefinierter Code**.</span><span class="sxs-lookup"><span data-stu-id="1a70a-123">Double-click the **Button** control, type Hello for the **Label** property on the **Properties** tab of the ribbon, and then click **Custom Code**.</span></span> <span data-ttu-id="1a70a-124">Speichern Sie das Formular bei entsprechender Aufforderung, und nennen Sie es HelloWorld.</span><span class="sxs-lookup"><span data-stu-id="1a70a-124">When prompted, save the form and name it HelloWorld.</span></span>
    
   <span data-ttu-id="1a70a-125">Dadurch wird die **Visual Studio Tools for Applications** -Umgebung mit dem Cursor im Ereignishandler für das [clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) -Ereignis des **Schaltflächen** -Steuerelements geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1a70a-125">This will open the **Visual Studio Tools for Applications** environment with the cursor in the event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of **Button** control.</span></span> 
    
   <span data-ttu-id="1a70a-126">Jetzt können Sie dem Ereignishandler für die Schaltfläche Formularcode hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1a70a-126">You are now ready to add form code to the event handler for the button.</span></span> 
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a><span data-ttu-id="1a70a-127">Hinzufügen von Code für "Hello World" zum Ereignishandler und Anzeigen einer Vorschau für das Formular</span><span class="sxs-lookup"><span data-stu-id="1a70a-127">Add "Hello World" code to the event handler and preview the form</span></span>

1. <span data-ttu-id="1a70a-128">Geben Sie in die Ereignishandlervorlage Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="1a70a-128">In the event handler skeleton, type:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="1a70a-129">Der Code für die Formularvorlage sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="1a70a-129">The code for your form template should look similar to the following:</span></span>
    
   ```cs
    using Microsoft.Office.InfoPath;
    using System;
    using System.Windows.Forms;
    using System.Xml;
    using System.Xml.XPath;
    namespace HelloWorld
    {
        public partial class FormCode
        {
            public void InternalStartup()
            {
            ((ButtonEvent)EventManager.ControlEvents["CTRL1_5"]).Clicked += new ClickedEventHandler(CTRL1_5_Clicked);
            }
            public void CTRL1_5_Clicked(object sender, ClickedEventArgs e)
            {
            MessageBox.Show("Hello World!");
            }
        }
    }
   ```

   ```vb
    Imports Microsoft.Office.InfoPath
    Imports System
    Imports System.Windows.Forms
    Imports System.Xml
    Imports System.Xml.XPath
    Namespace HelloWorld
        Public Class FormCode
            Private Sub InternalStartup(ByVal sender As Object, ByVal e As EventArgs) Handles Me.Startup
            AddHandler DirectCast(EventManager.ControlEvents("CTRL1_5"), ButtonEvent).Clicked, AddressOf CTRL1_5_Clicked
            End Sub
            Public Sub CTRL1_5_Clicked(ByVal sender As Object, ByVal e As ClickedEventArgs)
            MessageBox.Show("Hello World!")
            End Sub
        End Class
    End Namespace
   ```

2. <span data-ttu-id="1a70a-130">Wechseln Sie zum InfoPath-Designer-Fenster.</span><span class="sxs-lookup"><span data-stu-id="1a70a-130">Switch to the InfoPath designer window.</span></span>
    
3. <span data-ttu-id="1a70a-131">Klicken Sie auf der Registerkarte **Start** auf die Schaltfläche **Vorschau**.</span><span class="sxs-lookup"><span data-stu-id="1a70a-131">Click the **Preview** button on the **Home** tab.</span></span> 
    
4. <span data-ttu-id="1a70a-132">Klicken Sie auf dem Formular auf die Schaltfläche Hallo.</span><span class="sxs-lookup"><span data-stu-id="1a70a-132">Click the Hello button on the form.</span></span> 
    
   <span data-ttu-id="1a70a-133">Ein Meldungsfeld mit dem Text "Hello World!" wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1a70a-133">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="1a70a-134">Im nächsten Verfahren wird gezeigt, wie Sie dem Formularcode Haltepunkte für das Debuggen hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="1a70a-134">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="1a70a-135">Debuggen von Formularcode</span><span class="sxs-lookup"><span data-stu-id="1a70a-135">Debug form code</span></span>

1. <span data-ttu-id="1a70a-136">Wechseln Sie zurück zum Fenster von Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="1a70a-136">Switch back to the Visual Studio 2012 window.</span></span>
    
2. <span data-ttu-id="1a70a-137">Klicken Sie auf die graue Leiste links der Zeile:</span><span class="sxs-lookup"><span data-stu-id="1a70a-137">Click the grey bar to the left of the line:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="1a70a-138">Ein roter Kreis wird angezeigt, und die Codezeile wird hervorgehoben, um darauf hinzuweisen, dass die Laufzeit an diesem Haltepunkt im Formularcode angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="1a70a-138">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="1a70a-139">Klicken Sie im Menü **Debuggen** auf **Debuggen starten** (oder drücken Sie F5).</span><span class="sxs-lookup"><span data-stu-id="1a70a-139">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
4. <span data-ttu-id="1a70a-140">Klicken Sie im Fenster **Vorschau** von InfoPath auf die Schaltfläche Hallo auf dem Formular. </span><span class="sxs-lookup"><span data-stu-id="1a70a-140">In the InfoPath **Preview** window, click the Hello button on the form.</span></span> 
    
5. <span data-ttu-id="1a70a-141">Der Code-Editor von Visual Studio 2012 erhält den Fokus, und die Haltepunkt Linie wird hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="1a70a-141">The Visual Studio 2012 code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
6. <span data-ttu-id="1a70a-142">Klicken Sie im Menü **Debuggen** auf **Prozedurschritt** (oder drücken Sie UMSCHALT+F8), um das schrittweise Durchlaufen des Codes fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="1a70a-142">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
7. <span data-ttu-id="1a70a-p105">Der Ereignishandlercode wird ausgeführt, und die Meldung "Hello World!" wird angezeigt. </span><span class="sxs-lookup"><span data-stu-id="1a70a-p105">The event handler code is executed, and the "Hello World!" message is displayed.</span></span> 
    
8. <span data-ttu-id="1a70a-145">Klicken Sie auf **OK** , um zum Code-Editor von Visual Studio 2012 zurückzukehren, und klicken Sie dann im Menü **Debuggen** auf **Debuggen beenden** (oder drücken Sie STRG + ALT + Unterbrechung).</span><span class="sxs-lookup"><span data-stu-id="1a70a-145">Click **OK** to return to the Visual Studio 2012 code editor, and then click **Stop Debugging** on the **Debug** menu (or press Ctrl+Alt+Break).</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="1a70a-146">Aufrufen des aktuellen Benutzernamens</span><span class="sxs-lookup"><span data-stu-id="1a70a-146">Getting the current user's name</span></span>

<span data-ttu-id="1a70a-147">Im folgenden Beispiel erfahren Sie, wie Sie die [username](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) -Eigenschaft der [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) -Klasse verwenden, um den Namen des aktuellen Benutzers abzurufen und den Wert eines **Textfeld** -Steuerelements mithilfe eines Ereignishandlers für das [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignis aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="1a70a-147">In the following example, you will learn how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the name of the current user and populate the value of a **Text Box** control by using an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
<span data-ttu-id="1a70a-148">Das aufFüllen des **Textfeld** -Steuerelements erfolgt mithilfe einer Instanz der [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) -Klasse, um den Namen des aktuellen Benutzers in den XML-Knoten zu schreiben, an den das Steuerelement gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="1a70a-148">Populating the **Text Box** control is accomplished by using an instance of the [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) class to write the current user's name to the XML node that the control is bound to.</span></span> 
  
<span data-ttu-id="1a70a-149">Zuerst wird die [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) -Eigenschaft der [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) XmlForm-Klasse aufgerufen, um eine Instanz der [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Klasse abzurufen, die das zugrunde liegende XML-Dokument des Formulars darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a70a-149">First, the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class is called to retrieve an instance of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class that represents the underlying XML document of the form.</span></span> <span data-ttu-id="1a70a-150">Das [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Objekt ruft dann [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) die CreateNavigator-Methode auf, die das **XPathNavigator** -Objekt erstellt und am Stammknoten der Hauptdatenquelle des Formulars positioniert.</span><span class="sxs-lookup"><span data-stu-id="1a70a-150">The [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) object then calls the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method, which creates the **XPathNavigator** object and positions it at the root node of the form's main data source.</span></span> 
  
<span data-ttu-id="1a70a-151">Die [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) -Methode der **XPathNavigator** -Klasse wird aufgerufen, um das Feld Employee in der Datenquelle des Formulars auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1a70a-151">The [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) method of the **XPathNavigator** class is called to select the employee field in the form's data source.</span></span> <span data-ttu-id="1a70a-152">Schließlich wird die [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) -Methode aufgerufen, um den Wert des Felds mit der [username](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) -Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1a70a-152">Finally, the [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) method is called to set the value of the field with the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property.</span></span> 
  
<span data-ttu-id="1a70a-153">Weitere Informationen zum Arbeiten mit " **System. XML** " in Formularvorlagen mit verwaltetem Code finden Sie unter [Arbeiten mit den Klassen "XPathNavigator" und "XPathNodeIterator"](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).</span><span class="sxs-lookup"><span data-stu-id="1a70a-153">For more information on working with **System.Xml** in managed code form templates, see [Work with the XPathNavigator and XPathNodeIterator Classes](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).</span></span>
  
### <a name="add-a-loading-event-handler"></a><span data-ttu-id="1a70a-154">Hinzufügen eines Loading-Ereignishandlers</span><span class="sxs-lookup"><span data-stu-id="1a70a-154">Add a Loading event handler</span></span>

1. <span data-ttu-id="1a70a-155">Öffnen Sie die Formularvorlage "HelloWorld", die Sie in der vorherigen exemplarischen Vorgehensweise im InfoPath-Designer erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="1a70a-155">Open the HelloWorld form template that you created in the previous walkthrough in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="1a70a-156">Klicken Sie auf der Registerkarte **Ansicht** auf **Felder anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="1a70a-156">On the **View** tab, select **Show Fields**.</span></span>
    
3. <span data-ttu-id="1a70a-157">Klicken Sie mit der rechten Maustaste auf den Ordner **myFields**, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="1a70a-157">Right click the **myFields** folder, and then click **Add**.</span></span>
    
4. <span data-ttu-id="1a70a-158">Geben Sie unter **Name den Namen**Employee ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a70a-158">In **Name**, type employee, and then click **OK**.</span></span>
    
5. <span data-ttu-id="1a70a-159">Ziehen Sie das Feld employee in die Ansicht.</span><span class="sxs-lookup"><span data-stu-id="1a70a-159">Drag the employee field onto the view.</span></span> 
    
6. <span data-ttu-id="1a70a-160">Klicken Sie auf der Registerkarte **Entwickler** auf **Loading-Ereignis**.</span><span class="sxs-lookup"><span data-stu-id="1a70a-160">On the **Developer** tab, click **Loading Event**.</span></span>
    
   <span data-ttu-id="1a70a-161">Dadurch wird ein Ereignishandler für das [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignis erstellt, und der Fokus wird auf diesen Ereignishandler im Code-Editor verschoben.</span><span class="sxs-lookup"><span data-stu-id="1a70a-161">This will create an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, and move the focus to that event handler in the code editor.</span></span> 
    
7. <span data-ttu-id="1a70a-162">Geben Sie im Code-Editor Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="1a70a-162">In the code editor, type the following:</span></span>
    
   ```cs
    public void FormEvents_Loading(object sender, LoadingEventArgs e)
    {
        XPathNavigator dataSource;
        dataSource = this.MainDataSource.CreateNavigator();
        dataSource.SelectSingleNode(
            "/my:myFields/my:employee", NamespaceManager).SetValue(this.User.UserName);
    }
   ```
 
   ```vb
    Public Sub FormEvents_Loading(ByVal sender As Object, ByVal e As LoadingEventArgs)
        Dim dataSource As XPathNavigator
        dataSource = Me.MainDataSource.CreateNavigator
        dataSource.SelectSingleNode( _
            "/my:myFields/my:employee", NamespaceManager).SetValue(Me.User.UserName)
    End Sub
   ```

8. <span data-ttu-id="1a70a-163">Wechseln Sie in das InfoPath-Formularentwurfsfenster, und klicken Sie auf der Registerkarte **Start** auf die Schaltfläche **Vorschau**, um eine Vorschau des Formulars anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1a70a-163">Switch to the InfoPath form design window, and then click the **Preview** button on the **Home** tab to preview the form.</span></span> 
    
   <span data-ttu-id="1a70a-164">Im Feld employee sollte automatisch Ihr Benutzername eingelesen werden.</span><span class="sxs-lookup"><span data-stu-id="1a70a-164">The employee field should automatically fill in with your user name.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="1a70a-165">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="1a70a-165">Next steps</span></span>

- <span data-ttu-id="1a70a-166">Informationen zum Arbeiten mit Ereignishandlern für andere Steuerelemente und Ereignisse finden Sie unter [Hinzufügen eines Ereignishandlers](how-to-add-an-event-handler.md).</span><span class="sxs-lookup"><span data-stu-id="1a70a-166">For information about working with event handlers for other controls and events, see [Add an Event Handler](how-to-add-an-event-handler.md).</span></span>
    
- <span data-ttu-id="1a70a-167">Weitere Informationen zum Anzeigen und Debuggen von Code in Formularvorlagen finden Sie unter [Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="1a70a-167">For more information about previewing and debugging code in form templates, see [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="1a70a-168">Informationen zum Bereitstelleneiner Formularvorlage mit verwaltetem Code finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="1a70a-168">For information about how to deploy a managed-code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="1a70a-169">Weitere Informationen zum InfoPath-Objektmodell sowie zu allgemeinen Programmieraufgaben in Formularvorlagen mit verwaltetem Code finden Sie unter [Grundlegendes zum InfoPath-Objektmodell und zu allgemeinen Entwickleraufgaben](understanding-the-infopath-object-model-and-common-developer-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="1a70a-169">For information about the InfoPath object model and common programming tasks in managed-code form templates, see [Understanding the InfoPath Object Model and Common Developer Tasks](understanding-the-infopath-object-model-and-common-developer-tasks.md)</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a70a-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a70a-170">See also</span></span>

- [<span data-ttu-id="1a70a-171">XmlForm</span><span class="sxs-lookup"><span data-stu-id="1a70a-171">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

