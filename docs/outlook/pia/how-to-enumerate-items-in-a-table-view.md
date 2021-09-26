---
title: Auflisten der Elemente in einer Tabellenansicht
TOCTitle: Enumerate items in a table view
ms:assetid: c7d9a667-cfec-49c1-af7a-4c8063991588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184640(v=office.15)
ms:contentKeyID: 55119900
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1ff7ab9309388c2f83f843240dd6246490085c8b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583177"
---
# <a name="enumerate-items-in-a-table-view"></a>Auflisten der Elemente in einer Tabellenansicht

In diesem Beispiel werden Elemente in einer Tabellenansicht mit der [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\))-Methode aufgelistet.

## <a name="example"></a>Beispiel

Das folgende Codebeispiel ruft ein [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) -Objekt aus der aktuellen Ansicht des Posteingangsordners ab. Der aktuelle Ordner des aktiven Explorers wird auf den Posteingang festgelegt. Anschließend wird überprüft, ob es sich bei der aktuellen Ansicht des Posteingangs um eine Tabellenansicht handelt. Ist die aktuelle Ansicht eine Tabelle, wird im Codebeispiel die [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) -Methode aufgerufen und jedes durch jeweils eine Zeile im zurückgegebenen **Table**-Objekt dargestellte Element angezeigt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoViewGetTable()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder
    // for View.GetTable to work correctly.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType == 
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view = 
            inbox.CurrentView as Outlook.TableView;
        // No arguments needed for View.GetTable.
        Outlook.Table table = view.GetTable();
        Debug.WriteLine("View Count=" 
            + table.GetRowCount().ToString());
        while (!table.EndOfTable)
        {
            // First row in Table.
            Outlook.Row nextRow = table.GetNextRow();
            Debug.WriteLine(nextRow["Subject"]
                + " Modified: "
                + nextRow["LastModificationTime"]);
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Views](views.md)

