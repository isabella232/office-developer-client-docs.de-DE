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
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a><span data-ttu-id="0e198-104">Schreiben von bedingter Logik zur Bestimmung der Laufzeitumgebung</span><span class="sxs-lookup"><span data-stu-id="0e198-104">Write Conditional Logic That Determines the Run-time Environment</span></span>

<span data-ttu-id="0e198-105">Die [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) -Eigenschaft der [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse ruft einen Verweis auf ein [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) -Objekt ab, das verwendet werden kann, um zu bestimmen, welche Laufzeitumgebung (InfoPath, Webbrowser oder mobiler Browser) zum Öffnen des Formulars verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0e198-105">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class gets a reference to an [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) object, which can be used to determine which runtime environment (InfoPath, Web browser, or mobile browser) was used to open the form.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0e198-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0e198-106">Example</span></span>

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a><span data-ttu-id="0e198-107">Bestimmen der Laufzeitumgebung, in der ein Formular ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="0e198-107">Determining Which Runtime Environment a Form is Running In</span></span>

<span data-ttu-id="0e198-108">Die [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) -Klasse stellt [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) die isBrowser-und IsMobile-Eigenschaften bereit, mit denen Sie bestimmen können, welche Bearbeitungsumgebung zum Öffnen einer Formularvorlage verwendet wurde. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e198-108">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) class provides the [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) and [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) properties that enable you to determine what editing environment was used to open a form template.</span></span> <span data-ttu-id="0e198-109">Wenn beide Eigenschaften **false**zurückgeben, wurde die Formularvorlage im Microsoft InfoPath-Editor geöffnet.</span><span class="sxs-lookup"><span data-stu-id="0e198-109">If both properties return **false**, the form template was opened in the Microsoft InfoPath editor.</span></span> <span data-ttu-id="0e198-110">Wenn eine der Eigenschaften **true**zurückgibt, wurde die Formularvorlage aus einer entsprechend konfigurierten dokumentBibliothek in Microsoft SharePoint Server 2010 mit InfoPath Forms Services im Programm für die entsprechende Eigenschaft geöffnet: ein Webbrowser ([ IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) -Eigenschaft) oder ein mobiler [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) Browser (IsMobile-Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="0e198-110">If either property returns **true**, the form template was opened from an appropriately configured document library on Microsoft SharePoint Server 2010 running InfoPath Forms Services in the program for the corresponding property: a Web browser ([IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) property) or a mobile browser ( [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) property).</span></span> 
  
<span data-ttu-id="0e198-111">Im folgenden Beispiel wird beim Öffnen des Formulars in einem Browser oder mobilen Browser für den Wert von field1 (der an ein Steuerelement vom Typ **Textfeld** gebunden ist) eine Zeichenfolge festgelegt, um anzugeben, in welcher Laufzeitumgebung das Formular geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="0e198-111">In the following example, if the form is opened in a browser or mobile browser, the value of field1 (which is bound to a **Text Box** control) is set to a string to indicate which runtime environment the form was opened in.</span></span> <span data-ttu-id="0e198-112">Wenn das Formular in InfoPath geöffnet wird, wird die **System.Windows.Forms.MessageBox.Show**-Methode (die beim Öffnen eines Formulars in einem Browser nicht verfügbar ist) zum Anzeigen eines Mitteilungsfelds verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e198-112">If the form is opened in InfoPath, the **System.Windows.Forms.MessageBox.Show** method (which isn't available when a form is running in a browser) is used to display a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="0e198-113">Wenn Sie die Formularvorlage für das folgende Codebeispiel erstellen, wählen Sie die **leere** Vorlage auf der Registerkarte **neu** der backstaging-Ansicht aus.</span><span class="sxs-lookup"><span data-stu-id="0e198-113">When you create the form template for the following code sample, select the **Blank** template on the **New** tab of the Backstage view.</span></span> <span data-ttu-id="0e198-114">(Alternativ können Sie in der Dropdownliste Formulartyp unter \*\*\*\* der Kategorie **Kompatibilität** des Dialogfelds **Formularoptionen** die Option **Webbrowserformular** auswählen.) Um die **MessageBox** -Klasse zu unterstützen, fügen Sie einen Verweis auf **System. Windows. Forms** in.</span><span class="sxs-lookup"><span data-stu-id="0e198-114">(Alternatively, you can select **Web Browser Form** from the **Form type** drop-down list under the **Compatibility** category of the **Form Options** dialog box.) To support the **MessageBox** class, add a reference to **System.Windows.Forms** on the .</span></span> <span data-ttu-id="0e198-115">**Net** im Dialogfeld **Verweis hinzufügen** in Visual Studio 2012, und fügen Sie dann eine **using** - \*\*\*\* oder Imports-Direktive für **System. Windows. Forms** im Deklarationsabschnitt des Formularcodemoduls hinzu.</span><span class="sxs-lookup"><span data-stu-id="0e198-115">**NET** tab of the **Add Reference** dialog box in Visual Studio 2012, and then add a **using** or **Imports** directive for **System.Windows.Forms** in the declarations section of the form code module.</span></span> 
  
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


