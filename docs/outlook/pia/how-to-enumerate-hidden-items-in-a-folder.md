---
title: Aufzählen von ausgeblendeten Elementen in einem Ordner
TOCTitle: Enumerate hidden items in a folder
ms:assetid: dafad1fb-94ce-4584-b5d1-2de5fad2f72a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184645(v=office.15)
ms:contentKeyID: 55119888
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6508ea955ad74b49b5fef73352b4a1706d8e338c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713198"
---
# <a name="enumerate-hidden-items-in-a-folder"></a>Aufzählen von ausgeblendeten Elementen in einem Ordner

Dieses Beispiel zeigt, wie Sie ausgeblendete Elemente in einem Ordner suchen und aufzählen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Ein Feature des [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekts, das eine Gruppe von Elementen in einem Ordner darstellt, besteht darin, dass es ausgeblendete Elemente aufweisen kann. Wenn ausgeblendete Elemente in einem Ordner zurückgegeben werden sollen, legen Sie den *TableContents*-Parameter in der [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\))-Methode des [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\))-Objekts auf [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)) fest. Im folgenden Codebeispiel ruft TableForInboxHiddenItems die ausgeblendeten Elemente eines Posteingangsordners ab und schreibt die Werte der [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\))- und der [MessageClass](https://msdn.microsoft.com/library/bb645845\(v=office.15\))-Eigenschaft für jedes ausgeblendete Element in die Listener der Ablaufverfolgung für die [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableForInboxHiddenItems()
{
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with OlTableContents.olHiddenItems
    Outlook.Table table =
        folder.GetTable("",
        Outlook.OlTableContents.olHiddenItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        // Test for null subject
        if (nextRow["Subject"] == null)
        {
            Debug.WriteLine(nextRow["MessageClass"]);
        }
        else
        {
            Debug.WriteLine(nextRow["Subject"] + " "
                + nextRow["MessageClass"]);
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

-[Suchen und Filtern](search-and-filter.md)

