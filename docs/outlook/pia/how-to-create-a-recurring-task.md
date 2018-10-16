---
title: Erstellen eines periodischen Vorgangs
TOCTitle: Create a recurring task
ms:assetid: bbca8527-79af-4c00-aae7-a1fd381e707c
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623455(v=office.15)
ms:contentKeyID: 55119932
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 6a9308e42ebaea0bcd07066a31bab7eb7a768604
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405805"
---
# <a name="create-a-recurring-task"></a><span data-ttu-id="08d5a-102">Erstellen eines periodischen Vorgangs</span><span class="sxs-lookup"><span data-stu-id="08d5a-102">Create a recurring task</span></span>

<span data-ttu-id="08d5a-103">In diesem Beispiel wird eine wiederkehrende Aufgabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="08d5a-103">This example creates a recurrent task.</span></span>

## <a name="example"></a><span data-ttu-id="08d5a-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="08d5a-104">Example</span></span>

<span data-ttu-id="08d5a-105">Dieser Code erstellt ein [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\))-Objekt und verwendet die [GetRecurrencePattern](https://msdn.microsoft.com/library/bb647080\(v=office.15\))-Methode von **TaskItem**, um aus der Aufgabe eine wiederkehrende Aufgabe zu machen.</span><span class="sxs-lookup"><span data-stu-id="08d5a-105">This code sample creates a [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) object and uses the [GetRecurrencePattern](https://msdn.microsoft.com/library/bb647080\(v=office.15\)) method of the **TaskItem** to make the task a recurrent task.</span></span>

<span data-ttu-id="08d5a-106">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="08d5a-106">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="08d5a-107">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="08d5a-107">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="08d5a-108">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="08d5a-108">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="08d5a-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08d5a-109">See also</span></span>

- [<span data-ttu-id="08d5a-110">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="08d5a-110">Tasks</span></span>](tasks.md)

