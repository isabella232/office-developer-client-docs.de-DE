---
title: Auswählen eines Ordners und Anzeigen von Ordnerinformationen
TOCTitle: Select a folder and display folder information
ms:assetid: 737b19bc-1efd-4ddb-86d0-72b3ab8eaf8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184616(v=office.15)
ms:contentKeyID: 55119859
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f0523a7d317b6fb12adf1dec4ede855ef7f6acfd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629277"
---
# <a name="select-a-folder-and-display-folder-information"></a>Auswählen eines Ordners und Anzeigen von Ordnerinformationen

Dieses Beispiel zeigt, wie Informationen zu einem Ordner, den ein Benutzer aus einer Liste angegebener Ordner auswählt, programmgesteuert angezeigt werden können.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Im folgenden Codebeispiel verwendet ShowFolderInfo die [PickFolder()](https://msdn.microsoft.com/library/bb623484\(v=office.15\))-Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\))-Objekts zum Anzeigen des Dialogfeldes **Ordner auswählen**, damit der Benutzer einen Ordner auswählt. Nach Auswahl des Ordners werden die folgenden Eigenschaften angezeigt: [EntryID](https://msdn.microsoft.com/library/bb646192\(v=office.15\)), [StoreID](https://msdn.microsoft.com/library/bb612609\(v=office.15\)), [UnReadItemCount](https://msdn.microsoft.com/library/bb610138\(v=office.15\)), [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)), [CurrentView](https://msdn.microsoft.com/library/bb612411\(v=office.15\)), [Name](https://msdn.microsoft.com/library/bb623727\(v=office.15\)) und [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)). Anschließend ruft das Beispiel die [GetFolderFromID](https://msdn.microsoft.com/library/bb647784\(v=office.15\))-Methode zum Erstellen eines neuen [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekts und zum Anzeigen des Ordners auf.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ShowFolderInfo()
{
    Outlook.Folder folder =
        Application.Session.PickFolder()
        as Outlook.Folder;
    if (folder != null)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Folder EntryID:");
        sb.AppendLine(folder.EntryID);
        sb.AppendLine();
        sb.AppendLine("Folder StoreID:");
        sb.AppendLine(folder.StoreID);
        sb.AppendLine();
        sb.AppendLine("Unread Item Count: "
            + folder.UnReadItemCount);
        sb.AppendLine("Default MessageClass: "
            + folder.DefaultMessageClass);
        sb.AppendLine("Current View: "
            + folder.CurrentView.Name);
        sb.AppendLine("Folder Path: "
            + folder.FolderPath);
        MessageBox.Show(sb.ToString(),
            "Folder Information",
            MessageBoxButtons.OK,
            MessageBoxIcon.Information);
        Outlook.Folder folderFromID =
            Application.Session.GetFolderFromID(
            folder.EntryID, folder.StoreID)
            as Outlook.Folder;
        folderFromID.Display();
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Folders](folders.md)

