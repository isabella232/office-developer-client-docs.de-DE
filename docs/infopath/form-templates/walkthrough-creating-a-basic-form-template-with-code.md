---
title: 'Exemplarische Vorgehensweise: Erstellen einer einfachen Formularvorlage mit code'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- 'Formularvorlagen [Infopath 2007], Erstellen von verwaltetem Code, verwalteten code von Formularvorlagen [InfoPath 2007], erstellen, Formularvorlagen [InfoPath 2007], exemplarische Vorgehensweisen, die InfoPath 2007: Erste Schritte'
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: In Microsoft InfoPath können Sie Schreiben von Geschäftslogik in Visual Basic oder c# durch Öffnen einer Formularvorlage im InfoPath-Designer, und klicken Sie dann mit einer der den Befehlen der Benutzeroberfläche um einen Ereignishandler hinzuzufügen, der geöffnet wird, die Entwicklungsumgebung von Visual Studio 2012 für Schreiben des Codes.
ms.openlocfilehash: 8c98d71c26f8e56c532b2a4467218c366072b2ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790860"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a><span data-ttu-id="ff4ae-104">Exemplarische Vorgehensweise: Erstellen einer einfachen Formularvorlage mit code</span><span class="sxs-lookup"><span data-stu-id="ff4ae-104">Walkthrough: Create a basic form template with code</span></span>

<span data-ttu-id="ff4ae-105">In Microsoft InfoPath können Sie Schreiben von Geschäftslogik in Visual Basic oder c# durch Öffnen einer Formularvorlage im InfoPath-Designer, und klicken Sie dann mit einer der den Befehlen der Benutzeroberfläche um einen Ereignishandler hinzuzufügen, der geöffnet wird, die Entwicklungsumgebung von Visual Studio 2012 für Schreiben des Codes.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-105">In Microsoft InfoPath, you can write business logic in Visual Basic or C# by opening a form template in the InfoPath designer, and then using one of the user interface commands to add an event handler, which will open the Visual Studio 2012 development environment for writing your code.</span></span> <span data-ttu-id="ff4ae-106">Standardmäßig erstellt Formular Vorlagenprojekte mithilfe von Visual Studio 2012 funktionieren in Verbindung mit dem Objektmodell für verwalteten Code vom [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-106">By default, form template projects created using Visual Studio 2012 work against the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
<span data-ttu-id="ff4ae-107">Zuerst werden in dieser exemplarischen Vorgehensweise erstellen Sie eine einfache "Hello World"-Anwendung mit c# oder Visual Basic in der Entwicklungsumgebung von Visual Studio 2012 veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-107">This walkthrough first shows you how to create a simple Hello World application using C# or Visual Basic in the Visual Studio 2012 development environment.</span></span> <span data-ttu-id="ff4ae-108">Die exemplarische Vorgehensweise endet mit dem ein Codebeispiel, in dem Sie zeigt, wie die [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) -Eigenschaft der [Benutzer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) -Klasse verwenden, um den aktuellen Namen des Benutzers abrufen, und füllen Sie ein **Textfeld** -Steuerelement mit diesem Wert.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-108">The walkthrough concludes with a code sample that shows you how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the current user's name and populate a **Text Box** control with that value.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="ff4ae-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ff4ae-109">Prerequisites</span></span>

<span data-ttu-id="ff4ae-110">Für die Durchführung dieser exemplarischen Vorgehensweise mithilfe der Visual Studio 2012-Entwicklungsumgebung benötigen Sie:</span><span class="sxs-lookup"><span data-stu-id="ff4ae-110">In order to complete this walkthrough using the Visual Studio 2012 development environment, you will need:</span></span>
  
- <span data-ttu-id="ff4ae-111">Microsoft InfoPath mit Visual Studio 2012 installiert.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-111">Microsoft InfoPath with Visual Studio 2012 installed.</span></span>
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a><span data-ttu-id="ff4ae-112">Hello World in Visual Studio-Tools für Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ff4ae-112">Hello World in Visual Studio Tools for Applications</span></span>

