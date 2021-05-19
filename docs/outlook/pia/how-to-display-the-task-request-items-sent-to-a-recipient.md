---
title: Anzeigen der an einen Empfänger gesendeten Aufgabeanfragenelemente
TOCTitle: Display the task request items sent to a recipient
ms:assetid: 167c3d52-67b5-467c-a7b6-e8cc96002b63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184591(v=office.15)
ms:contentKeyID: 55119930
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9ab5e830003fbfb64b44fc9e0d813c7a7c5163bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357421"
---
# <a name="display-the-task-request-items-sent-to-a-recipient"></a>Anzeigen der an einen Empfänger gesendeten Aufgabeanfragenelemente

In diesem Beispiel wird veranschaulicht, wie alle Elemente der Aufgabenanforderung angezeigt werden, die sich im Postfach eines Empfängers befinden.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Ein [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\))-Objekt stellt eine Anforderung dar, eine Aufgabe einem anderen Benutzer zuzuweisen. Das **TaskRequestItem**-Objekt wird erstellt, wenn das Element im Posteingang des Empfängers eingeht. Im nachstehenden Codebeispiel filtert ShowTaskRequests den Posteingang eines Empfängers, erstellt ein [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt und fügt eine Zeile für jeden Eintrag ein, für den Wert der [MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\))-Eigenschaft gleich **IPM.TaskRequest** ist. Der Betreff jeder Aufgabe im Posteingangsordner des Empfängers wird dann in die Ablaufverfolgungslistener der [Listener](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung geschrieben.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ShowTaskRequests()
{
    string filter = "[MessageClass] = 'IPM.TaskRequest'";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderInbox).GetTable
        (filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Aufgaben](tasks.md)

