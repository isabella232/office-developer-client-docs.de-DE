---
title: Angeben verschiedener Empfängertypen für ein E-Mail-Element
TOCTitle: Specify different recipient types for a mail item
ms:assetid: 2a3ace9f-627c-4fdd-b182-afc1b53af85b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184598(v=office.15)
ms:contentKeyID: 55119871
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 9eca70f9c1b77e8430625fb49e3ae9787d337ba7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405532"
---
# <a name="specify-different-recipient-types-for-a-mail-item"></a>Angeben verschiedener Empfängertypen für ein E-Mail-Element

Dieses Beispiel zeigt, wie Sie programmgesteuert verschiedene Empfängertypen („An“, „Cc“ oder „Bcc“) für ein E-Mail-Element festlegen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Im folgenden Codebeispiel wird gezeigt, wie Sie angeben, ob ein Empfänger eines [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))-Objekts ein Empfänger vom Typ „An“, „Cc“ oder „Bcc“ ist. SetRecipientTypeForMail erstellt ein **MailItem**-Objekt, fügt drei [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\))-Objekte zur [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\))-Sammlung der **MailItem**-Objekte hinzu und legt dann die [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\))-Eigenschaft jedes **Recipient**-Objekts auf einen Wert aus der [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\))-Aufzählung fest.


> [!NOTE]
> Die **Type**-Eigenschaft des **Recipient**-Objekts ist ein int-Typ und steht nicht mit einer Aufzählung eines bestimmten Empfängertypen im Zusammenhang.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

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

## <a name="see-also"></a>Siehe auch

- [Mail](mail.md)