<span data-ttu-id="ff4ae-113">In der folgenden exemplarischen Vorgehensweise erfahren Sie, wie das Schreiben von Code in der Entwicklungsumgebung von Visual Studio 2012 um ein einfaches Warnungsdialogfeld anzeigen, indem Sie einen Ereignishandler für das [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) -Ereignis der [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) -Klasse, die verbunden ist schreiben mit der **Schaltfläche** -Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-113">In the following walkthrough, you will learn how to write code in the Visual Studio 2012 development environment to display a simple alert dialog box by writing an event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of the [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) class, which is associated with the **Button** control.</span></span> 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a><span data-ttu-id="ff4ae-114">Erstellen eines neuen Projekts und Angeben der Programmiersprache</span><span class="sxs-lookup"><span data-stu-id="ff4ae-114">Create a new project and specify the programming language</span></span>

1. <span data-ttu-id="ff4ae-115">Starten Sie den InfoPath-Designer, und doppelklicken Sie dann auf die Formularvorlage **leer (InfoPath Editor)** .</span><span class="sxs-lookup"><span data-stu-id="ff4ae-115">Start the InfoPath designer, and then double-click the **Blank (InfoPath Editor)** form template.</span></span> 
    
2. <span data-ttu-id="ff4ae-116">Um anzugeben, welche Programmiersprache verwenden, klicken Sie auf die **Office-Schaltfläche**, klicken Sie auf **Formularoptionen**, klicken Sie in der Liste **Kategorie** auf **Programmierung** , und wählen Sie dann aus der Formularvorlage **aus **Visual Basic** oder **Visual c#** Sprache Code** Dropdown-Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-116">To specify which programming language to use, click the **Office Button**, click **Form Options**, click **Programming** in the **Category** list, and then select either **Visual Basic** or **C#** from the **Form template code language** drop-down list.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="ff4ae-117">Die anderen programming Language-Optionen in der Dropdownliste **Codesprache der Formularvorlage** bieten Kompatibilität mit früheren Versionen von InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-117">The other programming language options in the **Form template code language** drop-down list provide compatibility with previous versions of InfoPath.</span></span> <span data-ttu-id="ff4ae-118">Die Verfahren in diesem Thema werden die Optionen für **c# (kompatibel mit InfoPath 2007)** und **Visual Basic (kompatibel mit InfoPath 2007)** entwickelt.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-118">The **C# (InfoPath 2007 Compatible)** and **Visual Basic (InfoPath 2007 Compatible)** options will work with the procedures in this topic.</span></span> <span data-ttu-id="ff4ae-119">Um die Optionen für **c# (kompatibel mit InfoPath 2003)** und **Visual Basic (kompatibel mit InfoPath 2003)** verwenden, jedoch finden Sie unter [Exemplarische Vorgehensweise: Erstellen und Debuggen einer grundlegenden Formular Vorlage mithilfe des InfoPath 2003-Objektmodells](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="ff4ae-119">However, to use the **C# (InfoPath 2003 Compatible)** and **Visual Basic (InfoPath 2003 Compatible)** options, see [Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md).</span></span> 
  
    <span data-ttu-id="ff4ae-120">Sie sind jetzt bereit, die ein **Button** -Steuerelement hinzufügen und dessen Ereignishandler erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-120">You are now ready to add a **Button** control and create its event handler.</span></span> 
    
### <a name="add-a-button-control-and-event-handler"></a><span data-ttu-id="ff4ae-121">Hinzufügen eines Steuerelements vom Typ "Schaltfläche" und eines Ereignishandlers</span><span class="sxs-lookup"><span data-stu-id="ff4ae-121">Add a Button control and event handler</span></span>

1. <span data-ttu-id="ff4ae-122">Klicken Sie in der Gruppe **Steuerelemente** auf das **Schaltfläche** -Steuerelement, um dieses dem Formular hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-122">In the **Controls** group, click the **Button** control to add it the form.</span></span> 
    
