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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723026"
---
# <a name="add-or-remove-a-store"></a><span data-ttu-id="6668c-102">Hinzufügen oder Entfernen eines Speichers</span><span class="sxs-lookup"><span data-stu-id="6668c-102">Add or remove a store</span></span>

<span data-ttu-id="6668c-103">In diesem Beispiel wird veranschaulicht, wie ein Speicher in einem Profil hinzugefügt und entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="6668c-103">This example shows how to add and remove a store in a given profile.</span></span>

## <a name="example"></a><span data-ttu-id="6668c-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6668c-104">Example</span></span>

<span data-ttu-id="6668c-105">Das Codebeispiel zeigt das Hinzufügen und Entfernen eines Speichers in einem angegebenen Profil durch einen Aufruf der [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) -Methode bzw. der [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)) -Methode für das [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6668c-105">This code sample shows how to add and remove a store in a specified profile, by calling the [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) method and the [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)) method respectively on the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span>

<span data-ttu-id="6668c-106">In Outlook können Sie einen PST-Speicher nur programmatisch hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="6668c-106">In Outlook, you can add or remove a PST store only programmatically.</span></span> <span data-ttu-id="6668c-107">Das folgende Codebeispiel fügt einen Unicode-Speicher hinzu und platziert die PST-Datei am Standardspeicherort für PST-Dateien von Benutzern: Dokumente und Einstellungen\\\<Benutzername\>\\Lokale Einstellungen\\Anwendungsdaten\\Microsoft\\Outlook.</span><span class="sxs-lookup"><span data-stu-id="6668c-107">The following code sample adds a Unicode store and places the .pst file in the default location for user .pst files: Documents and Settings\\\<UserName\>\\Local Settings\\Application Data\\Microsoft\\Outlook.</span></span> <span data-ttu-id="6668c-108">Das Codebeispiel verwendet Environment.SpecialFolder.LocalApplicationData zum Abrufen des Pfads zum Ordner „Anwendungsdaten“ unter dem Ordner „Lokale Einstellungen“.</span><span class="sxs-lookup"><span data-stu-id="6668c-108">The code sample uses Environment.SpecialFolder.LocalApplicationData to retrieve the path to the Application Data folder under the Local Settings folder.</span></span> <span data-ttu-id="6668c-109">Nachdem Sie den Speicher hinzugefügt haben, wird er vom Codebeispiel entfernt.</span><span class="sxs-lookup"><span data-stu-id="6668c-109">Once the store has been added, the code sample removes the store.</span></span> <span data-ttu-id="6668c-110">Da die **RemoveStore**-Methode ein [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekt zum Entfernen des [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\))-Objekts erfordert, listet es die [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\))-Sammlung auf, um das **Store**-Objekt zu suchen, das soeben hinzugefügt wurde. Dies geschieht basierend auf der [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\))-Eigenschaft des **Store**-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6668c-110">Because the **RemoveStore** method requires a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object to remove the [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object, it enumerates the [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) collection to find the **Store** object that has just been added based on the [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) property of the **Store** object.</span></span>

<span data-ttu-id="6668c-p102">**RemoveStore** entfernt nur den Speicher aus dem aktuellen Profil. Die PST-Datei wird nicht aus dem Dateisystem gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6668c-p102">**RemoveStore** only removes the store from the current profile. It does not delete the .pst file from the file system.</span></span>

<span data-ttu-id="6668c-113">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="6668c-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="6668c-114">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6668c-114">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="6668c-115">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="6668c-115">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="6668c-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6668c-116">See also</span></span>

- [<span data-ttu-id="6668c-117">Stores</span><span class="sxs-lookup"><span data-stu-id="6668c-117">Stores</span></span>](stores.md)

