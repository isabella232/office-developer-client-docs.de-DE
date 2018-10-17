---
title: Hinzufügen eines Ordners zur Ordnerliste
TOCTitle: Add a folder to the folder list
ms:assetid: f636a190-d966-4421-9977-0ead2bff5eee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184655(v=office.15)
ms:contentKeyID: 55119850
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: dc8ead207261cfd4835e230981d923211771de7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405525"
---
# <a name="add-a-folder-to-the-folder-list"></a>Hinzufügen eines Ordners zur Ordnerliste

In diesem Beispiel wird die Verwendung der [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\))-Methode erläutert, um einen Ordner zur Ordnerliste von Outlook hinzuzufügen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Im folgenden Codebeispiel ruft **AddMyNewFolder** die **Add**-Methode der [Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\))-Auflistung auf, um dem [Posteingang](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) in der Outlook-Ordnerliste ein **Folder**-Objekt hinzuzufügen, das einen Ordner namens „My New Folder“ darstellt. „My New Folder“ wird anschließend angezeigt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddMyNewFolder()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Folders folders = folder.Folders;
    try
    {
        Outlook.Folder newFolder = folders.Add(
            "My New Folder", Type.Missing)
            as Outlook.Folder;
        newFolder.Display();
    }
    catch
    {
        MessageBox.Show(
            "Could not add 'My New Folder'",
            "Add Folder",
            MessageBoxButtons.OK,
            MessageBoxIcon.Error);
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Ordner](folders.md)

