---
title: Hinzufügen einer benutzerdefinierten Aktion als Antwort auf ein E-Mail-Element
TOCTitle: Add a custom action as a response to a mail item
ms:assetid: 99e8ba6b-9c47-4b10-968b-436b08d199ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424474(v=office.15)
ms:contentKeyID: 55119870
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e253ffbb2da7b0c1a566cf9bbd211766c2916202
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609082"
---
# <a name="add-a-custom-action-as-a-response-to-a-mail-item"></a>Hinzufügen einer benutzerdefinierten Aktion als Antwort auf ein E-Mail-Element

In diesem Beispiel wird gezeigt, wie Sie mithilfe der [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\))-Methode der [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\))-Auflistung benutzerdefinierte Aktionen als Antwort auf ein E-Mail-Element hinzufügen können.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Sie können benutzerdefinierte Aktionen programmgesteuert so erstellen, dass sie in einer E-Mail-Antwort im Menüband auf der Registerkarte **Nachricht** in der Gruppe **Aktionen** angezeigt werden. Im folgenden Codebeispiel wird mithilfe von ReplyWithVoiceMail eine benutzerdefinierte Aktion namens „Reply with Voice Mail“ erstellt und der Inspektor-Befehlsleiste hinzugefügt. ReplyWithVoiceMail ruft zuerst ein [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\))-Objekt ab und erstellt dann durch Aufrufen der **Add**-Methode der **Actions**-Auflistung, die dem **MailItem** zugeordnet ist, ein [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\))-Objekt. Anschließend wird die [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) -Eigenschaft des **Action**-Objekts auf „Reply with Voice Mail“ festgelegt. Auch die [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\))-, die [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\))-, die [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\))- und die [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\))-Eigenschaft werden festgelegt. Schließlich wird das **MailItem** gespeichert.


> [!NOTE]
> Mit dem Outlook-Formular-Designer können Sie auch benutzerdefinierte Aktionen zur Entwurfszeit hinzufügen.


Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

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

## <a name="see-also"></a>Siehe auch

- [Mail](mail.md)

