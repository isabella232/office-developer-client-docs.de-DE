---
title: Verwenden von Arrays zum effizienten Aufzählen von Elementen in einem Ordner
TOCTitle: Use arrays to efficiently enumerate items in a folder
ms:assetid: 05a73225-ad0d-4d52-90b6-448d220348df
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184588(v=office.15)
ms:contentKeyID: 55119885
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: dbe2852de11c34401e1653d8e2b0b25d36e19b37
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560466"
---
# <a name="use-arrays-to-efficiently-enumerate-items-in-a-folder"></a>Verwenden von Arrays zum effizienten Aufzählen von Elementen in einem Ordner

In diesem Beispiel wird gezeigt, wie Elemente in einem [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekt mithilfe der [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\))-Methode effizient aufgezählt werden.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Im folgenden Codebeispiel ruft DemoGetArrayForTable mit der [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\))-Methode ein [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt aus einem **Folder**-Objekt ab. DemoGetArrayForTable gibt anschließend mithilfe der **GetArray**-Methode ein [Array](https://msdn.microsoft.com/library/system.array.aspx)-Objekt zurück, das Elemente für jede Zeile in der Tabelle enthält. Das zurückgegebene **Array**-Objekt ist ein zweidimensionales Array, das eine Gruppe von Zeilen- und Werten aus der **Tabelle** darstellt. Das Array ist nullbasiert (nicht einsbasiert wie bei Outlook-Auflistungen). Nach Abrufen des **Array**-Objekts verwendet der Code eine for-Schleife zum Auflisten der Tabelle.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoGetArrayForTable()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Table table =
        folder.GetTable("", Outlook.OlTableContents.olUserItems);
    Array tableArray = table.GetArray(table.GetRowCount()) as Array;
    for (int i = 0; i <= tableArray.GetUpperBound(0); i++)
    {
        for (int j = 0; j <= tableArray.GetUpperBound(1); j++)
        {
            Debug.WriteLine(tableArray.GetValue(i, j));
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Suchen und Filtern](search-and-filter.md)

