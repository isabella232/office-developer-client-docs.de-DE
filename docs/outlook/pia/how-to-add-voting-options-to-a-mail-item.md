---
title: Hinzufügen von Abstimmungsoptionen zu einem E-Mail-Element
TOCTitle: Add voting options to a mail item
ms:assetid: 0fb209a8-178d-411e-9551-0a72e041fd65
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424466(v=office.15)
ms:contentKeyID: 55119867
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3befe70363d1e2226b8a3a3a6ebb8db39aa2c6ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359724"
---
# <a name="add-voting-options-to-a-mail-item"></a><span data-ttu-id="0b571-102">Hinzufügen von Abstimmungsoptionen zu einem E-Mail-Element</span><span class="sxs-lookup"><span data-stu-id="0b571-102">Add voting options to a mail item</span></span>

<span data-ttu-id="0b571-103">In diesem Beispiel wird gezeigt, wie Sie mithilfe der [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\))-Eigenschaft des [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))-Objekts einer E-Mail-Nachricht Abstimmungsoptionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0b571-103">This example shows how to use the [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) property of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object to add voting options to an email message.</span></span>

## <a name="example"></a><span data-ttu-id="0b571-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0b571-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0b571-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="0b571-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="0b571-p101">Abstimmungsoptionen für Nachrichten dienen dazu, Nachrichtenempfängern eine Liste von Optionen anzuzeigen und ihre Antworten nachzuverfolgen. Legen Sie zum programmgesteuerten Erstellen von Abstimmungsoptionen für die **VotingOptions**-Eigenschaft eines **MailItem**-Objekts eine Zeichenfolge mit einer durch Semikolons getrennte Liste von Werten fest. Die Werte für die **VotingOptions**-Eigenschaft werden unter dem Befehl **Abstimmen** in der Gruppe **Antworten** im Menüband der empfangenen Nachricht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0b571-p101">Voting options on messages are used to give message recipients a list of choices and to track their responses. To create voting options programmatically, set a string that is a semicolon-delimited list of values for the **VotingOptions** property of a **MailItem** object. The values for the **VotingOptions** property will appear under the **Vote** command in the **Respond** group in the ribbon of the received message.</span></span>

<span data-ttu-id="0b571-109">Im folgenden Beispiel erstellt OrderPizza Abstimmungsoptionen in einer neuen E-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0b571-109">In the following example, OrderPizza creates voting options in a new mail message.</span></span> <span data-ttu-id="0b571-110">OrderPizza erstellt zunächst **MailItem**-Objekt und legt dann die **VotingOptions**-Eigenschaft auf „Cheese; Mushroom; Sausage; Combo; Veg Combo“ und die [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\))-Eigenschaft auf „Pizza Order“ fest.</span><span class="sxs-lookup"><span data-stu-id="0b571-110">OrderPizza first creates a **MailItem**, and then sets the **VotingOptions** property to “Cheese; Mushroom; Sausage; Combo; Veg Combo”, and the [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) property to “Pizza Order”.</span></span> <span data-ttu-id="0b571-111">Wenn die Nachricht „Pizza Order“ gesendet wird, werden die Abstimmungsoptionen für Empfänger angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0b571-111">When the “Pizza Order” message is sent, the voting options appear to recipients.</span></span> <span data-ttu-id="0b571-112">Für jede empfangene Antwort erhalten haben, wird die Wahl des Empfängers auf der Seite **Nachverfolgung** der Nachricht im Ordner „Gesendete Elemente“ des Absenders aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0b571-112">For each response received, the recipient’s choice will be tallied on the **Tracking** page of the message in the sender’s Sent Items folder.</span></span>

<span data-ttu-id="0b571-113">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="0b571-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="0b571-114">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0b571-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0b571-115">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="0b571-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void OrderPizza()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.CreateItem(
            Outlook.OlItemType.olMailItem);
        mail.VotingOptions = “Cheese; Mushroom; Sausage; Combo; Veg Combo;”
        mail.Subject = “Pizza Order”;
        mail.Display(false);
    }
```

## <a name="see-also"></a><span data-ttu-id="0b571-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b571-116">See also</span></span>

- [<span data-ttu-id="0b571-117">Mail</span><span class="sxs-lookup"><span data-stu-id="0b571-117">Mail</span></span>](mail.md)

