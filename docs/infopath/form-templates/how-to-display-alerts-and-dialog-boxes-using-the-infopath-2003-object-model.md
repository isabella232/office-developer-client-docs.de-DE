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
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a>Anzeigen von Warnungen und Dialog Feldern mit dem InfoPath-Objektmodell 2003

Beim Schreiben von Code, um die Funktionalität einer Formularvorlage zu erweitern, die das InfoPath 2003-Objektmodell verwendet, empfiehlt es sich häufig, dem Benutzer Informationen in einem Dialogfeld bereitzustellen. Programmgesteuertes Anzeigen eines Dialogfelds und zugehöriger Benutzeroberflächenelemente wird in InfoPath mithilfe der Methoden der [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle ausgeführt. 
  
## <a name="overview-of-the-uiobject-interface"></a>Übersicht über die UIObject-Schnittstelle

Die [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle stellt die folgenden Methoden bereit, mit denen Formularentwickler beim Ausfüllen eines Formulars unterschiedliche Arten von Dialogfeldern für InfoPath-Benutzer anzeigen können. 
  
|Name|Beschreibung|
|:-----|:-----|
|[Warnung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |Zeigt ein einfaches Meldungsfeld an, das eine bestimmte Meldungszeichenfolge enthält. Diese Methode sollte dann verwendet werden, wenn keine Benutzereingaben erforderlich sind und nur eine Meldung angezeigt werden muss. Das Dialogfeld wird durch Klicken auf die Schaltfläche **OK** geschlossen.<br/> |
|[Confirm](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |Zeigt ein Meldungsfeld mit Schaltflächen für Benutzereingaben an. Der zurückgegebene Wert ist eine der aufgezählten [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) -Konstanten.  <br/> |
|[SetSaveAsDialogFileName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |Legt den Standarddateinamen für ein Formular im Dialogfeld **Speichern unter** fest.  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |Legt den Ausgangsort fest, an dem das Dialogfeld **Speichern unter** beim Öffnen mit der Navigation beginnt.  <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |Erstellt eine neue e-Mail-Nachricht in der Standard-e-Mail-Anwendung, wobei das derzeit geöffnete Formular an die Nachricht angefügt ist.  <br/> |
|[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |Zeigt ein modales Dialogfeld basierend auf der angegebenen HTML-Datei und positionellen Argumenten an. Diese Methode sollte verwendet werden, wenn Sie mehr als eine einfache Nachricht für den Benutzer anzeigen möchten, und Sie müssen einige Daten vom Benutzer zurück erhalten (abgesehen von der einfachen Bestätigung, die vom **Ja** | **Nein** | Von der **Confirm** -Methode angezeigte Schaltflächen **Abbrechen** ).  <br/> |
|[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |Zeigt das integrierte Dialogfeld **Digitale Signaturen** an.  <br/> |
   
## <a name="using-the-uiobject-interface"></a>Verwenden der UIObject-Schnittstelle

Der Zugriff auf die [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle erfolgt über die [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) -Eigenschaft der [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle, `thisXDocument` auf die selbst über die Variable `_Startup` zugegriffen wird, die in der Methode der Formularcodeklasse initialisiert wird. Das folgende Beispiel veranschaulicht die Verwendung der [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) -und der [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) -Methode der [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle. 
  
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

In diesem Beispiel wird veranschaulicht, wie die [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) -Methode der [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle verwendet wird, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das in der HTML-Datei Show. HTML definiert ist. 
  
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

Sowohl die Visual C#-als auch die Visual Basic-Beispiele sind von einer HTML-Datei mit dem Namen "Show. html" abhängig, die das von der [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) -Methode aufgerufene Dialogfeld definiert. In dieser HTML-Datei werden einige Daten aus dem Formular angezeigt, und es wird ein Textfeld angezeigt, in dem der Benutzer einen Wert eingeben muss. Der Wert im TextBox-Steuerobjekt wird an das Formular zurückgegeben, wenn das Dialogfeld geschlossen wird. 
  
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
> Die [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) -Methode erfordert volle Vertrauenswürdigkeit zum Ausführen oder Vorschau. Weitere Informationen finden Sie unter [Vorschau und Debuggen von Formularvorlagen, die volle VertrauenswürdigKeit erfordern](how-to-preview-and-debug-form-templates-that-require-full-trust.md). 
  

