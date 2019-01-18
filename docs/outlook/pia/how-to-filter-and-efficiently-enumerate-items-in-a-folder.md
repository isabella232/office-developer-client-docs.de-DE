---
title: Filtern und effizientes Aufzählen von Elementen in einem Ordner
TOCTitle: Filter and efficiently enumerate items in a folder
ms:assetid: efee7704-b7d9-4586-a72e-4e960ec1ffdb
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612664(v=office.15)
ms:contentKeyID: 55119884
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 35215c24a9b953bf8406b268a6169abbd536202b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705617"
---
# <a name="filter-and-efficiently-enumerate-items-in-a-folder"></a>Filtern und effizientes Aufzählen von Elementen in einem Ordner

Dieses Beispiel zeigt die Verwendung des [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) -Objekts zum Filtern von Elementen im Posteingang, die Anlagen enthalten, und zum effizienten Aufzählen dieser Elemente mit ausgewählten Eigenschaften jedes Elements.

## <a name="example"></a>Beispiel

Das Codebeispiel gibt die Eigenschaft **PR\_HASATTACH** mit dem MAPI-Namespace an und verwendet die Eigenschaft zum Erstellen des ersten Filters in der [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\))-Methode im Posteingang. Ein **Table**-Objekt für einen Elementtyp weist Standardspalten auf, die bestimmte Eigenschaften dieses Elementtyps darstellen. Zum Anpassen der Spalten wird in diesem Beispiel zunächst die [RemoveAll](https://msdn.microsoft.com/library/bb611528\(v=office.15\))-Methode in der [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\))-Auflistung dieser **Table** aufgerufen und dann die [Add](https://msdn.microsoft.com/library/bb652865\(v=office.15\))-Methode in der **Columns**-Auflistung, um die **EntryID**-, die **Subject**- und die **ReceivedTime**-Eigenschaft mithilfe der integrierten Eigenschaftennamen hinzuzufügen, wobei in der **ReceivedTime**-Spalte Werte in der lokalen Datums-/Uhrzeitdarstellung gespeichert werden. 

Anschließend ruft das Beispiel **Columns.Add** ein weiteres Mal auf, um die **ReceiveTime**-Eigenschaft hinzuzufügen, wobei deren MAPI-Namespace angegeben wird, damit diese Spalte den Wert als Datums-/Uhrzeitwert in koordinierter Weltzeit (UTC) speichert. Im Beispiel wird schließlich jedes Element in der Tabelle aufgeführt, wobei der Wert der vier Eigenschaften als Tabellenspalten angegeben werden.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoTableColumns()
    Const PR_HAS_ATTACH As String = _
        "https://schemas.microsoft.com/mapi/proptag/0x0E1B000B"
    ' Obtain Inbox
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderInbox), _
        Outlook.Folder)
    ' Create filter
    Dim filter As String = "@SQL=" & Chr(34) _
        & PR_HAS_ATTACH & Chr(34) & " = 1"
    Dim table As Outlook.Table = _
        folder.GetTable(filter, _
        Outlook.OlTableContents.olUserItems)
    ' Remove default columns
    table.Columns.RemoveAll()
    ' Add using built-in name
    table.Columns.Add("EntryID")
    table.Columns.Add("Subject")
    table.Columns.Add("ReceivedTime")
    table.Sort("ReceivedTime", Outlook.OlSortOrder.olDescending)
    ' Add using namespace
    ' Date received
    table.Columns.Add( _
        "urn:schemas:httpmail:datereceived")
    While Not (table.EndOfTable)
        Dim nextRow As Outlook.Row = table.GetNextRow()
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(nextRow("Subject").ToString())
        ' Reference column by name 
        sb.AppendLine("Received (Local): " _
            & nextRow("ReceivedTime").ToString())
        ' Reference column by index
        sb.AppendLine("Received (UTC): " & nextRow(4).ToString())
        sb.AppendLine()
        Debug.WriteLine(sb.ToString())
    End While
End Sub
```


```csharp
private void DemoTableColumns()
{
    const string PR_HAS_ATTACH =
        "https://schemas.microsoft.com/mapi/proptag/0x0E1B000B";
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Create filter
    string filter = "@SQL=" + "\""
        + PR_HAS_ATTACH + "\"" + " = 1";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    // Remove default columns
    table.Columns.RemoveAll();
    // Add using built-in name
    table.Columns.Add("EntryID");
    table.Columns.Add("Subject");
    table.Columns.Add("ReceivedTime");
    table.Sort("ReceivedTime", Outlook.OlSortOrder.olDescending);
    // Add using namespace
    // Date received
    table.Columns.Add(
        "urn:schemas:httpmail:datereceived");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(nextRow["Subject"].ToString());
        // Reference column by name 
        sb.AppendLine("Received (Local): "
            + nextRow["ReceivedTime"]);
        // Reference column by index
        sb.AppendLine("Received (UTC): " + nextRow[4]);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Suchen und Filtern](search-and-filter.md)

