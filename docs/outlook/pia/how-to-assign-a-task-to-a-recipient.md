---
title: Zuordnen einer Aufgabe zu einem Empfänger
TOCTitle: Assign a task to a recipient
ms:assetid: c6be97a7-de3f-43e5-9111-534d0f04e986
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184639(v=office.15)
ms:contentKeyID: 55119929
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ba189b90468fdf967f4849cf0b1304afde0948f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616383"
---
# <a name="assign-a-task-to-a-recipient"></a>Zuordnen einer Aufgabe zu einem Empfänger

In diesem Beispiel wird gezeigt, wie Sie eine Aufgabe erstellen und einem Empfänger zuordnen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Im folgenden Codebeispiel erstellt AssignTaskExample ein [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\))-Objekt und gibt die Werte für die [Subject](https://msdn.microsoft.com/library/bb624148\(v=office.15\))-, die [StartDate](https://msdn.microsoft.com/library/bb643988\(v=office.15\))- und die [DueDate](https://msdn.microsoft.com/library/bb612307\(v=office.15\))-Eigenschaft an. Die [Assign()](https://msdn.microsoft.com/library/bb644565\(v=office.15\))-Methode gibt an, dass die Aufgabe eine zugewiesene Aufgabe ist. Nachdem ein [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\))-Objekt zu **TaskItem** mithilfe der [Add(String)](https://msdn.microsoft.com/library/bb612668\(v=office.15\))-Methode hinzugefügt wurde, sendet die [Send()](https://msdn.microsoft.com/library/bb646608\(v=office.15\))-Methode die Aufgabe an den Empfänger.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AssignTaskExample()
{
    Outlook.TaskItem task = Application.CreateItem(
        Outlook.OlItemType.olTaskItem) as Outlook.TaskItem;
    task.Subject = "Tax Preparation";
    task.StartDate = DateTime.Parse("4/1/2007 8:00 AM");
    task.DueDate = DateTime.Parse("4/15/2007 8:00 AM");
    Outlook.RecurrencePattern pattern =
        task.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearly;
    pattern.PatternStartDate = DateTime.Parse("4/1/2007");
    pattern.NoEndDate = true;
    task.ReminderSet = true;
    task.ReminderTime = DateTime.Parse("4/1/2007 8:00 AM");
    task.Assign();
    task.Recipients.Add("accountant@example.com");
    task.Recipients.ResolveAll();
    task.Send();
}
```

## <a name="see-also"></a>Siehe auch

- [Aufgaben](tasks.md)

