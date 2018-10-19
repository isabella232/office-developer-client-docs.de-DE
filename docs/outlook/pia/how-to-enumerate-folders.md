---
title: Aufzählen von Ordnern
TOCTitle: Enumerate folders
ms:assetid: 564730f9-3da3-4eff-b207-64ac4fec632d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184607(v=office.15)
ms:contentKeyID: 55119855
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 91165754ccd86ebff07ec99e60f0ad1a167dea05
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406253"
---
# <a name="enumerate-folders"></a>Aufzählen von Ordnern

In diesem Beispiel wird gezeigt, wie Ordner durch das Durchlaufen einer Sammlung von Ordnern aufgeführt werden.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Im folgenden Codebeispiel wird durch die EnumerateFoldersInDefaultStore-Methode zuerst der Stammordner des Standardspeichers mithilfe der [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\))-Methode abgerufen. Dann folgt der Aufruf der EnumerateFolders-Methode über den Stammordner. EnumerateFolders übernimmt einen Stammordner und durchläuft die Ordner des Standardspeichers, den der Stammordner darstellt. EnumerateFolders verwendet zuerst die [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\))-Eigenschaft zum Abrufen der Unterordner des [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekts des Stamms. EnumerateFolders wird dann rekursiv aufgerufen, um alle Ordner der Hierarchie aufzuzählen. Abschließend schreibt EnumerateFolders die [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\))-Eigenschaft aller **Folder** in die Ablaufverfolgungslistener der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Sammlung.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateFoldersInDefaultStore()
{
    Outlook.Folder root =
        Application.Session.
        DefaultStore.GetRootFolder() as Outlook.Folder;
    EnumerateFolders(root);
}

// Uses recursion to enumerate Outlook subfolders.
private void EnumerateFolders(Outlook.Folder folder)
{
    Outlook.Folders childFolders =
        folder.Folders;
    if (childFolders.Count > 0)
    {
        foreach (Outlook.Folder childFolder in childFolders)
        {
            // Write the folder path.
            Debug.WriteLine(childFolder.FolderPath);
            // Call EnumerateFolders using childFolder.
            EnumerateFolders(childFolder);
        }
    }
}               
```

## <a name="see-also"></a>Siehe auch

- [Ordner](folders.md)

