---
title: Abrufen eines Ordners basierend auf seinem Ordnerpfad
TOCTitle: Get a folder based on its folder path
ms:assetid: 613f2209-667c-48f0-82cf-86e3c9a24cb4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184612(v=office.15)
ms:contentKeyID: 55119858
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b418cda3f689182cb7133af22e0f2fdc6ba834c2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407142"
---
# <a name="get-a-folder-based-on-its-folder-path"></a>Abrufen eines Ordners basierend auf seinem Ordnerpfad

In diesem Beispiel wird ein Ordnerpfad verwendet und der zugehörige Ordner abgerufen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Im folgenden Codebeispiel verwendet die GetKeyContacts-Methode die [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\))-Eigenschaft zum Abrufen des Ordnerpfads des Ordners "Kontakte\\Wichtige Kontakte". Die GetFolder-Methode wird dann mithilfe der [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\))-Eigenschaft als Argument aufgerufen. Wenn GetFolder einen Ordner zurückgibt, wird eine Meldung angezeigt, die besagt, dass die wichtigen Kontakte gefunden wurden. Die GetFolder-Methode übernimmt den Pfad zum Ordner und gibt das richtige [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekt zurück. Hierzu wird die **FolderPath**-Eigenschaft in einen string-Array geteilt und dieser dazu verwendet, das richtige **Folder**-Objekt zu finden, indem die **FolderPath**-Eigenschaft von oben an durchsucht wird. Wenn der angegebene Ordner nicht gefunden wird, gibt GetFolder einen Null-Verweis zurück.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetKeyContacts()
{
    string folderPath =
        Application.Session.
        DefaultStore.GetRootFolder().FolderPath
        + @"\Contacts\Key Contacts";
    Outlook.Folder folder = GetFolder(folderPath);
    if (folder != null)
    {
        //Work with folder here
        Debug.WriteLine("Found Key Contacts");
    }
}

// Returns Folder object based on folder path
private Outlook.Folder GetFolder(string folderPath)
{
    Outlook.Folder folder;
    string backslash = @"\";
    try
    {
        if (folderPath.StartsWith(@"\\"))
        {
            folderPath = folderPath.Remove(0, 2);
        }
        String[] folders =
            folderPath.Split(backslash.ToCharArray());
        folder =
            Application.Session.Folders[folders[0]]
            as Outlook.Folder;
        if (folder != null)
        {
            for (int i = 1; i <= folders.GetUpperBound(0); i++)
            {
                Outlook.Folders subFolders = folder.Folders;
                folder = subFolders[folders[i]]
                    as Outlook.Folder;
                if (folder == null)
                {
                    return null;
                }
            }
        }
        return folder;
    }
    catch { return null; }
}        
```

## <a name="see-also"></a>Siehe auch

- [Ordner](folders.md)

