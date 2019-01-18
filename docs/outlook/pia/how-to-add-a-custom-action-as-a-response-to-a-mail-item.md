---
title: Hinzufügen einer benutzerdefinierten Aktion als Antwort auf ein E-Mail-Element
TOCTitle: Add a custom action as a response to a mail item
ms:assetid: 99e8ba6b-9c47-4b10-968b-436b08d199ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424474(v=office.15)
ms:contentKeyID: 55119870
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6a82b02d357f86ca37d3ec4987ea6323d6d59cb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722578"
---
# <a name="add-a-custom-action-as-a-response-to-a-mail-item"></a><span data-ttu-id="6c2f5-102">Hinzufügen einer benutzerdefinierten Aktion als Antwort auf ein E-Mail-Element</span><span class="sxs-lookup"><span data-stu-id="6c2f5-102">Add a custom action as a response to a mail item</span></span>

<span data-ttu-id="6c2f5-103">In diesem Beispiel wird gezeigt, wie Sie mithilfe der [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\))-Methode der [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\))-Auflistung benutzerdefinierte Aktionen als Antwort auf ein E-Mail-Element hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="6c2f5-103">This example shows how to add custom actions as a response to an email item by using the [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) method of the [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)) collection.</span></span>

## <a name="example"></a><span data-ttu-id="6c2f5-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6c2f5-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="6c2f5-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="6c2f5-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="6c2f5-106">Sie können benutzerdefinierte Aktionen programmgesteuert so erstellen, dass sie in einer E-Mail-Antwort im Menüband auf der Registerkarte **Nachricht** in der Gruppe **Aktionen** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6c2f5-106">You can create custom actions programmatically to appear on the ribbon in the **Actions** group on the **Message** tab in an email response.</span></span> <span data-ttu-id="6c2f5-107">Im folgenden Codebeispiel wird mithilfe von ReplyWithVoiceMail eine benutzerdefinierte Aktion namens „Reply with Voice Mail“ erstellt und der Inspektor-Befehlsleiste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6c2f5-107">In the following code example, ReplyWithVoiceMail creates and adds a custom action named “Reply with Voice Mail” to the inspector command bar.</span></span> <span data-ttu-id="6c2f5-108">ReplyWithVoiceMail ruft zuerst ein [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\))-Objekt ab und erstellt dann durch Aufrufen der **Add**-Methode der **Actions**-Auflistung, die dem **MailItem** zugeordnet ist, ein [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\))-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6c2f5-108">ReplyWithVoiceMail first gets a [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) object and then creates an [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) object by calling the **Add** method of the **Actions** collection that is associated with the **MailItem**.</span></span> <span data-ttu-id="6c2f5-109">Anschließend wird die [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) -Eigenschaft des **Action**-Objekts auf „Reply with Voice Mail“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c2f5-109">It then sets the [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) property of the **Action** object to “Reply with Voice Mail”.</span></span> <span data-ttu-id="6c2f5-110">Auch die [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\))-, die [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\))-, die [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\))- und die [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\))-Eigenschaft werden festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c2f5-110">The [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)), [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)), [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)), and [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)) properties are also set.</span></span> <span data-ttu-id="6c2f5-111">Schließlich wird das **MailItem** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6c2f5-111">Finally, the **MailItem**is saved.</span></span>


> [!NOTE]
> <span data-ttu-id="6c2f5-112">Mit dem Outlook-Formular-Designer können Sie auch benutzerdefinierte Aktionen zur Entwurfszeit hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6c2f5-112">You can also add custom actions at design time by using the Outlook Forms Designer.</span></span>


<span data-ttu-id="6c2f5-113">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="6c2f5-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="6c2f5-114">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6c2f5-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="6c2f5-115">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="6c2f5-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void ReplyWithVoiceMail()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.ActiveInspector().CurrentItem;
        Outlook.Action action = mail.Actions.Add();
        action.Name = “Reply with Voice Mail”;
        action.ReplyStyle = Outlook.OlActionReplyStyle.olUserPreference;
        action.ResponseStyle = Outlook.OlActionResponseStyle.olOpen;
        action.CopyLike = Outlook.OlActionCopyLike.olReply;
        action.MessageClass = “IPM.Post.Voice Message”;
        mail.Save();
    }
```

## <a name="see-also"></a><span data-ttu-id="6c2f5-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c2f5-116">See also</span></span>

- [<span data-ttu-id="6c2f5-117">Mail</span><span class="sxs-lookup"><span data-stu-id="6c2f5-117">Mail</span></span>](mail.md)

