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
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a><span data-ttu-id="2c759-104">Schreiben von bedingter Logik, der bestimmt, die zur Laufzeit-Umgebung</span><span class="sxs-lookup"><span data-stu-id="2c759-104">Write Conditional Logic That Determines the Run-time Environment</span></span>

<span data-ttu-id="2c759-105">Die [Umgebung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) -Eigenschaft des [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse ruft einen Verweis auf ein Objekt [Umgebung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) , die verwendet werden kann, in welcher Laufzeitumgebung (InfoPath, Webbrowser oder mobiler Browser) wurde verwendet, um das Formular zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c759-105">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class gets a reference to an [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) object, which can be used to determine which runtime environment (InfoPath, Web browser, or mobile browser) was used to open the form.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2c759-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2c759-106">Example</span></span>

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a><span data-ttu-id="2c759-107">Bestimmen der Laufzeitumgebung, in der ein Formular ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="2c759-107">Determining Which Runtime Environment a Form is Running In</span></span>

<span data-ttu-id="2c759-108">Die [Umgebung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) -Klasse stellt die Eigenschaften [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) und [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) , mit denen Sie bestimmen, welche Umgebung bearbeiten zum Öffnen einer Formularvorlage verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2c759-108">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) class provides the [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) and [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) properties that enable you to determine what editing environment was used to open a form template.</span></span> <span data-ttu-id="2c759-109">Wenn beide Eigenschaften **false**zurückgibt, wurde die Formularvorlage in Microsoft InfoPath-Editor geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2c759-109">If both properties return **false**, the form template was opened in the Microsoft InfoPath editor.</span></span> <span data-ttu-id="2c759-110">Wenn entweder-Eigenschaft **true**zurückgibt, wurde die Formularvorlage aus einer entsprechend konfigurierten Dokumentenbibliothek auf Microsoft SharePoint Server 2010 mit InfoPath Forms Services in der Anwendung für die entsprechende Eigenschaft geöffnet: einen Webbrowser ([ IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) -Eigenschaft) oder eines mobilen Browsers ( [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) -Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="2c759-110">If either property returns **true**, the form template was opened from an appropriately configured document library on Microsoft SharePoint Server 2010 running InfoPath Forms Services in the program for the corresponding property: a Web browser ([IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) property) or a mobile browser ( [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) property).</span></span> 
  
<span data-ttu-id="2c759-111">Im folgenden Beispiel wird das Formular in einem Browser oder mobiler Browser geöffnet wird der Wert der Feld1 (das an ein **Textfeld** -Steuerelement gebunden ist) auf eine Zeichenfolge festgelegt um anzugeben, welcher Laufzeitumgebung das Formular, in geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="2c759-111">In the following example, if the form is opened in a browser or mobile browser, the value of field1 (which is bound to a **Text Box** control) is set to a string to indicate which runtime environment the form was opened in.</span></span> <span data-ttu-id="2c759-112">Wenn das Formular in InfoPath geöffnet ist, wird die **System.Windows.Forms.MessageBox.Show** -Methode (Dies ist nicht verfügbar, wenn ein Formular in einem Browser ausgeführt wird) verwendet, um ein Meldungsfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2c759-112">If the form is opened in InfoPath, the **System.Windows.Forms.MessageBox.Show** method (which isn't available when a form is running in a browser) is used to display a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="2c759-113">Wenn Sie die Formularvorlage für das folgende Codebeispiel erstellen, wählen Sie die **leere** Vorlage auf der Registerkarte **neu** der Backstage-Ansicht.</span><span class="sxs-lookup"><span data-stu-id="2c759-113">When you create the form template for the following code sample, select the **Blank** template on the **New** tab of the Backstage view.</span></span> <span data-ttu-id="2c759-114">(Alternativ können Sie **Webbrowserformular** aus der Dropdownliste **Formulartyp** unter der Kategorie **Kompatibilität** im Dialogfeld **Formularoptionen** auswählen.) Fügen Sie einen Verweis auf **System.Windows.Forms** auf, um das **Abfrageergebnis** -Klasse unterstützt, die.</span><span class="sxs-lookup"><span data-stu-id="2c759-114">(Alternatively, you can select **Web Browser Form** from the **Form type** drop-down list under the **Compatibility** category of the **Form Options** dialog box.) To support the **MessageBox** class, add a reference to **System.Windows.Forms** on the .</span></span> <span data-ttu-id="2c759-115">**NET** -Registerkarte des Dialogfelds **Verweis hinzufügen** in Visual Studio 2012 ein, und fügen Sie eine **Using-** oder **Imports** -Direktive für **System.Windows.Forms** im Deklarationsabschnitt des formularcodemoduls.</span><span class="sxs-lookup"><span data-stu-id="2c759-115">**NET** tab of the **Add Reference** dialog box in Visual Studio 2012, and then add a **using** or **Imports** directive for **System.Windows.Forms** in the declarations section of the form code module.</span></span> 
  
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


