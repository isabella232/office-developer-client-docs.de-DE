---
title: Anzeigen von Warnungen und Dialogfelder mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-kompatible Formularvorlagen, Anzeigen von Dialogfelder,Formularvorlagen [InfoPath 2007], Anzeigen von Dialogfelder,Warnungen, Anzeigen in InfoPath 2003-kompatiblen Formularvorlagen,Dialogfelder, Anzeigen in InfoPath 2003-kompatiblen Formularvorlagen,InfoPath 2003-kompatible Formularvorlagen, Anzeigen von Warnungen
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: Beim Schreiben von Code, um die Funktionalität einer Formularvorlage zu erweitern, die das InfoPath 2003-Objektmodell verwendet, empfiehlt es sich häufig, dem Benutzer Informationen in einem Dialogfeld bereitzustellen.
ms.openlocfilehash: 12088747250037e53a3b7d8d0577936e30d6292c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409482"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a><span data-ttu-id="dfc19-104">Anzeigen von Warnungen und Dialogfelder mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="dfc19-104">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="dfc19-105">Beim Schreiben von Code, um die Funktionalität einer Formularvorlage zu erweitern, die das InfoPath 2003-Objektmodell verwendet, empfiehlt es sich häufig, dem Benutzer Informationen in einem Dialogfeld bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="dfc19-105">When writing code to extend the functionality of a form template that uses the InfoPath 2003 object model, it is often useful to provide the user with information in a dialog box.</span></span> <span data-ttu-id="dfc19-106">Die programmgesteuerte Anzeige eines Dialogfelds und zugehöriger Benutzeroberflächenelemente erfolgt in InfoPath mithilfe der Methoden der [UIObject-Schnittstelle.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)</span><span class="sxs-lookup"><span data-stu-id="dfc19-106">Programmatically displaying a dialog box and related user interface elements is accomplished in InfoPath by using the methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
## <a name="overview-of-the-uiobject-interface"></a><span data-ttu-id="dfc19-107">Übersicht über die UIObject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dfc19-107">Overview of the UIObject Interface</span></span>

<span data-ttu-id="dfc19-108">Die [UIObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) bietet die folgenden Methoden, mit denen Formularentwickler unterschiedliche Arten von Dialogfeldern den InfoPath-Benutzern beim Ausfüllen eines Formulars anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="dfc19-108">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface provides the following methods, which form developers can use to have different types of dialog boxes displayed to InfoPath users as they are filling out a form.</span></span> 
  
