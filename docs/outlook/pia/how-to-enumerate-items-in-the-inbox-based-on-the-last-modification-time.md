---
title: Aufzählen der Elemente im Posteingang basierend auf dem Zeitpunkt der letzten Änderung
TOCTitle: Enumerate items in the Inbox based on the last modification time
ms:assetid: 93a25143-def6-4832-bac2-3744558c2736
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184626(v=office.15)
ms:contentKeyID: 55119920
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0a568209caf172fbab26af1441ba7c208562ae19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320356"
---
# <a name="enumerate-items-in-the-inbox-based-on-the-last-modification-time"></a>Aufzählen der Elemente im Posteingang basierend auf dem Zeitpunkt der letzten Änderung

Dieses Beispiel zeigt das Aufzählen der Elemente im Posteingangsordner basierend auf dem Zeitpunkt der letzten Änderung.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Das [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt repräsentiert eine Gruppe von Elementen aus dem [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))- oder [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\))-Objekt. Um ein **Table**-Objekt abzurufen, rufen Sie die [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\))-Methode in einem **Folder**- oder **Search**-Objekt auf. Jedes Element in dem zurückgegebenen **Table**-Objekt enthält nur eine Standarduntermenge der Eigenschaften des Elements. Jedes [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\))-Objekt kann als ein Element im Ordner betrachtet werden und jedes [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\))-Objekt als eine Eigenschaft eines Elements. Das Entfernen, Hinzufügen oder Ändern von Zeilen wird im **Table**-Objekt nicht unterstützt. Zum Auflisten der Elemente in einer **Table** prüfen Sie zuerst mithilfe der [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) -Eigenschaft, ob die aktuelle Position das Ende der Tabelle ist. Wenn **EndOfTable** den Wert **false** zurückgibt, verwenden Sie die [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) -Methode, um ein **Row**-Objekt zurückzugeben, das eine Standardanzahl von **Column**-Objekten enthält. Sie durchlaufen das **Table**-Objekt weiterhin vorwärts, indem Sie **GetNextRow** aufrufen, bis **EndOfTable** **true** zurückgibt.

Im folgenden Codebeispiel ruft DemoTableForInbox ein **Table**-Objekt für den Posteingangsordner ab, sortiert das **Table**-Objekt mithilfe der **LastModificationTime**-Eigenschaft und der [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\))-Methode und durchläuft die Tabelle, um den Betreff jedes Elements in die Listener der Ablaufverfolgung für die [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung zu schreiben.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTableForInbox()
{
    //Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    //Obtain Table using defaults
    Outlook.Table table =
        folder.GetTable(Type.Missing, Type.Missing);
    table.Sort("LastModificationTime",
        Outlook.OlSortOrder.olDescending);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Suchen und Filtern](search-and-filter.md)

