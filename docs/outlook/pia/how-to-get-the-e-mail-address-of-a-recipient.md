---
title: Abrufen der E-Mail-Adresse eines Empfängers
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-the-e-mail-address-of-a-recipient?redirectedfrom=MSDN
ms:contentKeyID: 55119879
ms.date: 12/03/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8957cbc92414b0cdac442167a5c9ea025ce318cb
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819336"
---
# <a name="get-the-email-address-of-a-recipient"></a><span data-ttu-id="9db5f-102">Abrufen der E-Mail-Adresse eines Empfängers</span><span class="sxs-lookup"><span data-stu-id="9db5f-102">Get the email address of a recipient</span></span>

<span data-ttu-id="9db5f-103">In diesem Beispiel wird gezeigt, wie die SMTP-Adresse (Simple Mail Transfer Protocol) eines Empfängers abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9db5f-103">This example shows how to get the Simple Mail Transfer Protocol (SMTP) address of a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="9db5f-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9db5f-104">Example</span></span>

<span data-ttu-id="9db5f-105">Im folgenden Codebeispiel verwendet die GetSMTPAddressForRecipients-Methode ein [MailItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mailitem?redirectedfrom=MSDN&view=outlook-pia)-Objekt als Eingabeargument und zeigt dann die SMTP-Adresse jedes Empfängers für das E-Mail-Element an.</span><span class="sxs-lookup"><span data-stu-id="9db5f-105">In the following the code example, the GetSMTPAddressForRecipients method takes a [MailItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mailitem?redirectedfrom=MSDN&view=outlook-pia) object as an input argument and then displays the SMTP address of each recipient for that mail item.</span></span> <span data-ttu-id="9db5f-106">Die Methode ruft zuerst die [Recipients](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipients?redirectedfrom=MSDN&view=outlook-pia)-Auflistung ab, die den Satz von Empfängern darstellt, die für das E-Mail-Element angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="9db5f-106">The method first retrieves the [Recipients](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipients?redirectedfrom=MSDN&view=outlook-pia) collection that represents the set of recipients specified for the mail item.</span></span> <span data-ttu-id="9db5f-107">Für jeden [Empfänger](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient?redirectedfrom=MSDN&view=outlook-pia) in dieser **Recipients** -Auflistung ruft die Methode dann das [propertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia))-Objekt ab, das diesem **Recipient** -Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="9db5f-107">For each [Recipient](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient?redirectedfrom=MSDN&view=outlook-pia) in that **Recipients** collection, the method then obtains the [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia)) object that corresponds to that **Recipient** object.</span></span> <span data-ttu-id="9db5f-108">Schließlich verwendet die Methode die [propertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_Recipient_PropertyAccessor) -Eigenschaft, um den Wert der MAPI-Eigenschaft https://schemas.microsoft.com/mapi/proptag/0x39FE001Eabzurufen, die der[PidTagSmtpAddress](https://docs.microsoft.com/office/client-developer/outlook/mapi/pidtagsmtpaddress-canonical-property?redirectedfrom=MSDN)-Eigenschaft ( **\_PR SMTP\_Address** ) des Empfängers zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9db5f-108">Finally, the method uses the [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_Recipient_PropertyAccessor) property to get the value of the MAPI property https://schemas.microsoft.com/mapi/proptag/0x39FE001E, which maps to the **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://docs.microsoft.com/office/client-developer/outlook/mapi/pidtagsmtpaddress-canonical-property?redirectedfrom=MSDN)) property of the recipient.</span></span>

<span data-ttu-id="9db5f-109">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="9db5f-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="9db5f-110">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9db5f-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="9db5f-111">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="9db5f-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="9db5f-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9db5f-112">See also</span></span>

- [<span data-ttu-id="9db5f-113">Empfänger</span><span class="sxs-lookup"><span data-stu-id="9db5f-113">Recipients</span></span>](recipients.md)