2. <span data-ttu-id="ff4ae-123">Doppelklicken Sie auf das **Button** -Steuerelement, geben Sie Hello für die **Label** -Eigenschaft auf der Registerkarte **Eigenschaften** des Menübands, und klicken Sie dann auf **Benutzerdefinierter Code**.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-123">Double-click the **Button** control, type Hello for the **Label** property on the **Properties** tab of the ribbon, and then click **Custom Code**.</span></span> <span data-ttu-id="ff4ae-124">Wenn Sie aufgefordert werden, speichern Sie das Formular, und nennen Sie sie "HelloWorld".</span><span class="sxs-lookup"><span data-stu-id="ff4ae-124">When prompted, save the form and name it HelloWorld.</span></span>
    
   <span data-ttu-id="ff4ae-125">Dadurch wird die **Visual Studio Tools for Applications** -Umgebung mit dem Mauszeiger geöffnet, in der Ereignisprozedur Handler für das [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) -Ereignis der **Schaltfläche** steuern.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-125">This will open the **Visual Studio Tools for Applications** environment with the cursor in the event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of **Button** control.</span></span> 
    
   <span data-ttu-id="ff4ae-126">Jetzt können Sie dem Ereignishandler für die Schaltfläche Formularcode hinzufügen. </span><span class="sxs-lookup"><span data-stu-id="ff4ae-126">You are now ready to add form code to the event handler for the button.</span></span> 
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a><span data-ttu-id="ff4ae-127">Hinzufügen von Code für "Hello World" zum Ereignishandler und Anzeigen einer Vorschau für das Formular</span><span class="sxs-lookup"><span data-stu-id="ff4ae-127">Add "Hello World" code to the event handler and preview the form</span></span>

1. <span data-ttu-id="ff4ae-128">Geben Sie in die Ereignishandlervorlage Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="ff4ae-128">In the event handler skeleton, type:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="ff4ae-129">Der Code für die Formularvorlage sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="ff4ae-129">The code for your form template should look similar to the following:</span></span>
    
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

2. <span data-ttu-id="ff4ae-130">Wechseln Sie zum InfoPath-Designer-Fenster.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-130">Switch to the InfoPath designer window.</span></span>
    
3. <span data-ttu-id="ff4ae-131">Klicken Sie auf die Schaltfläche **Vorschau** auf der Registerkarte **Start** .</span><span class="sxs-lookup"><span data-stu-id="ff4ae-131">Click the **Preview** button on the **Home** tab.</span></span> 
    
4. <span data-ttu-id="ff4ae-132">Klicken Sie auf die Schaltfläche Hallo auf dem Formular.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-132">Click the Hello button on the form.</span></span> 
    
   <span data-ttu-id="ff4ae-133">Ein Meldungsfeld mit dem Text "Hello World!" wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-133">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="ff4ae-134">Im nächsten Verfahren wird gezeigt, wie Sie dem Formularcode Haltepunkte für das Debuggen hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-134">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="ff4ae-135">Debuggen von Formularcode</span><span class="sxs-lookup"><span data-stu-id="ff4ae-135">Debug form code</span></span>

1. <span data-ttu-id="ff4ae-136">Wechseln Sie in das Fenster des Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-136">Switch back to the Visual Studio 2012 window.</span></span>
    
2. <span data-ttu-id="ff4ae-137">Klicken Sie auf die graue Leiste links der Zeile:</span><span class="sxs-lookup"><span data-stu-id="ff4ae-137">Click the grey bar to the left of the line:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="ff4ae-138">Ein roter Kreis wird angezeigt, und die Codezeile wird hervorgehoben, um darauf hinzuweisen, dass die Laufzeit an diesem Haltepunkt im Formularcode angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-138">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="ff4ae-139">Klicken Sie im Menü **Debuggen** auf **Debuggen starten,** klicken Sie auf (oder drücken Sie F5).</span><span class="sxs-lookup"><span data-stu-id="ff4ae-139">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
4. <span data-ttu-id="ff4ae-140">Klicken Sie im InfoPath- **Vorschau** klicken Sie auf die Schaltfläche Hallo auf dem Formular.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-140">In the InfoPath **Preview** window, click the Hello button on the form.</span></span> 
    
