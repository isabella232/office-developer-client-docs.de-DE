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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349525"
---
# <a name="create-a-recurring-task"></a><span data-ttu-id="f1632-102">Erstellen eines periodischen Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f1632-102">Create a recurring task</span></span>

<span data-ttu-id="f1632-103">In diesem Beispiel wird eine wiederkehrende Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="f1632-103">This example creates a recurrent task.</span></span>

## <a name="example"></a><span data-ttu-id="f1632-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f1632-104">Example</span></span>

<span data-ttu-id="f1632-105">Dieser Code erstellt ein [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\))-Objekt und verwendet die [GetRecurrencePattern](https://msdn.microsoft.com/library/bb647080\(v=office.15\))-Methode von **TaskItem**, um aus der Aufgabe eine wiederkehrende Aufgabe zu machen.</span><span class="sxs-lookup"><span data-stu-id="f1632-105">This code sample creates a [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) object and uses the [GetRecurrencePattern](https://msdn.microsoft.com/library/bb647080\(v=office.15\)) method of the **TaskItem** to make the task a recurrent task.</span></span>

<span data-ttu-id="f1632-106">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="f1632-106">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="f1632-107">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f1632-107">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="f1632-108">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="f1632-108">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="f1632-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1632-109">See also</span></span>

- [<span data-ttu-id="f1632-110">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="f1632-110">Tasks</span></span>](tasks.md)