|<span data-ttu-id="dfc19-109">Name</span><span class="sxs-lookup"><span data-stu-id="dfc19-109">Name</span></span>|<span data-ttu-id="dfc19-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfc19-110">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dfc19-111">Warnung</span><span class="sxs-lookup"><span data-stu-id="dfc19-111">Alert</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |<span data-ttu-id="dfc19-p102">Zeigt ein einfaches Meldungsfeld an, das eine bestimmte Meldungszeichenfolge enthält. Diese Methode sollte dann verwendet werden, wenn keine Benutzereingaben erforderlich sind und nur eine Meldung angezeigt werden muss. Das Dialogfeld wird durch Klicken auf die Schaltfläche **OK** geschlossen.</span><span class="sxs-lookup"><span data-stu-id="dfc19-p102">Displays a simple message box that contains a specified message string. This method should be used when no input is required from the user and only a message needs to be displayed. The dialog box displayed is closed by clicking the **OK** button.  </span></span><br/> |
|[<span data-ttu-id="dfc19-115">Confirm</span><span class="sxs-lookup"><span data-stu-id="dfc19-115">Confirm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |<span data-ttu-id="dfc19-116">Zeigt ein Meldungsfeld mit Schaltflächen für Benutzereingaben an.</span><span class="sxs-lookup"><span data-stu-id="dfc19-116">Displays a message box with buttons for input from a user.</span></span> <span data-ttu-id="dfc19-117">Der zurückgegebene Wert ist eine der [XdConfirmChoice-Enumerationskonstante.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx)</span><span class="sxs-lookup"><span data-stu-id="dfc19-117">The value that is returned is one of the [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) enumerated constants.</span></span>  <br/> |
|[<span data-ttu-id="dfc19-118">SetSaveAsDialogFileName</span><span class="sxs-lookup"><span data-stu-id="dfc19-118">SetSaveAsDialogFileName</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |<span data-ttu-id="dfc19-119">Legt den Standarddateinamen für ein Formular im Dialogfeld **Speichern unter** fest.</span><span class="sxs-lookup"><span data-stu-id="dfc19-119">Sets the default file name for a form in the **Save As** dialog box.</span></span>  <br/> |
|[<span data-ttu-id="dfc19-120">SetSaveAsDialogLocation</span><span class="sxs-lookup"><span data-stu-id="dfc19-120">SetSaveAsDialogLocation</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |<span data-ttu-id="dfc19-121">Legt den Ausgangsort fest, an dem das Dialogfeld **Speichern unter** beim Öffnen mit der Navigation beginnt.</span><span class="sxs-lookup"><span data-stu-id="dfc19-121">Sets the initial location at which the **Save As** dialog box starts to browse when it is opened.</span></span>  <br/> |
|[<span data-ttu-id="dfc19-122">ShowMailItem</span><span class="sxs-lookup"><span data-stu-id="dfc19-122">ShowMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |<span data-ttu-id="dfc19-123">Erstellt eine neue E-Mail-Nachricht in der Standard-E-Mail-Anwendung mit dem derzeit geöffneten Formular, das der Nachricht angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="dfc19-123">Creates a new email message in the default email application, with the currently open form attached to the message.</span></span>  <br/> |
|[<span data-ttu-id="dfc19-124">ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="dfc19-124">ShowModalDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |<span data-ttu-id="dfc19-125">Zeigt ein modales Dialogfeld basierend auf der angegebenen HTML-Datei und positionellen Argumenten an.</span><span class="sxs-lookup"><span data-stu-id="dfc19-125">Displays a modal dialog box, based on the specified .html file and positional arguments.</span></span> <span data-ttu-id="dfc19-126">Diese Methode sollte verwendet werden, wenn Sie dem Benutzer mehr als eine einfache Nachricht anzeigen möchten und einige Daten  vom Benutzer zurückerstatten müssen (über die einfache Bestätigung hinaus, die vom Ja bereitgestellt wird).</span><span class="sxs-lookup"><span data-stu-id="dfc19-126">This method should be used if you want to display more than a simple message to the user and you need to get back some data from the user (beyond the simple confirmation that is provided by the **Yes**</span></span> | <span data-ttu-id="dfc19-127">**Nein**</span><span class="sxs-lookup"><span data-stu-id="dfc19-127">**No**</span></span> | <span data-ttu-id="dfc19-128">**Schaltflächen** abbrechen, die von der **Confirm-Methode angezeigt** werden).</span><span class="sxs-lookup"><span data-stu-id="dfc19-128">**Cancel** buttons displayed by the **Confirm** method).</span></span>  <br/> |
|[<span data-ttu-id="dfc19-129">ShowSignatureDialog</span><span class="sxs-lookup"><span data-stu-id="dfc19-129">ShowSignatureDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |<span data-ttu-id="dfc19-130">Zeigt das integrierte Dialogfeld **Digitale Signaturen** an.</span><span class="sxs-lookup"><span data-stu-id="dfc19-130">Displays the built-in **Digital Signatures** dialog box.</span></span>  <br/> |
   
## <a name="using-the-uiobject-interface"></a><span data-ttu-id="dfc19-131">Verwenden der UIObject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="dfc19-131">Using the UIObject Interface</span></span>

<span data-ttu-id="dfc19-132">Auf [die UIObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) wird über die [UI-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) der [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) zugegriffen, auf die selbst über die Variable zugegriffen wird, die in der Methode der Formularcodeklasse initialisiert  `thisXDocument`  `_Startup` wird.</span><span class="sxs-lookup"><span data-stu-id="dfc19-132">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface is accessed through the [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, which itself is accessed through the  `thisXDocument` variable that is initialized in the  `_Startup` method of the form code class.</span></span> <span data-ttu-id="dfc19-133">Im folgenden Beispiel wird die Verwendung der [ShowMailItem-](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) und [Alert-Methoden](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) der [UIObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="dfc19-133">The following example demonstrates using the [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) and [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
```cs
thisXDocument.UI.ShowMailItem("someone@example.com","", "", 
   "Updated Form", "Here is the updated form that you requested.");
thisXDocument.UI.Alert("The email message has been created.");
```

```vb
thisXDocument.UI.ShowMailItem("someone@example.com", "", "", _
   "Updated Form", "Here is the updated form that you requested.")
thisXDocument.UI.Alert("The email message has been created.")
```

## <a name="using-the-showmodaldialog-method"></a><span data-ttu-id="dfc19-134">Verwenden der ShowModalDialog-Methode</span><span class="sxs-lookup"><span data-stu-id="dfc19-134">Using the ShowModalDialog Method</span></span>

<span data-ttu-id="dfc19-135">In diesem Beispiel wird veranschaulicht, wie Sie die [ShowModalDialog-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) der [UIObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) verwenden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das in der HTML-Datei show.html definiert ist.</span><span class="sxs-lookup"><span data-stu-id="dfc19-135">This example demonstrates how to use the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface to display a custom dialog box defined in the HTML file show.html.</span></span> 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Write your code here.
   thisXDocument.UI.ShowModalDialog(
      "show.html",(object)thisXDocument,200,450,50,50);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Write your code here.
   thisXDocument.UI.ShowModalDialog( _
      "show.html", _
      DirectCast(thisXDocument, Object), 200, 450, 50, 50)
End Sub

```

<span data-ttu-id="dfc19-136">Sowohl visual C# als auch Visual Basic sind von einer HTML-Datei namens "show.html" abhängig, die das Dialogfeld definiert, das von der [ShowModalDialog-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="dfc19-136">Both the Visual C# and Visual Basic samples depend on an HTML file named "show.html" that defines the dialog box that is invoked by the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method.</span></span> <span data-ttu-id="dfc19-137">In dieser HTML-Datei werden einige Daten aus dem Formular und ein Textfeld angezeigt, in dem der Benutzer einen Wert ausfüllen kann.</span><span class="sxs-lookup"><span data-stu-id="dfc19-137">This HTML file displays some data from the form and shows a text box for the user to fill in a value.</span></span> <span data-ttu-id="dfc19-138">Der Wert im Textfeld wird an das Formular zurückgegeben, wenn das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="dfc19-138">The value in the textbox is returned to the form when the dialog box is closed.</span></span> 
  
```html
<HTML>
   <HEAD>
      <script language="JScript">
function BtnClick()
{
   xdocument = window.dialogArguments;
   myXml = xdocument.DOM.xml
   aForm = oForm.elements;
   aForm.textBox.value = myXml;
}
      </script>
   </HEAD>
   <BODY>
      <H1><FONT face="Arial">This is a modal dialog box</FONT> &nbsp;
      </H1>
      <BUTTON onclick="BtnClick()" id="BUTTON1" type="button">
         Get XML DOM
      </BUTTON>
      <FORM ID="oForm">
         <INPUT Type="text" name="textBox">
      </FORM>
   </BODY>
</HTML>

```

> [!IMPORTANT]
> <span data-ttu-id="dfc19-139">Für [die ShowModalDialog-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) ist die Ausführung oder Vorschau der voll vertrauenswürdigen Methode erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dfc19-139">The [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method requires Full Trust to run or preview.</span></span> <span data-ttu-id="dfc19-140">Weitere Informationen finden Sie unter [Vorschau und Debuggen von Formularvorlagen, die voll vertrauenswürdig sind.](how-to-preview-and-debug-form-templates-that-require-full-trust.md)</span><span class="sxs-lookup"><span data-stu-id="dfc19-140">For more information, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  

