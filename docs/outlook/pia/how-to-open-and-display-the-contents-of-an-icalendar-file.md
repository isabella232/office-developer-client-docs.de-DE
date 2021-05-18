---
title: Öffnen und Anzeigen des Inhalts einer iCalendar-Datei
TOCTitle: Open and display the contents of an iCalendar file
ms:assetid: 2066e404-7aaf-4fd2-bf5c-9604e3fc2681
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644609(v=office.15)
ms:contentKeyID: 55119818
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fad55b4e9b98a2157d1efdab83d5495cd2169429
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320020"
---
# <a name="open-and-display-the-contents-of-an-icalendar-file"></a><span data-ttu-id="b7ce9-102">Öffnen und Anzeigen des Inhalts einer iCalendar-Datei</span><span class="sxs-lookup"><span data-stu-id="b7ce9-102">Open and display the contents of an iCalendar file</span></span>

<span data-ttu-id="b7ce9-103">In diesem Beispiel wird gezeigt, wie Inhalte einer iCalendar-Datei geöffnet und angezeigt werden, abhängig davon, ob die Datei einen einzelnen Termin, eine Terminserie oder eine Gruppe von Terminen enthält.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-103">This example shows how to open and display the contents of an iCalendar file, depending on whether the file contains a single or recurrent appointment, or the file contains a group of appointments.</span></span>

## <a name="example"></a><span data-ttu-id="b7ce9-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b7ce9-104">Example</span></span>

<span data-ttu-id="b7ce9-p101">In diesem Codebeispiel wird zuerst versucht, die [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) -Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekts zu verwenden, um die iCalendar-Datei als iCalendar-Datei mit einem einzelnen Termin zu öffnen. Ist dieser Versuch erfolgreich, werden die Einzelheiten des Termins in einem Inspektorfenster angezeigt. Das Element wird jedoch nicht in den Standardspeicher kopiert. Wenn die Datei durch das Codebeispiel nicht als iCalendar-Datei mit einem einzelnen Termin geöffnet werden kann, wird mithilfe der [OpenSharedFolder](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) -Methode des **NameSpace**-Objekts versucht, die Inhalte als neuen Kalender in den Standardspeicher zu importieren. Ist der Import erfolgt, wird der Kalender in einem Explorer-Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-p101">This code sample first tries to use the [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to open the iCalendar file as a single-appointment iCalendar file. If it succeeds, it will display the appointment item details in an inspector window. However, it will not copy the item to the default store. If the sample cannot open the file as a single-appointment iCalendar file, then it will use the [OpenSharedFolder](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the **NameSpace** object to attempt to import the contents as a new calendar in the default store. If it succeeds in importing, then it will display the calendar in an explorer window.</span></span>

<span data-ttu-id="b7ce9-110">In diesem Codebeispiel wird die OutlookItem-Hilfsklasse verwendet, die unter [Erstellen einer Hilfsklasse zum Zugriff auf allgemeine Member von Outlook-Elementen](how-to-create-a-helper-class-to-access-common-outlook-item-members.md) definiert ist, um die **OutlookItem.Display**-Methode zum Anzeigen des Terminelements aufzurufen, ohne das Element zunächst umwandeln zu müssen.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-110">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the **OutlookItem.Display** method to display the appointment item without having to first cast the item.</span></span>

<span data-ttu-id="b7ce9-111">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="b7ce9-112">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b7ce9-113">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="b7ce9-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub OpenICalendarFile(ByVal fileName As String)
    If String.IsNullOrEmpty(fileName) Then
        Throw New ArgumentException(_
        "Parameter must contain a value.", "exportFileName")
    End If
    If Not File.Exists(fileName) Then
        Throw New FileNotFoundException(fileName)
    End If

    '' First try to open the icalendar file as an appointment 
    '' (not a calendar folder).
    Dim item As Object = Nothing
    Try
         item = Application.Session.OpenSharedItem(fileName)
    Catch
    End Try

    If Not item Is Nothing Then
        '' Display the item
        Dim olItem As OutlookItem = New OutlookItem(item)
        olItem.Display()
        Return
    End If

    '' If unsucessful in opening it as an item, 
    '' try opening it as a folder
    Dim importedFolder As Outlook.Folder = Nothing
    Try
        importedFolder = TryCast( _
            Application.Session.OpenSharedFolder(fileName), _
            Outlook.Folder)
    Catch
    End Try

    '' If sucessful, open the folder in a new explorer window
    If Not importedFolder Is Nothing Then
        Dim explorer As Outlook.Explorer = _
            Application.Explorers.Add( _
            importedFolder, _
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal)
        explorer.Display()
    End If
End Sub
```


```csharp
private void OpenICalendarFile(string fileName)
{
    if (string.IsNullOrEmpty(fileName))
        throw new ArgumentException("exportFileName", 
        "Parameter must contain a value.");
    if (!File.Exists(fileName))
        throw new FileNotFoundException(fileName);

    // First try to open the icalendar file as an appointment 
    // (not a calendar folder).
    object item = null;
    try
    {
        item = Application.Session.OpenSharedItem(fileName);
    }
    catch
    { }

    if (item != null)
    {
         // Display the item
         OutlookItem olItem = new OutlookItem(item);
         olItem.Display();
         return;
    }

    // If unsucessful in opening it as an item, 
    // try opening it as a folder
    Outlook.Folder importedFolder = null;
    try
    {
        importedFolder = Application.Session.OpenSharedFolder(
            fileName, Type.Missing, Type.Missing, Type.Missing) 
            as Outlook.Folder;
    }
    catch
    { }

    // If sucessful, open the folder in a new explorer window
    if (importedFolder != null)
    {
        Outlook.Explorer explorer =
            Application.Explorers.Add(importedFolder, 
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        explorer.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="b7ce9-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7ce9-114">See also</span></span>

- [<span data-ttu-id="b7ce9-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="b7ce9-115">Calendar</span></span>](calendar.md)

