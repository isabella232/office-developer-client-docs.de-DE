---
title: Schreiben von bedingter Logik, die die Laufzeitumgebung bestimmt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- running in infopath [infopath 2007],run-time environment [InfoPath 2007],running in browser [InfoPath 2007],InfoPath 2007, determining run-time environment
ms.localizationpriority: medium
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: Die Environment-Eigenschaft der Application-Klasse ruft einen Verweis auf ein Environment-Objekt ab, mit dem bestimmt werden kann, welche Laufzeitumgebung (InfoPath, Webbrowser oder mobiler Browser) zum Öffnen des Formulars verwendet wurde.
ms.openlocfilehash: 347633f0dc13b8b001ca146cd56aa734c0edc8b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625819"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a>Schreiben von bedingter Logik, die die Laufzeitumgebung bestimmt

Die [Environment-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) ruft einen Verweis auf ein [Environment-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) ab, mit dem bestimmt werden kann, welche Laufzeitumgebung (InfoPath, Webbrowser oder mobiler Browser) zum Öffnen des Formulars verwendet wurde. 
  
## <a name="example"></a>Beispiel

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a>Bestimmen der Laufzeitumgebung, in der ein Formular ausgeführt wird

Die [Environment-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) stellt die [IsBrowser-](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) und [IsMobile-Eigenschaften](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) bereit, mit denen Sie bestimmen können, welche Bearbeitungsumgebung zum Öffnen einer Formularvorlage verwendet wurde. Wenn beide Eigenschaften **"false"** zurückgeben, wurde die Formularvorlage im Microsoft InfoPath-Editor geöffnet. Wenn eine der Eigenschaften **"true"** zurückgibt, wurde die Formularvorlage in einer entsprechend konfigurierten Dokumentbibliothek Microsoft SharePoint Server 2010 geöffnet, die InfoPath Forms Services im Programm für die entsprechende Eigenschaft ausführt: einen Webbrowser ([IsBrowser-Eigenschaft)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) oder einen mobilen Browser ( [IsMobile-Eigenschaft).](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) 
  
Im folgenden Beispiel wird beim Öffnen des Formulars in einem Browser oder mobilen Browser für den Wert von field1 (der an ein Steuerelement vom Typ **Textfeld** gebunden ist) eine Zeichenfolge festgelegt, um anzugeben, in welcher Laufzeitumgebung das Formular geöffnet wurde. Wenn das Formular in InfoPath geöffnet wird, wird die **System.Windows.Forms.MessageBox.Show**-Methode (die beim Öffnen eines Formulars in einem Browser nicht verfügbar ist) zum Anzeigen eines Mitteilungsfelds verwendet. 
  
> [!IMPORTANT]
> Wenn Sie die Formularvorlage für das folgende Codebeispiel erstellen, wählen Sie auf der Registerkarte **"Neu"** der Backstage-Ansicht die Vorlage **"Leer"** aus. (Alternativ können Sie im Dialogfeld **"Formularoptionen"** in der Dropdownliste **"Formulartyp"** in der Kategorie **"Kompatibilität"** das Webbrowserformular **auswählen.)** Um die **MessageBox-Klasse** zu unterstützen, fügen Sie einen Verweis auf **"System.Windows" hinzu. Formulare** auf der . **Net** tab of the **Add Reference** dialog box in Visual Studio 2012, and then add a **using** or **Imports** directive for **System.Windows. Formulare** im Deklarationsbereich des Formularcodemoduls. 
  
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


