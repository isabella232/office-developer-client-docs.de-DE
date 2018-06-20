---
title: Anzeigen von Warnungen und Dialogfeldern mit dem InfoPath 2003-Objektmodell
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen, Anzeigen von Dialogfeldern, Formularvorlagen [InfoPath 2007], Anzeigen von Dialogfeldern, Benachrichtigungen, Anzeigen von in InfoPath 2003-kompatible Formularvorlagen, Dialogfelder anzeigen in InfoPath 2003-kompatible Formularvorlagen , InfoPath 2003-kompatible Formularvorlagen, Anzeigen von Warnungen
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: Beim Schreiben von Code zum Erweitern der Funktionalität des einer Formularvorlage, die das InfoPath 2003-Objektmodell verwendet, ist es oft sinnvoll, die den Benutzer Informationen in einem Dialogfeld bereitzustellen.
ms.openlocfilehash: 1cc0f4c7a6696eae2d3b7058898b4119cede79e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790744"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a><span data-ttu-id="831f0-104">Anzeigen von Warnungen und Dialogfeldern mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="831f0-104">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="831f0-105">Beim Schreiben von Code zum Erweitern der Funktionalität des einer Formularvorlage, die das InfoPath 2003-Objektmodell verwendet, ist es oft sinnvoll, die den Benutzer Informationen in einem Dialogfeld bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="831f0-105">When writing code to extend the functionality of a form template that uses the InfoPath 2003 object model, it is often useful to provide the user with information in a dialog box.</span></span> <span data-ttu-id="831f0-106">Programmgesteuertes Anzeigen eines Dialogfelds und verwandte Elemente der Benutzeroberfläche in InfoPath erfolgt mithilfe der Methods der [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="831f0-106">Programmatically displaying a dialog box and related user interface elements is accomplished in InfoPath by using the methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
## <a name="overview-of-the-uiobject-interface"></a><span data-ttu-id="831f0-107">Übersicht über die UIObject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="831f0-107">Overview of the UIObject Interface</span></span>

