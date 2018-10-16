---
title: Zugreifen auf lösungsspezifische Daten, die als ausgeblendete Nachricht in einem Ordner gespeichert sind
TOCTitle: Access solution-specific data stored as a hidden message in a folder
ms:assetid: bacf0562-1026-4c3b-87b0-4eaad5033592
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623414(v=office.15)
ms:contentKeyID: 55119861
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 5134cc2b3a71f8fe93970f040a44d16291dbbb0c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405546"
---
# <a name="access-solution-specific-data-stored-as-a-hidden-message-in-a-folder"></a><span data-ttu-id="10865-102">Zugreifen auf lösungsspezifische Daten, die als ausgeblendete Nachricht in einem Ordner gespeichert sind</span><span class="sxs-lookup"><span data-stu-id="10865-102">Access solution-specific data stored as a hidden message in a folder</span></span>

<span data-ttu-id="10865-103">Dieses Beispiel zeigt die Verwendung des [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) -Objekts zum Abrufen von Daten, die als ausgeblendete Nachricht einer bestimmten Nachrichtenklasse in einem Ordner gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="10865-103">This example shows how to use the [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) object to retrieve data that is stored as a hidden message of a specific message class in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="10865-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="10865-104">Example</span></span>

<span data-ttu-id="10865-p101">Das **StorageItem**-Objekt wird üblicherweise verwendet, um lösungsspezifische Daten auszublenden, die nicht programmgesteuert angezeigt werden können. In einer Exchange-Umgebung wird das **StorageItem**-Objekt zum Roaming von Lösungseinstellungen verwendet und um sicherzustellen, dass diese Einstellungen online und offline verfügbar sind. Sie können dem **StorageItem**-Objekt eine benutzerdefinierte Nachrichtenklasse zuweisen oder das Objekt durch den Betreff identifizieren.</span><span class="sxs-lookup"><span data-stu-id="10865-p101">The **StorageItem** object is typically used to hide solution-specific data that cannot be displayed programmatically. In an Exchange environment, the **StorageItem** object is used to roam solution settings and ensure that these settings are available online and offline. You can assign a custom message class to the **StorageItem** object, or identify the object by subject.</span></span>

<span data-ttu-id="10865-108">Im folgenden Codebeispiel werden die XML-Daten abgerufen, die im Kalenderordner als ausgeblendete Nachricht mit der Nachrichtenklasse IPM.Configuration.WorkHours gespeichert sind. </span><span class="sxs-lookup"><span data-stu-id="10865-108">The following code sample retrieves the XML data that is stored as a hidden message in the Calendar folder with the message class equal to IPM.Configuration.WorkHours.</span></span>

<span data-ttu-id="10865-p102">Das [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) -Objekt gibt die XML-Daten in Form eines Objekts zurück, das anstelle einer Zeichenkettendarstellung der XML-Daten einen Datenstrom enthält. Der Datenstrom wird im Codebeispiel mithilfe von **System.Text.Encoding.Ascii.GetString** in eine Zeichenfolge umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="10865-p102">The [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object returns the XML as an object that contains a byte stream rather than a string representation of the XML. The code sample uses **System.Text.Encoding.Ascii.GetString** to convert the byte stream to a string.</span></span>

<span data-ttu-id="10865-111">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="10865-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="10865-112">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="10865-112">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="10865-113">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="10865-113">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Function GetWorkHoursXML() As String
    Try
        Dim storage As Outlook.StorageItem = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderCalendar).GetStorage( _
            "IPM.Configuration.WorkHours", _
            Outlook.OlStorageIdentifierType.olIdentifyByMessageClass)
        Dim pa As Outlook.PropertyAccessor = storage.PropertyAccessor
        ' PropertyAccessor will return a byte array for this property
        Dim rawXmlBytes As Byte() = CType(pa.GetProperty( _
            "https://schemas.microsoft.com/mapi/proptag/0x7C080102"), _
            Byte())
        ' Use Encoding to convert the array to a string
        Return System.Text.Encoding.ASCII.GetString(rawXmlBytes)
    Catch
        Return String.Empty
    End Try
End Function
```

```csharp
private string GetWorkHoursXML()
{
    try
    {
        Outlook.StorageItem storage =
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderCalendar).GetStorage(
            "IPM.Configuration.WorkHours",
            Outlook.OlStorageIdentifierType.olIdentifyByMessageClass);
        Outlook.PropertyAccessor pa = storage.PropertyAccessor;
        // PropertyAccessor will return a byte array for this property
        byte[] rawXmlBytes = (byte[])pa.GetProperty(
            "https://schemas.microsoft.com/mapi/proptag/0x7C080102");
        // Use Encoding to convert the array to a string
        return System.Text.Encoding.ASCII.GetString(rawXmlBytes);
    }
    catch
    {
        return string.Empty;
    }
}
```


## <a name="see-also"></a><span data-ttu-id="10865-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10865-114">See also</span></span>

- [<span data-ttu-id="10865-115">Folders</span><span class="sxs-lookup"><span data-stu-id="10865-115">Folders</span></span>](folders.md)

