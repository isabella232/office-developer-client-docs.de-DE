---
title: Zugreifen auf lösungsspezifische Daten, die als ausgeblendete Nachricht in einem Ordner gespeichert sind
TOCTitle: Access solution-specific data stored as a hidden message in a folder
ms:assetid: bacf0562-1026-4c3b-87b0-4eaad5033592
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623414(v=office.15)
ms:contentKeyID: 55119861
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4a0a686327bb43b07773b149831107f51fcb4fa
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708144"
---
# <a name="access-solution-specific-data-stored-as-a-hidden-message-in-a-folder"></a>Zugreifen auf lösungsspezifische Daten, die als ausgeblendete Nachricht in einem Ordner gespeichert sind

Dieses Beispiel zeigt die Verwendung des [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) -Objekts zum Abrufen von Daten, die als ausgeblendete Nachricht einer bestimmten Nachrichtenklasse in einem Ordner gespeichert sind.

## <a name="example"></a>Beispiel

Das **StorageItem**-Objekt wird üblicherweise verwendet, um lösungsspezifische Daten auszublenden, die nicht programmgesteuert angezeigt werden können. In einer Exchange-Umgebung wird das **StorageItem**-Objekt zum Roaming von Lösungseinstellungen verwendet und um sicherzustellen, dass diese Einstellungen online und offline verfügbar sind. Sie können dem **StorageItem**-Objekt eine benutzerdefinierte Nachrichtenklasse zuweisen oder das Objekt durch den Betreff identifizieren.

Im folgenden Codebeispiel werden die XML-Daten abgerufen, die im Kalenderordner als ausgeblendete Nachricht mit der Nachrichtenklasse IPM.Configuration.WorkHours gespeichert sind. 

Das [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) -Objekt gibt die XML-Daten in Form eines Objekts zurück, das anstelle einer Zeichenkettendarstellung der XML-Daten einen Datenstrom enthält. Der Datenstrom wird im Codebeispiel mithilfe von **System.Text.Encoding.Ascii.GetString** in eine Zeichenfolge umgewandelt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.

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


## <a name="see-also"></a>Siehe auch

- [Folders](folders.md)