<span data-ttu-id="831f0-108">Die [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle bietet die folgenden Methoden, die Formularentwickler verwenden können, damit unterschiedliche Arten von Dialogfeldern für InfoPath-Benutzer angezeigt wird, wie sie ein Formular ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="831f0-108">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface provides the following methods, which form developers can use to have different types of dialog boxes displayed to InfoPath users as they are filling out a form.</span></span> 
  
|<span data-ttu-id="831f0-109">Name</span><span class="sxs-lookup"><span data-stu-id="831f0-109">Name</span></span>|<span data-ttu-id="831f0-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="831f0-110">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="831f0-111">Warnen</span><span class="sxs-lookup"><span data-stu-id="831f0-111">Alert</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |<span data-ttu-id="831f0-112">Zeigt ein einfaches Meldungsfeld an, das eine angegebene Meldungszeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="831f0-112">Displays a simple message box that contains a specified message string.</span></span> <span data-ttu-id="831f0-113">Diese Methode sollte verwendet werden, wenn keine Eingabe vom Benutzer erforderlich ist und nur eine Meldung angezeigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="831f0-113">This method should be used when no input is required from the user and only a message needs to be displayed.</span></span> <span data-ttu-id="831f0-114">Das angezeigte Dialogfeld wird geschlossen, indem Sie auf die Schaltfläche **OK** .</span><span class="sxs-lookup"><span data-stu-id="831f0-114">The dialog box displayed is closed by clicking the **OK** button.</span></span>  <br/> |
|[<span data-ttu-id="831f0-115">Vergewissern Sie sich</span><span class="sxs-lookup"><span data-stu-id="831f0-115">Confirm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |<span data-ttu-id="831f0-116">Zeigt ein Meldungsfeld mit Schaltflächen für Benutzereingaben an.</span><span class="sxs-lookup"><span data-stu-id="831f0-116">Displays a message box with buttons for input from a user.</span></span> <span data-ttu-id="831f0-117">Der zurückgegebene Wert ist eine der Konstanten [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="831f0-117">The value that is returned is one of the [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) enumerated constants.</span></span>  <br/> |
|[<span data-ttu-id="831f0-118">SetSaveAsDialogFileName</span><span class="sxs-lookup"><span data-stu-id="831f0-118">SetSaveAsDialogFileName</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |<span data-ttu-id="831f0-119">Legt den Standarddateinamen für ein Formular im Dialogfeld **Speichern unter** fest.</span><span class="sxs-lookup"><span data-stu-id="831f0-119">Sets the default file name for a form in the **Save As** dialog box.</span></span>  <br/> |
|[<span data-ttu-id="831f0-120">SetSaveAsDialogLocation</span><span class="sxs-lookup"><span data-stu-id="831f0-120">SetSaveAsDialogLocation</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |<span data-ttu-id="831f0-121">Legt den Ausgangsort, an dem das Dialogfeld **Speichern unter** beginnt um wechseln, wenn es geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="831f0-121">Sets the initial location at which the **Save As** dialog box starts to browse when it is opened.</span></span>  <br/> |
|[<span data-ttu-id="831f0-122">ShowMailItem</span><span class="sxs-lookup"><span data-stu-id="831f0-122">ShowMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |<span data-ttu-id="831f0-123">Erstellt eine neue e-Mail-Nachricht in der standardmäßige e-Mail-Anwendung, mit das derzeit geöffnete Formular an die Nachricht angefügt.</span><span class="sxs-lookup"><span data-stu-id="831f0-123">Creates a new email message in the default email application, with the currently open form attached to the message.</span></span>  <br/> |
|[<span data-ttu-id="831f0-124">ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="831f0-124">ShowModalDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |<span data-ttu-id="831f0-125">Zeigt ein modales Dialogfeld, basierend auf der angegebenen HTML-Datei und positionelle Argumente an.</span><span class="sxs-lookup"><span data-stu-id="831f0-125">Displays a modal dialog box, based on the specified .html file and positional arguments.</span></span> <span data-ttu-id="831f0-126">Diese Methode sollte verwendet werden, wenn Sie mehr als eine einfache Meldung für den Benutzer anzeigen möchten, und Sie müssen, erhalten einige Daten vom Benutzer (über die einfache Bestätigung, die von der **Ja** bereitgestellt wird</span><span class="sxs-lookup"><span data-stu-id="831f0-126">This method should be used if you want to display more than a simple message to the user and you need to get back some data from the user (beyond the simple confirmation that is provided by the **Yes**</span></span> | <span data-ttu-id="831f0-127">**Nein**</span><span class="sxs-lookup"><span data-stu-id="831f0-127">**No**</span></span> | <span data-ttu-id="831f0-128">**Abbrechen** Schaltflächen angezeigt, indem die **Confirm** -Methode).</span><span class="sxs-lookup"><span data-stu-id="831f0-128">**Cancel** buttons displayed by the **Confirm** method).</span></span>  <br/> |
|[<span data-ttu-id="831f0-129">ShowSignatureDialog</span><span class="sxs-lookup"><span data-stu-id="831f0-129">ShowSignatureDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |<span data-ttu-id="831f0-130">Zeigt das integrierte Dialogfeld **Digitale Signaturen** .</span><span class="sxs-lookup"><span data-stu-id="831f0-130">Displays the built-in **Digital Signatures** dialog box.</span></span>  <br/> |
   
## <a name="using-the-uiobject-interface"></a><span data-ttu-id="831f0-131">Verwenden der UIObject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="831f0-131">Using the UIObject Interface</span></span>

<span data-ttu-id="831f0-132">Die [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle erfolgt über die [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) -Eigenschaft des [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle, die wiederum über zugegriffen wird die `thisXDocument` Variable, die in initialisiert wird die `_Startup` -Methode des Form-Codeklasse.</span><span class="sxs-lookup"><span data-stu-id="831f0-132">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface is accessed through the [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, which itself is accessed through the  `thisXDocument` variable that is initialized in the  `_Startup` method of the form code class.</span></span> <span data-ttu-id="831f0-133">Im folgenden Beispiel wird mithilfe der Methoden [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) und [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) des [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="831f0-133">The following example demonstrates using the [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) and [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
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

## <a name="using-the-showmodaldialog-method"></a><span data-ttu-id="831f0-134">Verwenden der ShowModalDialog-Methode</span><span class="sxs-lookup"><span data-stu-id="831f0-134">Using the ShowModalDialog Method</span></span>

<span data-ttu-id="831f0-135">In diesem Beispiel wird veranschaulicht, wie die [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) -Methode des [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle verwenden Sie zum Anzeigen eines benutzerdefinierten Dialogfelds, in der HTML-Datei show.html definiert.</span><span class="sxs-lookup"><span data-stu-id="831f0-135">This example demonstrates how to use the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface to display a custom dialog box defined in the HTML file show.html.</span></span> 
  
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

<span data-ttu-id="831f0-136">Die Visual c# und Visual Basic-Beispiele richten sich nach einer HTML-Datei mit dem Namen "show.html", die das Dialogfeld definiert, die von der [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="831f0-136">Both the Visual C# and Visual Basic samples depend on an HTML file named "show.html" that defines the dialog box that is invoked by the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method.</span></span> <span data-ttu-id="831f0-137">Diese HTML-Datei zeigt einige Daten aus dem Formular und ein Textfeld für den Benutzer auf einen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="831f0-137">This HTML file displays some data from the form and shows a text box for the user to fill in a value.</span></span> <span data-ttu-id="831f0-138">Der Wert in das Textfeld wird an das Formular zurückgegeben, wenn das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="831f0-138">The value in the textbox is returned to the form when the dialog box is closed.</span></span> 
  
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
> <span data-ttu-id="831f0-139">Die [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) -Methode erfordert voll vertrauenswürdig ausgeführt oder eine Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="831f0-139">The [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method requires Full Trust to run or preview.</span></span> <span data-ttu-id="831f0-140">Weitere Informationen finden Sie unter [Anzeigen der Vorschau und Debuggen von Formularvorlagen, erfordern voll vertrauenswürdig](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="831f0-140">For more information, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  

