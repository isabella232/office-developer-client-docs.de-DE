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
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a>Anzeigen von Warnungen und Dialogfeldern mit dem InfoPath 2003-Objektmodell

Beim Schreiben von Code zum Erweitern der Funktionalität des einer Formularvorlage, die das InfoPath 2003-Objektmodell verwendet, ist es oft sinnvoll, die den Benutzer Informationen in einem Dialogfeld bereitzustellen. Programmgesteuertes Anzeigen eines Dialogfelds und verwandte Elemente der Benutzeroberfläche in InfoPath erfolgt mithilfe der Methods der [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle. 
  
## <a name="overview-of-the-uiobject-interface"></a>Übersicht über die UIObject-Schnittstelle

Die [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle bietet die folgenden Methoden, die Formularentwickler verwenden können, damit unterschiedliche Arten von Dialogfeldern für InfoPath-Benutzer angezeigt wird, wie sie ein Formular ausfüllen. 
  
|Name|Beschreibung|
|:-----|:-----|
|[Warnen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |Zeigt ein einfaches Meldungsfeld an, das eine angegebene Meldungszeichenfolge enthält. Diese Methode sollte verwendet werden, wenn keine Eingabe vom Benutzer erforderlich ist und nur eine Meldung angezeigt werden muss. Das angezeigte Dialogfeld wird geschlossen, indem Sie auf die Schaltfläche **OK** .  <br/> |
|[Vergewissern Sie sich](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |Zeigt ein Meldungsfeld mit Schaltflächen für Benutzereingaben an. Der zurückgegebene Wert ist eine der Konstanten [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) aufgelistet.  <br/> |
|[SetSaveAsDialogFileName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |Legt den Standarddateinamen für ein Formular im Dialogfeld **Speichern unter** fest.  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |Legt den Ausgangsort, an dem das Dialogfeld **Speichern unter** beginnt um wechseln, wenn es geöffnet wird.  <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |Erstellt eine neue e-Mail-Nachricht in der standardmäßige e-Mail-Anwendung, mit das derzeit geöffnete Formular an die Nachricht angefügt.  <br/> |
|[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |Zeigt ein modales Dialogfeld, basierend auf der angegebenen HTML-Datei und positionelle Argumente an. Diese Methode sollte verwendet werden, wenn Sie mehr als eine einfache Meldung für den Benutzer anzeigen möchten, und Sie müssen, erhalten einige Daten vom Benutzer (über die einfache Bestätigung, die von der **Ja** bereitgestellt wird | **Nein** | **Abbrechen** Schaltflächen angezeigt, indem die **Confirm** -Methode).  <br/> |
|[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |Zeigt das integrierte Dialogfeld **Digitale Signaturen** .  <br/> |
   
## <a name="using-the-uiobject-interface"></a>Verwenden der UIObject-Schnittstelle

Die [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle erfolgt über die [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) -Eigenschaft des [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle, die wiederum über zugegriffen wird die `thisXDocument` Variable, die in initialisiert wird die `_Startup` -Methode des Form-Codeklasse. Im folgenden Beispiel wird mithilfe der Methoden [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) und [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) des [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle. 
  
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

In diesem Beispiel wird veranschaulicht, wie die [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) -Methode des [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle verwenden Sie zum Anzeigen eines benutzerdefinierten Dialogfelds, in der HTML-Datei show.html definiert. 
  
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

Die Visual c# und Visual Basic-Beispiele richten sich nach einer HTML-Datei mit dem Namen "show.html", die das Dialogfeld definiert, die von der [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) -Methode aufgerufen wird. Diese HTML-Datei zeigt einige Daten aus dem Formular und ein Textfeld für den Benutzer auf einen Wert eingeben. Der Wert in das Textfeld wird an das Formular zurückgegeben, wenn das Dialogfeld geschlossen wird. 
  
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
> Die [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) -Methode erfordert voll vertrauenswürdig ausgeführt oder eine Vorschau anzeigen. Weitere Informationen finden Sie unter [Anzeigen der Vorschau und Debuggen von Formularvorlagen, erfordern voll vertrauenswürdig](how-to-preview-and-debug-form-templates-that-require-full-trust.md). 
  

