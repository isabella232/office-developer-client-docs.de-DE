---
title: Abrufen der E-Mail-Adresse eines Empfängers
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-the-e-mail-address-of-a-recipient?redirectedfrom=MSDN
ms:contentKeyID: 55119879
ms.date: 12/03/2019
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 57b2e0ee4dd3db0da42dcb5a075248999deed6ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590625"
---
# <a name="get-the-email-address-of-a-recipient"></a>Abrufen der E-Mail-Adresse eines Empfängers

In diesem Beispiel wird gezeigt, wie die SMTP-Adresse (Simple Mail Transfer Protocol) eines Empfängers abgerufen wird.

## <a name="example"></a>Beispiel

Im folgenden Codebeispiel verwendet die GetSMTPAddressForRecipients-Methode ein [MailItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mailitem?redirectedfrom=MSDN&view=outlook-pia)-Objekt als Eingabeargument und zeigt dann die SMTP-Adresse jedes Empfängers für das E-Mail-Element an. Die Methode ruft zuerst die [Recipients](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipients?redirectedfrom=MSDN&view=outlook-pia)-Auflistung ab, die den Satz von Empfängern darstellt, die für das E-Mail-Element angegeben wurden. Für jeden [Recipient](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient?redirectedfrom=MSDN&view=outlook-pia) in dieser **Recipients** -Auflistung ruft die Methode dann das [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia)) -Objekt ab, das diesem **Recipient -Objekt** entspricht. Schließlich verwendet die Methode die [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_Recipient_PropertyAccessor)-Eigenschaft, um den Wert der MAPI-Eigenschaft https://schemas.microsoft.com/mapi/proptag/0x39FE001E abzurufen, die der **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://docs.microsoft.com/office/client-developer/outlook/mapi/pidtagsmtpaddress-canonical-property?redirectedfrom=MSDN)) des Empfängers zugeordnet ist.

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

