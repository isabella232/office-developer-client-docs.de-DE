---
title: Abrufen der SMTP-Adresse des Absenders eines E-Mail-Elements
TOCTitle: Get the SMTP address of the sender of a mail item
ms:assetid: 86e0c0aa-1696-4415-b25f-f9c1c29d88a9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184624(v=office.15)
ms:contentKeyID: 55119869
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 74adbf02180e0e993b22e35481f51d304b14e7d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320083"
---
# <a name="get-the-smtp-address-of-the-sender-of-a-mail-item"></a>Abrufen der SMTP-Adresse des Absenders eines E-Mail-Elements

In diesem Beispiel wird die SMTP-Adresse (Simple Mail Transfer Protocol) des Absenders für ein E-Mail-Element abgerufen.

## <a name="example"></a>Beispiel

Zum Ermitteln der SMTP-Adresse für ein empfangenes E-Mail-Element verwenden Sie die [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\))-Eigenschaft des [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))-Objekts. Befindet sich der Absender jedoch innerhalb Ihrer Organisation, gibt **SenderEmailAddress** keine SMTP-Adresse zurück, d. h. Sie müssen das [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\))-Objekt verwenden, damit die SMTP-Adresse des Absenders zurückgegeben wird.

Im folgenden Codebeispiel ruft GetSenderSMTPAddress mithilfe des **PropertyAccessor**-Objekts Werte ab, die im Outlook-Objektmodell nicht direkt verfügbar gemacht werden. GetSenderSMTPAddress verwendet ein **MailItem**. Ist der Wert der [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) -Eigenschaft des empfangenen **MailItem**-Elements "EX", befindet sich der Absender der Nachricht auf einem Exchange-Server innerhalb Ihrer Organisation. GetSenderSMTPAddress ruft mithilfe der [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\))-Eigenschaft des **MailItem**-Objekts den Absender ab, der durch das [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\))-Objekt dargestellt wird. Stellt das **AddressEntry**-Objekt einen Exchange-Benutzer dar, wird im Beispielcode die [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) -Methode aufgerufen, damit das [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) -Objekt des **AddressEntry**-Objekts zurückgegeben wird. Anschließend verwendet GetSenderSMTPAddress die [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\))-Eigenschaft des **ExchangeUser**-Objekts, um die SMTP-Adresse des Absenders zurückzugeben. Stellt das **AddressEntry**-Objekt für den Absender kein **ExchangeUser**-Objekt dar, wird die [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\))-Methode des **PropertyAccessor**-Objekts mit **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) als Argument verwendet, um die SMTP-Adresse des Absenders zurückzugeben.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetSenderSMTPAddress(Outlook.MailItem mail)
{
    string PR_SMTP_ADDRESS =
        @"https://schemas.microsoft.com/mapi/proptag/0x39FE001E";
    if (mail == null)
    {
        throw new ArgumentNullException();
    }
    if (mail.SenderEmailType == "EX")
    {
        Outlook.AddressEntry sender =
            mail.Sender;
        if (sender != null)
        {
            //Now we have an AddressEntry representing the Sender
            if (sender.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeUserAddressEntry
                || sender.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeRemoteUserAddressEntry)
            {
                //Use the ExchangeUser object PrimarySMTPAddress
                Outlook.ExchangeUser exchUser =
                    sender.GetExchangeUser();
                if (exchUser != null)
                {
                    return exchUser.PrimarySmtpAddress;
                }
                else
                {
                    return null;
                }
            }
            else
            {
                return sender.PropertyAccessor.GetProperty(
                    PR_SMTP_ADDRESS) as string;
            }
        }
        else
        {
            return null;
        }
    }
    else
    {
        return mail.SenderEmailAddress;
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Mail](mail.md)