5. <span data-ttu-id="ff4ae-141">Im Code-Editor von Visual Studio 2012 erhält den Fokus, und die haltepunktlinie wird hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-141">The Visual Studio 2012 code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
6. <span data-ttu-id="ff4ae-142">Klicken Sie im Menü **Debuggen** auf **Prozedurschritt** (oder drücken Sie UMSCHALT + F8) um das schrittweise Durchlaufen des Codes fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-142">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
7. <span data-ttu-id="ff4ae-p105">Der Ereignishandlercode wird ausgeführt, und die Meldung "Hello World!" wird angezeigt. </span><span class="sxs-lookup"><span data-stu-id="ff4ae-p105">The event handler code is executed, and the "Hello World!" message is displayed.</span></span> 
    
8. <span data-ttu-id="ff4ae-145">Klicken Sie auf **OK** , um zurück zum Code-Editor von Visual Studio 2012, und klicken Sie im Menü **Debuggen** auf **Debuggen beenden** (oder drücken Strg + Alt + UNTBR).</span><span class="sxs-lookup"><span data-stu-id="ff4ae-145">Click **OK** to return to the Visual Studio 2012 code editor, and then click **Stop Debugging** on the **Debug** menu (or press Ctrl+Alt+Break).</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="ff4ae-146">Abrufen des aktuellen Benutzers namens</span><span class="sxs-lookup"><span data-stu-id="ff4ae-146">Getting the current user's name</span></span>

