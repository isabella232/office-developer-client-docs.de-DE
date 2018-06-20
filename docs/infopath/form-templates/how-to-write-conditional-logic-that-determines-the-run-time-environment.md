---
title: Schreiben von bedingter Logik, der bestimmt, die zur Laufzeit-Umgebung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Ausführen in Infopath [Infopath 2007] Laufzeitumgebung [InfoPath 2007], in Browser [InfoPath 2007], InfoPath 2007-Laufzeit Umgebung bestimmen ausgeführt wird
localization_priority: Normal
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: Die Umgebung-Eigenschaft des Application-Klasse ruft einen Verweis auf ein Umgebungsobjekt, die verwendet werden kann, in welcher Laufzeitumgebung (InfoPath, Webbrowser oder mobiler Browser) wurde verwendet, um das Formular zu öffnen.
ms.openlocfilehash: b854d6a3b65fcc37375480bef9f1909d84407b6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790742"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a>Schreiben von bedingter Logik, der bestimmt, die zur Laufzeit-Umgebung

Die [Umgebung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) -Eigenschaft des [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse ruft einen Verweis auf ein Objekt [Umgebung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) , die verwendet werden kann, in welcher Laufzeitumgebung (InfoPath, Webbrowser oder mobiler Browser) wurde verwendet, um das Formular zu öffnen. 
  
## <a name="example"></a>Beispiel

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a>Bestimmen der Laufzeitumgebung, in der ein Formular ausgeführt wird

Die [Umgebung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) -Klasse stellt die Eigenschaften [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) und [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) , mit denen Sie bestimmen, welche Umgebung bearbeiten zum Öffnen einer Formularvorlage verwendet wurde. Wenn beide Eigenschaften **false**zurückgibt, wurde die Formularvorlage in Microsoft InfoPath-Editor geöffnet. Wenn entweder-Eigenschaft **true**zurückgibt, wurde die Formularvorlage aus einer entsprechend konfigurierten Dokumentenbibliothek auf Microsoft SharePoint Server 2010 mit InfoPath Forms Services in der Anwendung für die entsprechende Eigenschaft geöffnet: einen Webbrowser ([ IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) -Eigenschaft) oder eines mobilen Browsers ( [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) -Eigenschaft). 
  
Im folgenden Beispiel wird das Formular in einem Browser oder mobiler Browser geöffnet wird der Wert der Feld1 (das an ein **Textfeld** -Steuerelement gebunden ist) auf eine Zeichenfolge festgelegt um anzugeben, welcher Laufzeitumgebung das Formular, in geöffnet wurde. Wenn das Formular in InfoPath geöffnet ist, wird die **System.Windows.Forms.MessageBox.Show** -Methode (Dies ist nicht verfügbar, wenn ein Formular in einem Browser ausgeführt wird) verwendet, um ein Meldungsfeld anzuzeigen. 
  
> [!IMPORTANT]
> Wenn Sie die Formularvorlage für das folgende Codebeispiel erstellen, wählen Sie die **leere** Vorlage auf der Registerkarte **neu** der Backstage-Ansicht. (Alternativ können Sie **Webbrowserformular** aus der Dropdownliste **Formulartyp** unter der Kategorie **Kompatibilität** im Dialogfeld **Formularoptionen** auswählen.) Fügen Sie einen Verweis auf **System.Windows.Forms** auf, um das **Abfrageergebnis** -Klasse unterstützt, die. **NET** -Registerkarte des Dialogfelds **Verweis hinzufügen** in Visual Studio 2012 ein, und fügen Sie eine **Using-** oder **Imports** -Direktive für **System.Windows.Forms** im Deklarationsabschnitt des formularcodemoduls. 
  
```cs
if(this.Application.Environment.IsBrowser)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a browser.");
}
else if (this.Application.Environment.IsMobile)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a mobile browser.");
}
else
{
   MessageBox.Show("This form is running in the InfoPath editor.");
}
```

```vb
If (Me.Application.Environment.IsBrowser) Then
   CreateNavigator().SelectSingleNode(_
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a browser.")
ElseIf (Me.Application.Environment.IsMobile) Then
   CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a mobile browser.")
Else
   MessageBox.Show("This form is running in the InfoPath editor.")
End If
```


