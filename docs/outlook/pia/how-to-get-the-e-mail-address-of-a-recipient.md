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
# <a name="get-the-email-address-of-a-recipient"></a>Abrufen der E-Mail-Adresse eines Empfängers

In diesem Beispiel wird gezeigt, wie die SMTP-Adresse (Simple Mail Transfer Protocol) eines Empfängers abgerufen wird.

## <a name="example"></a>Beispiel

Im folgenden Codebeispiel verwendet die GetSMTPAddressForRecipients-Methode ein [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))-Objekt als Eingabeargument und zeigt dann die SMTP-Adresse jedes Empfängers für das E-Mail-Element an. Die Methode ruft zuerst die [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\))-Auflistung ab, die den Satz von Empfängern darstellt, die für das E-Mail-Element angegeben wurden. Für jedes [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) -Objekt in der **Recipients**-Auflistung ruft die Methode dann das [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) -Objekt ab, das diesem **Recipient**-Objekt entspricht. Schließlich verwendet die Methode die [propertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) -Eigenschaft, um den Wert der MAPI-Eigenschaft http://schemas.microsoft.com/mapi/proptag/0x39FE001Eabzurufen, die der[PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))-Eigenschaft ( **\_PR SMTP\_Address** ) des Empfängers zugeordnet ist.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

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

## <a name="see-also"></a>Siehe auch

- [Empfänger](recipients.md)

