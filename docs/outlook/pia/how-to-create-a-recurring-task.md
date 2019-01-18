---
title: Erstellen eines periodischen Vorgangs
TOCTitle: Create a recurring task
ms:assetid: bbca8527-79af-4c00-aae7-a1fd381e707c
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623455(v=office.15)
ms:contentKeyID: 55119932
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4fd2df68ef866008799a7206e7ae041e5bfd82a3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698260"
---
# <a name="create-a-recurring-task"></a>Erstellen eines periodischen Vorgangs

In diesem Beispiel wird eine wiederkehrende Aufgabe erstellt.

## <a name="example"></a>Beispiel

Dieser Code erstellt ein [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\))-Objekt und verwendet die [GetRecurrencePattern](https://msdn.microsoft.com/library/bb647080\(v=office.15\))-Methode von **TaskItem**, um aus der Aufgabe eine wiederkehrende Aufgabe zu machen.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateRecurringTask()
    Dim task As Outlook.TaskItem = CType(Application.CreateItem( _
        Outlook.OlItemType.olTaskItem), Outlook.TaskItem)
    task.Subject = "Tax Preparation"
    task.StartDate = DateTime.Parse("4/1/2007 8:00 AM")
    task.DueDate = DateTime.Parse("4/15/2007 8:00 AM")
    Dim pattern As Outlook.RecurrencePattern = _
        task.GetRecurrencePattern()
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearly
    pattern.PatternStartDate = DateTime.Parse("4/1/2007")
    pattern.NoEndDate = True
    task.ReminderSet = True
    task.ReminderTime = DateTime.Parse("4/1/2007 8:00 AM")
    task.Save()
End Sub
```


```csharp
private void CreateRecurringTask()
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
    task.Save();
}
```

## <a name="see-also"></a>Siehe auch

- [Aufgaben](tasks.md)