<span data-ttu-id="ff4ae-147">Im folgenden Beispiel erfahren Sie, wie Sie die [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) -Eigenschaft der [Benutzer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) -Klasse verwenden, um den Namen des aktuellen Benutzers abrufen, und füllen Sie den Wert eines **Textfeld** -Steuerelements mit einem Ereignishandler für das [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-147">In the following example, you will learn how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the name of the current user and populate the value of a **Text Box** control by using an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
<span data-ttu-id="ff4ae-148">Füllen das **Textfeld** -Steuerelement erfolgt mithilfe einer Instanz der [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) -Klasse zum Schreiben des aktuellen Benutzers Name in der XML-Knoten, das an das Steuerelement gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-148">Populating the **Text Box** control is accomplished by using an instance of the [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) class to write the current user's name to the XML node that the control is bound to.</span></span> 
  
<span data-ttu-id="ff4ae-149">Zunächst wird die [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse aufgerufen, um eine Instanz der [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Klasse abrufen, die das zugrunde liegende XML-Dokument des Formulars darstellt.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-149">First, the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class is called to retrieve an instance of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class that represents the underlying XML document of the form.</span></span> <span data-ttu-id="ff4ae-150">Das [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Objekt ruft dann die [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode, die das **XPathNavigator** -Objekt erstellt und am Stammknoten der Hauptdatenquelle des Formulars positioniert.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-150">The [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) object then calls the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method, which creates the **XPathNavigator** object and positions it at the root node of the form's main data source.</span></span> 
  
<span data-ttu-id="ff4ae-151">Die [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) -Methode der **XPathNavigator** -Klasse aufgerufen, um Wählen Sie im Feld Employee in die Datenquelle des Formulars.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-151">The [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) method of the **XPathNavigator** class is called to select the employee field in the form's data source.</span></span> <span data-ttu-id="ff4ae-152">Abschließend wird die [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) -Methode aufgerufen, um den Wert des Felds mit der [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) -Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-152">Finally, the [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) method is called to set the value of the field with the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property.</span></span> 
  
<span data-ttu-id="ff4ae-153">Weitere Informationen zum Arbeiten mit **System.Xml** in Formularvorlagen mit verwaltetem Code finden Sie unter [Arbeiten mit dem XPathNavigator und XPathNodeIterator-Klassen](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).</span><span class="sxs-lookup"><span data-stu-id="ff4ae-153">For more information on working with **System.Xml** in managed code form templates, see [Work with the XPathNavigator and XPathNodeIterator Classes](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).</span></span>
  
### <a name="add-a-loading-event-handler"></a><span data-ttu-id="ff4ae-154">Hinzufügen eines Loading-Ereignishandlers </span><span class="sxs-lookup"><span data-stu-id="ff4ae-154">Add a Loading event handler</span></span>

1. <span data-ttu-id="ff4ae-155">Öffnen Sie die Formularvorlage "HelloWorld", die Sie in der vorherigen exemplarischen Vorgehensweise im InfoPath-Designer erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-155">Open the HelloWorld form template that you created in the previous walkthrough in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="ff4ae-156">Wählen Sie auf der Registerkarte **Ansicht** **Felder anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-156">On the **View** tab, select **Show Fields**.</span></span>
    
3. <span data-ttu-id="ff4ae-157">Klicken Sie mit der rechten Maustaste auf den Ordner **MyFields** , und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-157">Right click the **myFields** folder, and then click **Add**.</span></span>
    
4. <span data-ttu-id="ff4ae-158">Klicken Sie im Feld **Name**Geben Sie Mitarbeiter, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-158">In **Name**, type employee, and then click **OK**.</span></span>
    
5. <span data-ttu-id="ff4ae-159">Ziehen Sie im Feld Employee in die Ansicht.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-159">Drag the employee field onto the view.</span></span> 
    
6. <span data-ttu-id="ff4ae-160">Klicken Sie auf der Registerkarte **Entwicklertools** auf **Loading-Ereignis**.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-160">On the **Developer** tab, click **Loading Event**.</span></span>
    
   <span data-ttu-id="ff4ae-161">Erstellt einen Ereignishandler für das [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignis, und verschieben Sie den Fokus auf diesen Ereignishandler im Code-Editor.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-161">This will create an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, and move the focus to that event handler in the code editor.</span></span> 
    
7. <span data-ttu-id="ff4ae-162">Geben Sie im Code-Editor Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="ff4ae-162">In the code editor, type the following:</span></span>
    
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

8. <span data-ttu-id="ff4ae-163">Wechseln Sie in der InfoPath-Formularentwurfsfenster, und klicken Sie dann auf die Schaltfläche **Vorschau** auf der Registerkarte **Start** auf Vorschau des Formulars anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-163">Switch to the InfoPath form design window, and then click the **Preview** button on the **Home** tab to preview the form.</span></span> 
    
   <span data-ttu-id="ff4ae-164">Das Feld Employee sollte sich mit Ihrem Benutzernamen automatisch ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-164">The employee field should automatically fill in with your user name.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="ff4ae-165">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="ff4ae-165">Next steps</span></span>

- <span data-ttu-id="ff4ae-166">Informationen zum Arbeiten mit Ereignishandlern für andere Steuerelemente und Ereignisse finden Sie unter [Hinzufügen eines Ereignishandlers](how-to-add-an-event-handler.md).</span><span class="sxs-lookup"><span data-stu-id="ff4ae-166">For information about working with event handlers for other controls and events, see [Add an Event Handler](how-to-add-an-event-handler.md).</span></span>
    
- <span data-ttu-id="ff4ae-167">Weitere Informationen zum Anzeigen einer Vorschau und Debuggen von Code in Formularvorlagen finden Sie unter [Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="ff4ae-167">For more information about previewing and debugging code in form templates, see [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="ff4ae-168">Informationen zum Bereitstellen einer Formularvorlage mit verwaltetem Code finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="ff4ae-168">For information about how to deploy a managed-code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="ff4ae-169">Informationen zu den InfoPath-Objektmodell und allgemeine Programmieraufgaben in Formularvorlagen mit verwaltetem Code finden Sie unter [Grundlegendes zum InfoPath-Objektmodell und zu allgemeinen Entwickleraufgaben](understanding-the-infopath-object-model-and-common-developer-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="ff4ae-169">For information about the InfoPath object model and common programming tasks in managed-code form templates, see [Understanding the InfoPath Object Model and Common Developer Tasks](understanding-the-infopath-object-model-and-common-developer-tasks.md)</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff4ae-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff4ae-170">See also</span></span>

- [<span data-ttu-id="ff4ae-171">XmlForm</span><span class="sxs-lookup"><span data-stu-id="ff4ae-171">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

