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
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a>Anzeigen von Warnungen und Dialogfelder mithilfe des InfoPath 2003-Objektmodells

Beim Schreiben von Code, um die Funktionalität einer Formularvorlage zu erweitern, die das InfoPath 2003-Objektmodell verwendet, empfiehlt es sich häufig, dem Benutzer Informationen in einem Dialogfeld bereitzustellen. Die programmgesteuerte Anzeige eines Dialogfelds und zugehöriger Benutzeroberflächenelemente erfolgt in InfoPath mithilfe der Methoden der [UIObject-Schnittstelle.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) 
  
## <a name="overview-of-the-uiobject-interface"></a>Übersicht über die UIObject-Schnittstelle

Die [UIObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) bietet die folgenden Methoden, mit denen Formularentwickler unterschiedliche Arten von Dialogfeldern den InfoPath-Benutzern beim Ausfüllen eines Formulars anzeigen können. 
  
|Name|Beschreibung|
|:-----|:-----|
|[Warnung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |Zeigt ein einfaches Meldungsfeld an, das eine bestimmte Meldungszeichenfolge enthält. Diese Methode sollte dann verwendet werden, wenn keine Benutzereingaben erforderlich sind und nur eine Meldung angezeigt werden muss. Das Dialogfeld wird durch Klicken auf die Schaltfläche **OK** geschlossen.<br/> |
|[Confirm](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |Zeigt ein Meldungsfeld mit Schaltflächen für Benutzereingaben an. Der zurückgegebene Wert ist eine der [XdConfirmChoice-Enumerationskonstante.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx)  <br/> |
|[SetSaveAsDialogFileName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |Legt den Standarddateinamen für ein Formular im Dialogfeld **Speichern unter** fest.  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |Legt den Ausgangsort fest, an dem das Dialogfeld **Speichern unter** beim Öffnen mit der Navigation beginnt.  <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |Erstellt eine neue E-Mail-Nachricht in der Standard-E-Mail-Anwendung mit dem derzeit geöffneten Formular, das der Nachricht angefügt ist.  <br/> |
|[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |Zeigt ein modales Dialogfeld basierend auf der angegebenen HTML-Datei und positionellen Argumenten an. Diese Methode sollte verwendet werden, wenn Sie dem Benutzer mehr als eine einfache Nachricht anzeigen möchten und einige Daten  vom Benutzer zurückerstatten müssen (über die einfache Bestätigung hinaus, die vom Ja bereitgestellt wird). | **Nein** | **Schaltflächen** abbrechen, die von der **Confirm-Methode angezeigt** werden).  <br/> |
|[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |Zeigt das integrierte Dialogfeld **Digitale Signaturen** an.  <br/> |
   
## <a name="using-the-uiobject-interface"></a>Verwenden der UIObject-Schnittstelle

Auf [die UIObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) wird über die [UI-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) der [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) zugegriffen, auf die selbst über die Variable zugegriffen wird, die in der Methode der Formularcodeklasse initialisiert  `thisXDocument`  `_Startup` wird. Im folgenden Beispiel wird die Verwendung der [ShowMailItem-](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) und [Alert-Methoden](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) der [UIObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) veranschaulicht. 
  
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

## <a name="using-the-showmodaldialog-method"></a>Verwenden der ShowModalDialog-Methode

In diesem Beispiel wird veranschaulicht, wie Sie die [ShowModalDialog-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) der [UIObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) verwenden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das in der HTML-Datei show.html definiert ist. 
  
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

Sowohl visual C# als auch Visual Basic sind von einer HTML-Datei namens "show.html" abhängig, die das Dialogfeld definiert, das von der [ShowModalDialog-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) aufgerufen wird. In dieser HTML-Datei werden einige Daten aus dem Formular und ein Textfeld angezeigt, in dem der Benutzer einen Wert ausfüllen kann. Der Wert im Textfeld wird an das Formular zurückgegeben, wenn das Dialogfeld geschlossen wird. 
  
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
> Für [die ShowModalDialog-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) ist die Ausführung oder Vorschau der voll vertrauenswürdigen Methode erforderlich. Weitere Informationen finden Sie unter [Vorschau und Debuggen von Formularvorlagen, die voll vertrauenswürdig sind.](how-to-preview-and-debug-form-templates-that-require-full-trust.md) 
  

