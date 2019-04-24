---
title: Schreiben von bedingter Logik zur Bestimmung der Laufzeitumgebung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Ausführen in InfoPath [InfoPath 2007], Run-Time Environment [InfoPath 2007], Running in Browser [InfoPath 2007], InfoPath 2007, bestimmen der Laufzeitumgebung
localization_priority: Normal
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: Die Environment-Eigenschaft der Application-Klasse ruft einen Verweis auf ein Environment-Objekt ab, das verwendet werden kann, um zu bestimmen, welche Laufzeitumgebung (InfoPath, Webbrowser oder mobiler Browser) zum Öffnen des Formulars verwendet wurde.
ms.openlocfilehash: 31bfd8dcd05d52d6c6e162d4aa4838e423d97e0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299727"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a>Schreiben von bedingter Logik zur Bestimmung der Laufzeitumgebung

Die [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) -Eigenschaft der [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse ruft einen Verweis auf ein [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) -Objekt ab, das verwendet werden kann, um zu bestimmen, welche Laufzeitumgebung (InfoPath, Webbrowser oder mobiler Browser) zum Öffnen des Formulars verwendet wurde. 
  
## <a name="example"></a>Beispiel

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a>Bestimmen der Laufzeitumgebung, in der ein Formular ausgeführt wird

Die [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) -Klasse stellt [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) die isBrowser-und IsMobile-Eigenschaften bereit, mit denen Sie bestimmen können, welche Bearbeitungsumgebung zum Öffnen einer Formularvorlage verwendet wurde. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) Wenn beide Eigenschaften **false**zurückgeben, wurde die Formularvorlage im Microsoft InfoPath-Editor geöffnet. Wenn eine der Eigenschaften **true**zurückgibt, wurde die Formularvorlage aus einer entsprechend konfigurierten dokumentBibliothek in Microsoft SharePoint Server 2010 mit InfoPath Forms Services im Programm für die entsprechende Eigenschaft geöffnet: ein Webbrowser ([ IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) -Eigenschaft) oder ein mobiler [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) Browser (IsMobile-Eigenschaft). 
  
Im folgenden Beispiel wird beim Öffnen des Formulars in einem Browser oder mobilen Browser für den Wert von field1 (der an ein Steuerelement vom Typ **Textfeld** gebunden ist) eine Zeichenfolge festgelegt, um anzugeben, in welcher Laufzeitumgebung das Formular geöffnet wurde. Wenn das Formular in InfoPath geöffnet wird, wird die **System.Windows.Forms.MessageBox.Show**-Methode (die beim Öffnen eines Formulars in einem Browser nicht verfügbar ist) zum Anzeigen eines Mitteilungsfelds verwendet. 
  
> [!IMPORTANT]
> Wenn Sie die Formularvorlage für das folgende Codebeispiel erstellen, wählen Sie die **leere** Vorlage auf der Registerkarte **neu** der backstaging-Ansicht aus. (Alternativ können Sie in der Dropdownliste Formulartyp unter **** der Kategorie **Kompatibilität** des Dialogfelds **Formularoptionen** die Option **Webbrowserformular** auswählen.) Um die **MessageBox** -Klasse zu unterstützen, fügen Sie einen Verweis auf **System. Windows. Forms** in. **Net** im Dialogfeld **Verweis hinzufügen** in Visual Studio 2012, und fügen Sie dann eine **using** - **** oder Imports-Direktive für **System. Windows. Forms** im Deklarationsabschnitt des Formularcodemoduls hinzu. 
  
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


