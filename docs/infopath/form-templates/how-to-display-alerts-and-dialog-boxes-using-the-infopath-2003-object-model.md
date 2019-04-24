---
title: Anzeigen von Warnungen und Dialog Feldern mit dem InfoPath-Objektmodell 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen, Anzeigen von Dialogfeldern, Formularvorlagen [InfoPath 2007], Anzeigen von Dialogfeldern, Warnungen, Anzeigen in InfoPath 2003-kompatiblen Formularvorlagen, Dialogfeldern, Anzeigen in InfoPath 2003-kompatible Formularvorlagen , InfoPath 2003-kompatible Formularvorlagen, Warnungen anzeigen
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: Beim Schreiben von Code, um die Funktionalität einer Formularvorlage zu erweitern, die das InfoPath 2003-Objektmodell verwendet, empfiehlt es sich häufig, dem Benutzer Informationen in einem Dialogfeld bereitzustellen.
ms.openlocfilehash: 12088747250037e53a3b7d8d0577936e30d6292c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303612"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a><span data-ttu-id="6ddd8-104">Anzeigen von Warnungen und Dialog Feldern mit dem InfoPath-Objektmodell 2003</span><span class="sxs-lookup"><span data-stu-id="6ddd8-104">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="6ddd8-105">Beim Schreiben von Code, um die Funktionalität einer Formularvorlage zu erweitern, die das InfoPath 2003-Objektmodell verwendet, empfiehlt es sich häufig, dem Benutzer Informationen in einem Dialogfeld bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-105">When writing code to extend the functionality of a form template that uses the InfoPath 2003 object model, it is often useful to provide the user with information in a dialog box.</span></span> <span data-ttu-id="6ddd8-106">Programmgesteuertes Anzeigen eines Dialogfelds und zugehöriger Benutzeroberflächenelemente wird in InfoPath mithilfe der Methoden der [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-106">Programmatically displaying a dialog box and related user interface elements is accomplished in InfoPath by using the methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
## <a name="overview-of-the-uiobject-interface"></a><span data-ttu-id="6ddd8-107">Übersicht über die UIObject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6ddd8-107">Overview of the UIObject Interface</span></span>

<span data-ttu-id="6ddd8-108">Die [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle stellt die folgenden Methoden bereit, mit denen Formularentwickler beim Ausfüllen eines Formulars unterschiedliche Arten von Dialogfeldern für InfoPath-Benutzer anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-108">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface provides the following methods, which form developers can use to have different types of dialog boxes displayed to InfoPath users as they are filling out a form.</span></span> 
  
|<span data-ttu-id="6ddd8-109">Name</span><span class="sxs-lookup"><span data-stu-id="6ddd8-109">Name</span></span>|<span data-ttu-id="6ddd8-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ddd8-110">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ddd8-111">Warnung</span><span class="sxs-lookup"><span data-stu-id="6ddd8-111">Alert</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |<span data-ttu-id="6ddd8-p102">Zeigt ein einfaches Meldungsfeld an, das eine bestimmte Meldungszeichenfolge enthält. Diese Methode sollte dann verwendet werden, wenn keine Benutzereingaben erforderlich sind und nur eine Meldung angezeigt werden muss. Das Dialogfeld wird durch Klicken auf die Schaltfläche **OK** geschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-p102">Displays a simple message box that contains a specified message string. This method should be used when no input is required from the user and only a message needs to be displayed. The dialog box displayed is closed by clicking the **OK** button.  </span></span><br/> |
|[<span data-ttu-id="6ddd8-115">Confirm</span><span class="sxs-lookup"><span data-stu-id="6ddd8-115">Confirm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |<span data-ttu-id="6ddd8-116">Zeigt ein Meldungsfeld mit Schaltflächen für Benutzereingaben an.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-116">Displays a message box with buttons for input from a user.</span></span> <span data-ttu-id="6ddd8-117">Der zurückgegebene Wert ist eine der aufgezählten [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) -Konstanten.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-117">The value that is returned is one of the [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) enumerated constants.</span></span>  <br/> |
|[<span data-ttu-id="6ddd8-118">SetSaveAsDialogFileName</span><span class="sxs-lookup"><span data-stu-id="6ddd8-118">SetSaveAsDialogFileName</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |<span data-ttu-id="6ddd8-119">Legt den Standarddateinamen für ein Formular im Dialogfeld **Speichern unter** fest.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-119">Sets the default file name for a form in the **Save As** dialog box.</span></span>  <br/> |
|[<span data-ttu-id="6ddd8-120">SetSaveAsDialogLocation</span><span class="sxs-lookup"><span data-stu-id="6ddd8-120">SetSaveAsDialogLocation</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |<span data-ttu-id="6ddd8-121">Legt den Ausgangsort fest, an dem das Dialogfeld **Speichern unter** beim Öffnen mit der Navigation beginnt.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-121">Sets the initial location at which the **Save As** dialog box starts to browse when it is opened.</span></span>  <br/> |
|[<span data-ttu-id="6ddd8-122">ShowMailItem</span><span class="sxs-lookup"><span data-stu-id="6ddd8-122">ShowMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |<span data-ttu-id="6ddd8-123">Erstellt eine neue e-Mail-Nachricht in der Standard-e-Mail-Anwendung, wobei das derzeit geöffnete Formular an die Nachricht angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-123">Creates a new email message in the default email application, with the currently open form attached to the message.</span></span>  <br/> |
|[<span data-ttu-id="6ddd8-124">ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="6ddd8-124">ShowModalDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |<span data-ttu-id="6ddd8-125">Zeigt ein modales Dialogfeld basierend auf der angegebenen HTML-Datei und positionellen Argumenten an.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-125">Displays a modal dialog box, based on the specified .html file and positional arguments.</span></span> <span data-ttu-id="6ddd8-126">Diese Methode sollte verwendet werden, wenn Sie mehr als eine einfache Nachricht für den Benutzer anzeigen möchten, und Sie müssen einige Daten vom Benutzer zurück erhalten (abgesehen von der einfachen Bestätigung, die vom **Ja**</span><span class="sxs-lookup"><span data-stu-id="6ddd8-126">This method should be used if you want to display more than a simple message to the user and you need to get back some data from the user (beyond the simple confirmation that is provided by the **Yes**</span></span> | <span data-ttu-id="6ddd8-127">**Nein**</span><span class="sxs-lookup"><span data-stu-id="6ddd8-127">**No**</span></span> | <span data-ttu-id="6ddd8-128">Von der **Confirm** -Methode angezeigte Schaltflächen **Abbrechen** ).</span><span class="sxs-lookup"><span data-stu-id="6ddd8-128">**Cancel** buttons displayed by the **Confirm** method).</span></span>  <br/> |
|[<span data-ttu-id="6ddd8-129">ShowSignatureDialog</span><span class="sxs-lookup"><span data-stu-id="6ddd8-129">ShowSignatureDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |<span data-ttu-id="6ddd8-130">Zeigt das integrierte Dialogfeld **Digitale Signaturen** an.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-130">Displays the built-in **Digital Signatures** dialog box.</span></span>  <br/> |
   
## <a name="using-the-uiobject-interface"></a><span data-ttu-id="6ddd8-131">Verwenden der UIObject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6ddd8-131">Using the UIObject Interface</span></span>

<span data-ttu-id="6ddd8-132">Der Zugriff auf die [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle erfolgt über die [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) -Eigenschaft der [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle, `thisXDocument` auf die selbst über die Variable `_Startup` zugegriffen wird, die in der Methode der Formularcodeklasse initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-132">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface is accessed through the [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, which itself is accessed through the  `thisXDocument` variable that is initialized in the  `_Startup` method of the form code class.</span></span> <span data-ttu-id="6ddd8-133">Das folgende Beispiel veranschaulicht die Verwendung der [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) -und der [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) -Methode der [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-133">The following example demonstrates using the [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) and [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
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

## <a name="using-the-showmodaldialog-method"></a><span data-ttu-id="6ddd8-134">Verwenden der ShowModalDialog-Methode</span><span class="sxs-lookup"><span data-stu-id="6ddd8-134">Using the ShowModalDialog Method</span></span>

<span data-ttu-id="6ddd8-135">In diesem Beispiel wird veranschaulicht, wie die [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) -Methode der [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle verwendet wird, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das in der HTML-Datei Show. HTML definiert ist.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-135">This example demonstrates how to use the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface to display a custom dialog box defined in the HTML file show.html.</span></span> 
  
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

<span data-ttu-id="6ddd8-136">Sowohl die Visual C#-als auch die Visual Basic-Beispiele sind von einer HTML-Datei mit dem Namen "Show. html" abhängig, die das von der [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) -Methode aufgerufene Dialogfeld definiert.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-136">Both the Visual C# and Visual Basic samples depend on an HTML file named "show.html" that defines the dialog box that is invoked by the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method.</span></span> <span data-ttu-id="6ddd8-137">In dieser HTML-Datei werden einige Daten aus dem Formular angezeigt, und es wird ein Textfeld angezeigt, in dem der Benutzer einen Wert eingeben muss.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-137">This HTML file displays some data from the form and shows a text box for the user to fill in a value.</span></span> <span data-ttu-id="6ddd8-138">Der Wert im TextBox-Steuerobjekt wird an das Formular zurückgegeben, wenn das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-138">The value in the textbox is returned to the form when the dialog box is closed.</span></span> 
  
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
> <span data-ttu-id="6ddd8-139">Die [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) -Methode erfordert volle Vertrauenswürdigkeit zum Ausführen oder Vorschau.</span><span class="sxs-lookup"><span data-stu-id="6ddd8-139">The [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method requires Full Trust to run or preview.</span></span> <span data-ttu-id="6ddd8-140">Weitere Informationen finden Sie unter [Vorschau und Debuggen von Formularvorlagen, die volle VertrauenswürdigKeit erfordern](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="6ddd8-140">For more information, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  

