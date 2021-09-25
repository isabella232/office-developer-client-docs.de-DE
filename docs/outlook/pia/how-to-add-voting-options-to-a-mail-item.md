---
title: Hinzufügen von Abstimmungsoptionen zu einem E-Mail-Element
TOCTitle: Add voting options to a mail item
ms:assetid: 0fb209a8-178d-411e-9551-0a72e041fd65
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424466(v=office.15)
ms:contentKeyID: 55119867
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b339bf003a95e37cf5feb33fb707e220e419c14e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609103"
---
# <a name="add-voting-options-to-a-mail-item"></a>Hinzufügen von Abstimmungsoptionen zu einem E-Mail-Element

In diesem Beispiel wird gezeigt, wie Sie mithilfe der [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\))-Eigenschaft des [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))-Objekts einer E-Mail-Nachricht Abstimmungsoptionen hinzufügen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Abstimmungsoptionen für Nachrichten dienen dazu, Nachrichtenempfängern eine Liste von Optionen anzuzeigen und ihre Antworten nachzuverfolgen. Legen Sie zum programmgesteuerten Erstellen von Abstimmungsoptionen für die **VotingOptions**-Eigenschaft eines **MailItem**-Objekts eine Zeichenfolge mit einer durch Semikolons getrennte Liste von Werten fest. Die Werte für die **VotingOptions**-Eigenschaft werden unter dem Befehl **Abstimmen** in der Gruppe **Antworten** im Menüband der empfangenen Nachricht angezeigt.

Im folgenden Beispiel erstellt OrderPizza Abstimmungsoptionen in einer neuen E-Mail-Nachricht. OrderPizza erstellt zunächst **MailItem**-Objekt und legt dann die **VotingOptions**-Eigenschaft auf „Cheese; Mushroom; Sausage; Combo; Veg Combo“ und die [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\))-Eigenschaft auf „Pizza Order“ fest. Wenn die Nachricht „Pizza Order“ gesendet wird, werden die Abstimmungsoptionen für Empfänger angezeigt. Für jede empfangene Antwort erhalten haben, wird die Wahl des Empfängers auf der Seite **Nachverfolgung** der Nachricht im Ordner „Gesendete Elemente“ des Absenders aufgezeichnet.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

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

## <a name="see-also"></a>Siehe auch

- [Mail](mail.md)

