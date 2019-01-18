---
title: Senden eines E-Mail-Elements mithilfe eines Hotmail-Kontos
TOCTitle: Send a mail item by using a Hotmail account
ms:assetid: f25853a7-67c0-46a3-a298-5cdf72ebc53f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184652(v=office.15)
ms:contentKeyID: 55119797
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 008f66ff1a43f90e756900c467ba6c086829b769
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701522"
---
# <a name="send-a-mail-item-by-using-a-hotmail-account"></a>Senden eines E-Mail-Elements mithilfe eines Hotmail-Kontos

In diesem Beispiel wird die [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\))-Eigenschaft verwendet, um ein E-Mail-Element mithilfe eines Windows Live Hotmail-Kontos zu senden.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

In einem Profil sind ein oder mehrere E-Mail-Konten definiert, die jeweils einem Server eines bestimmten Typs, wie Microsoft Exchange Server oder POP3 (Post Office Protocol 3), zugeordnet sind. Da ein Profil mehrere Konten enthalten kann, müssen Sie angeben, mit welchem E-Mail-Konto Sie das Element senden möchten, und dann ein [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) -Objekt zu seiner Darstellung abrufen.

Im nachstehenden Codebeispiel wird eine Nachricht mit einer angefügten Reiseroute erstellt und dann mit einem Windows Live Hotmail-Konto gesendet. Das Hotmail-E-Mail-Konto wird als **Account**-Objekt im Profil des Benutzers verwendet. Das Codebeispiel legt dann die SendUsingAccount-Eigenschaft auf dieses Konto fest und ruft die [Send()](https://msdn.microsoft.com/library/bb644139\(v=office.15\))-Methode aus dem [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))-Objekt auf.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void SendUsingAccountExample()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Our itinerary";
    mail.Attachments.Add(@"c:\travel\itinerary.doc",
        Outlook.OlAttachmentType.olByValue,
        Type.Missing, Type.Missing);
    Outlook.Account account =
        Application.Session.Accounts["Hotmail"];
    mail.SendUsingAccount = account;
    mail.Send();
}
```

## <a name="see-also"></a>Siehe auch

- [Konten](accounts.md)

