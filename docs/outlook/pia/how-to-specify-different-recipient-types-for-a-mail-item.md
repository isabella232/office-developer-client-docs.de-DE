---
title: Angeben verschiedener Empfängertypen für ein E-Mail-Element
TOCTitle: Specify different recipient types for a mail item
ms:assetid: 2a3ace9f-627c-4fdd-b182-afc1b53af85b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184598(v=office.15)
ms:contentKeyID: 55119871
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf61a7fbb470291eae448a93c80866112c41407a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335511"
---
# <a name="specify-different-recipient-types-for-a-mail-item"></a><span data-ttu-id="59433-102">Angeben verschiedener Empfängertypen für ein E-Mail-Element</span><span class="sxs-lookup"><span data-stu-id="59433-102">Specify different recipient types for a mail item</span></span>

<span data-ttu-id="59433-103">Dieses Beispiel zeigt, wie Sie programmgesteuert verschiedene Empfängertypen („An“, „Cc“ oder „Bcc“) für ein E-Mail-Element festlegen.</span><span class="sxs-lookup"><span data-stu-id="59433-103">This example shows how to programmatically set different recipient types (To, Cc, or Bcc) for a mail item.</span></span>

## <a name="example"></a><span data-ttu-id="59433-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="59433-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="59433-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="59433-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="59433-106">Im folgenden Codebeispiel wird gezeigt, wie Sie angeben, ob ein Empfänger eines [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))-Objekts ein Empfänger vom Typ „An“, „Cc“ oder „Bcc“ ist.</span><span class="sxs-lookup"><span data-stu-id="59433-106">The following code example illustrates how to specify whether a recipient of a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object is a To, Cc, or Bcc recipient.</span></span> <span data-ttu-id="59433-107">SetRecipientTypeForMail erstellt ein **MailItem**-Objekt, fügt drei [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\))-Objekte zur [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\))-Sammlung der **MailItem**-Objekte hinzu und legt dann die [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\))-Eigenschaft jedes **Recipient**-Objekts auf einen Wert aus der [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\))-Aufzählung fest.</span><span class="sxs-lookup"><span data-stu-id="59433-107">SetRecipientTypeForMail creates a **MailItem** object, adds three [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) objects to the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection of the **MailItem**, and then sets the [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) property of each **Recipient** object to a value from the [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)) enumeration.</span></span>


> [!NOTE]
> <span data-ttu-id="59433-108">Die **Type**-Eigenschaft des **Recipient**-Objekts ist ein int-Typ und steht nicht mit einer Aufzählung eines bestimmten Empfängertypen im Zusammenhang.</span><span class="sxs-lookup"><span data-stu-id="59433-108">The **Type** property of the **Recipient** object is an int type and does not correlate to a specific recipient type enumeration.</span></span>

<span data-ttu-id="59433-109">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="59433-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="59433-110">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="59433-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="59433-111">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="59433-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void SetRecipientTypeForMail()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Sample Message";
    Outlook.Recipient recipTo =
        mail.Recipients.Add("someone@example.com");
    recipTo.Type = (int)Outlook.OlMailRecipientType.olTo;
    Outlook.Recipient recipCc =
        mail.Recipients.Add("someonecc@example.com");
    recipCc.Type = (int)Outlook.OlMailRecipientType.olCC;
    Outlook.Recipient recipBcc =
        mail.Recipients.Add("someonebcc@example.com");
    recipBcc.Type = (int)Outlook.OlMailRecipientType.olBCC;
    mail.Recipients.ResolveAll();
    mail.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="59433-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59433-112">See also</span></span>

- [<span data-ttu-id="59433-113">Mail</span><span class="sxs-lookup"><span data-stu-id="59433-113">Mail</span></span>](mail.md)

