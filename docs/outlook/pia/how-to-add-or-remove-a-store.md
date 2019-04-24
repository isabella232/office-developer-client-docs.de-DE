---
title: Hinzufügen oder Entfernen eines Speichers
TOCTitle: Add or remove a store
ms:assetid: db2930ec-ef99-4e31-86c5-820e8368e05f
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612380(v=office.15)
ms:contentKeyID: 55119895
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4346f3bf1b7bba1f26a34e1562997b4d043c8d49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359745"
---
# <a name="add-or-remove-a-store"></a>Hinzufügen oder Entfernen eines Speichers

In diesem Beispiel wird veranschaulicht, wie ein Speicher in einem Profil hinzugefügt und entfernt wird.

## <a name="example"></a>Beispiel

Das Codebeispiel zeigt das Hinzufügen und Entfernen eines Speichers in einem angegebenen Profil durch einen Aufruf der [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) -Methode bzw. der [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)) -Methode für das [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekt.

In Outlook können Sie einen PST-Speicher nur programmatisch hinzufügen oder entfernen. Das folgende Codebeispiel fügt einen Unicode-Speicher hinzu und platziert die PST-Datei am Standardspeicherort für PST-Dateien von Benutzern: Dokumente und Einstellungen\\\<Benutzername\>\\Lokale Einstellungen\\Anwendungsdaten\\Microsoft\\Outlook. Das Codebeispiel verwendet Environment.SpecialFolder.LocalApplicationData zum Abrufen des Pfads zum Ordner „Anwendungsdaten“ unter dem Ordner „Lokale Einstellungen“. Nachdem Sie den Speicher hinzugefügt haben, wird er vom Codebeispiel entfernt. Because the **RemoveStore** method requires a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object to remove the [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object, it enumerates the [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) collection to find the **Store** object that has just been added based on the [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) property of the **Store** object.

**RemoveStore** entfernt nur den Speicher aus dem aktuellen Profil. Die PST-Datei wird nicht aus dem Dateisystem gelöscht.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateUnicodePST()
    Dim path As String = Environment.GetFolderPath( _
        Environment.SpecialFolder.LocalApplicationData) _
        & "\Microsoft\Outlook\MyUnicodeStore.pst"
    Try
        Application.Session.AddStoreEx( _
            path, Outlook.OlStoreType.olStoreUnicode)
        Dim stores As Outlook.Stores = Application.Session.Stores
        For Each store As Outlook.Store In stores
            If store.FilePath = path Then
                Dim folder As Outlook.Folder = _
                    CType(store.GetRootFolder(), Outlook.Folder)
                ' Remove the store
                Application.Session.RemoveStore(folder)
            End If
        Next
    Catch ex As Exception
        Debug.WriteLine(ex.Message)
    End Try
End Sub
```


```csharp
private void CreateUnicodePST()
{
    string path = Environment.GetFolderPath(
        Environment.SpecialFolder.LocalApplicationData)
        + @"\Microsoft\Outlook\MyUnicodeStore.pst";
    try
    {
        Application.Session.AddStoreEx(
            path, Outlook.OlStoreType.olStoreUnicode);
        Outlook.Stores stores = Application.Session.Stores;
        foreach (Outlook.Store store in stores)
        {
            if (store.FilePath == path)
            {
               Outlook.Folder folder =
                    store.GetRootFolder() as Outlook.Folder;
               // Remove the store
               Application.Session.RemoveStore(folder);
            }
        }
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Stores](stores.md)

