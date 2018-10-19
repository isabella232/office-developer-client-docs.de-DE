---
title: Filtern und effizientes Aufzählen von Elementen in einem Ordner
TOCTitle: Filter and efficiently enumerate items in a folder
ms:assetid: efee7704-b7d9-4586-a72e-4e960ec1ffdb
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612664(v=office.15)
ms:contentKeyID: 55119884
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 01f0019d0f038cd1e9ea8fee7c85d0d2f18c4b47
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405672"
---
# <a name="filter-and-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="fc29a-102">Filtern und effizientes Aufzählen von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="fc29a-102">Filter and efficiently enumerate items in a folder</span></span>

<span data-ttu-id="fc29a-103">Dieses Beispiel zeigt die Verwendung des [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) -Objekts zum Filtern von Elementen im Posteingang, die Anlagen enthalten, und zum effizienten Aufzählen dieser Elemente mit ausgewählten Eigenschaften jedes Elements.</span><span class="sxs-lookup"><span data-stu-id="fc29a-103">This example shows how to use the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object to filter for items in the Inbox that have attachments, and efficiently enumerate such items, displaying selected properties for each item.</span></span>

## <a name="example"></a><span data-ttu-id="fc29a-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fc29a-104">Example</span></span>

<span data-ttu-id="fc29a-105">Das Codebeispiel gibt die Eigenschaft **PR\_HASATTACH** mit dem MAPI-Namespace an und verwendet die Eigenschaft zum Erstellen des ersten Filters in der [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\))-Methode im Posteingang.</span><span class="sxs-lookup"><span data-stu-id="fc29a-105">The code sample specifies the property **PR\_HASATTACH** with the MAPI namespace, and uses the property to create the initial filter in the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox.</span></span> <span data-ttu-id="fc29a-106">Ein **Table**-Objekt für einen Elementtyp weist Standardspalten auf, die bestimmte Eigenschaften dieses Elementtyps darstellen.</span><span class="sxs-lookup"><span data-stu-id="fc29a-106">A **Table** object for an item type has default columns representing certain properties of that item type.</span></span> <span data-ttu-id="fc29a-107">Zum Anpassen der Spalten wird in diesem Beispiel zunächst die [RemoveAll](https://msdn.microsoft.com/library/bb611528\(v=office.15\))-Methode in der [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\))-Auflistung dieser **Table** aufgerufen und dann die [Add](https://msdn.microsoft.com/library/bb652865\(v=office.15\))-Methode in der **Columns**-Auflistung, um die **EntryID**-, die **Subject**- und die **ReceivedTime**-Eigenschaft mithilfe der integrierten Eigenschaftennamen hinzuzufügen, wobei in der **ReceivedTime**-Spalte Werte in der lokalen Datums-/Uhrzeitdarstellung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="fc29a-107">To customize the columns, this example first calls the [RemoveAll](https://msdn.microsoft.com/library/bb611528\(v=office.15\)) method on the [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) collection of that **Table**, and then calls the [Add](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) method on the **Columns** collection to add the **EntryID**, **Subject**, and **ReceivedTime** properties using the built-in property names, with the **ReceivedTime** column storing values in local date-time representation.</span></span> 

<span data-ttu-id="fc29a-108">Anschließend ruft das Beispiel **Columns.Add** ein weiteres Mal auf, um die **ReceiveTime**-Eigenschaft hinzuzufügen, wobei deren MAPI-Namespace angegeben wird, damit diese Spalte den Wert als Datums-/Uhrzeitwert in koordinierter Weltzeit (UTC) speichert.</span><span class="sxs-lookup"><span data-stu-id="fc29a-108">The example then calls **Columns.Add** one more time to add the **ReceiveTime** property specifying its MAPI namespace so that this column will store the value as a Universal Coordinated Time (UTC) date-time value.</span></span> <span data-ttu-id="fc29a-109">Im Beispiel wird schließlich jedes Element in der Tabelle aufgeführt, wobei der Wert der vier Eigenschaften als Tabellenspalten angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fc29a-109">Finally, the example enumerates each item in the Table, displaying the value of each of the four properties specified as the table columns.</span></span>

<span data-ttu-id="fc29a-110">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="fc29a-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="fc29a-111">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fc29a-111">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="fc29a-112">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="fc29a-112">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="fc29a-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc29a-113">See also</span></span>

- [<span data-ttu-id="fc29a-114">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="fc29a-114">Search and Filter</span></span>](search-and-filter.md)

