---
title: Erstellen eines Aufgabenelements
TOCTitle: Create a task item
ms:assetid: d458dd31-2771-4a3c-a713-13c7e4e02a74
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184644(v=office.15)
ms:contentKeyID: 55119894
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 467d715e0fca1adfd835b11c36889dff3dbf145d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406806"
---
# <a name="create-a-task-item"></a><span data-ttu-id="ab522-102">Erstellen eines Aufgabenelements</span><span class="sxs-lookup"><span data-stu-id="ab522-102">Create a task item</span></span>

<span data-ttu-id="ab522-103">Dieses Beispiel zeigt, wie Sie mithilfe der [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\))-Methode ein Aufgabenelement erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab522-103">This example shows how to create a task item by using the [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="ab522-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ab522-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ab522-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="ab522-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="ab522-106">Im folgenden Codebeispiel erstellt CreateToDoItemExample ein Aufgabenelement durch Aufrufen der **MarkAsTask**-Methode für das Element und anschließendes Speichern des Elements.</span><span class="sxs-lookup"><span data-stu-id="ab522-106">In the following code example, CreateToDoItemExample creates a to-do item by calling the **MarkAsTask** method on the item and then saving the item.</span></span> <span data-ttu-id="ab522-107">Im Beispiel wird das Element zur Nachverfolgung morgen markiert und eine Erinnerung für morgen um 10:00 Uhr wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ab522-107">The example marks the item for follow-up tomorrow and sets a reminder for tomorrow at 10:00 A.M.</span></span> <span data-ttu-id="ab522-108">Dabei kommen die [ReminderSet](https://msdn.microsoft.com/library/bb622600\(v=office.15\))- und [ReminderTime](https://msdn.microsoft.com/library/bb622803\(v=office.15\))-Eigenschaften zum Einsatz.</span><span class="sxs-lookup"><span data-stu-id="ab522-108">by using the [ReminderSet](https://msdn.microsoft.com/library/bb622600\(v=office.15\)) and [ReminderTime](https://msdn.microsoft.com/library/bb622803\(v=office.15\)) properties.</span></span> <span data-ttu-id="ab522-109">Im Beispiel wird das Element dann mithilfe der [Save()](https://msdn.microsoft.com/library/bb645518\(v=office.15\))-Methode gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ab522-109">The example then uses the [Save()](https://msdn.microsoft.com/library/bb645518\(v=office.15\)) method to save the item.</span></span>

<span data-ttu-id="ab522-110">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="ab522-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="ab522-111">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ab522-111">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="ab522-112">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ab522-112">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateToDoItemExample()
{
    // Date operations
    DateTime today = DateTime.Parse("10:00 AM");
    TimeSpan duration = TimeSpan.FromDays(1);
    DateTime tomorrow = today.Add(duration);
    Outlook.MailItem mail = Application.Session.
        GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Items.Find(
        "[MessageClass]='IPM.Note'") as Outlook.MailItem;
    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkTomorrow);
    mail.TaskStartDate = today;
    mail.ReminderSet = true;
    mail.ReminderTime = tomorrow;
    mail.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="ab522-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab522-113">See also</span></span>

- [<span data-ttu-id="ab522-114">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ab522-114">Tasks</span></span>](tasks.md)

