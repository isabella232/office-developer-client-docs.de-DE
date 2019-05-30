---
title: Abrufen der E-Mail-Adresse eines Empfängers
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184647(v=office.15)
ms:contentKeyID: 55119879
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5d145dadd974b6608da29cdf85a4624d6c452eb8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542576"
---
# <a name="get-the-email-address-of-a-recipient"></a><span data-ttu-id="b8451-102">Abrufen der E-Mail-Adresse eines Empfängers</span><span class="sxs-lookup"><span data-stu-id="b8451-102">Get the email address of a recipient</span></span>

<span data-ttu-id="b8451-103">In diesem Beispiel wird gezeigt, wie die SMTP-Adresse (Simple Mail Transfer Protocol) eines Empfängers abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b8451-103">This example shows how to get the Simple Mail Transfer Protocol (SMTP) address of a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="b8451-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b8451-104">Example</span></span>

<span data-ttu-id="b8451-105">Im folgenden Codebeispiel verwendet die GetSMTPAddressForRecipients-Methode ein [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))-Objekt als Eingabeargument und zeigt dann die SMTP-Adresse jedes Empfängers für das E-Mail-Element an.</span><span class="sxs-lookup"><span data-stu-id="b8451-105">In the following the code example, the GetSMTPAddressForRecipients method takes a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object as an input argument and then displays the SMTP address of each recipient for that mail item.</span></span> <span data-ttu-id="b8451-106">Die Methode ruft zuerst die [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\))-Auflistung ab, die den Satz von Empfängern darstellt, die für das E-Mail-Element angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="b8451-106">The method first retrieves the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection that represents the set of recipients specified for the mail item.</span></span> <span data-ttu-id="b8451-107">Für jedes [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) -Objekt in der **Recipients**-Auflistung ruft die Methode dann das [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) -Objekt ab, das diesem **Recipient**-Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="b8451-107">For each [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) in that **Recipients** collection, the method then obtains the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object that corresponds to that **Recipient** object.</span></span> <span data-ttu-id="b8451-108">Schließlich verwendet die Methode die [propertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) -Eigenschaft, um den Wert der MAPI-Eigenschaft http://schemas.microsoft.com/mapi/proptag/0x39FE001Eabzurufen, die der[PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))-Eigenschaft ( **\_PR SMTP\_Address** ) des Empfängers zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b8451-108">Finally, the method uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) property to get the value of the MAPI property http://schemas.microsoft.com/mapi/proptag/0x39FE001E, which maps to the **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) property of the recipient.</span></span>

<span data-ttu-id="b8451-109">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="b8451-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="b8451-110">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b8451-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b8451-111">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="b8451-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetSMTPAddressForRecipients(Outlook.MailItem mail)
{
    const string PR_SMTP_ADDRESS =
        "http://schemas.microsoft.com/mapi/proptag/0x39FE001E";
    Outlook.Recipients recips = mail.Recipients;
    foreach (Outlook.Recipient recip in recips)
    {
        Outlook.PropertyAccessor pa = recip.PropertyAccessor;
        string smtpAddress =
            pa.GetProperty(PR_SMTP_ADDRESS).ToString();
        Debug.WriteLine(recip.Name + " SMTP=" + smtpAddress);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="b8451-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8451-112">See also</span></span>

- [<span data-ttu-id="b8451-113">Empfänger</span><span class="sxs-lookup"><span data-stu-id="b8451-113">Recipients</span></span>](recipients.md)

