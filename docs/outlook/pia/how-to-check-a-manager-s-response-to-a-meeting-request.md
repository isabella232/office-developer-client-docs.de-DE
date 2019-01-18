---
title: Überprüfen der Antwort eines Vorgesetzten auf eine Besprechungsanfrage
TOCTitle: Check a manager's response to a meeting request
ms:assetid: 7bdb2163-17e3-47b4-95e5-e051b90506c6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184618(v=office.15)
ms:contentKeyID: 55119847
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba54ba740182eaffc92a0e1932a6fbed1d3804c8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722536"
---
# <a name="check-a-managers-response-to-a-meeting-request"></a>Überprüfen der Antwort eines Vorgesetzten auf eine Besprechungsanfrage

In diesem Beispiel wird veranschaulicht, wie Sie mithilfe der [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) - und der [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) -Methode den Status der Antwort des Vorgesetzten des aktuellen Benutzers auf eine Besprechungsanfrage überprüfen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Wenn Sie ermitteln möchten, ob ein gegebener Empfänger eine Besprechungsanfrage angenommen oder abgelehnt hat, verwenden Sie die [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) -Eigenschaft des [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) -Objekts aus der [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) -Auflistung, die dem [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) -Objekt zugeordnet ist.

Im folgenden Codebeispiel nimmt CheckManagerResponseStatus ein **AppointmentItem**-Objekt als Parameter an. CheckManagerResponseStatus ruft das [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\))-Objekt durch Aufrufen der **GetExchangeUser**-Methode für den aktuellen Benutzer ab. Anschließend ruft CheckManagerResponseStatus das **ExchangeUser**-Objekt ab, das dem Vorgesetzten des aktuellen Benutzers zugeordnet ist, indem es die **GetExchangeUserManager**-Methode aufruft. Mithilfe der [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) -Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\))-Objekts wird dann überprüft, ob das dem **AppointmentItem**-Objekt zugeordnete **Recipient**-Objekt identisch ist mit dem **ExchangeUser**-Objekt, das den Vorgesetzten des Benutzers darstellt. Wenn **CompareEntryIDs** den Wert **true** zurückgibt, befindet sich der Vorgesetzte des Benutzers in der **Recipients**-Auflistung, und CheckManagerResponseStatus gibt den **MeetingResponseStatus** des Vorgesetzten zurück. Gibt **CompareEntryIDs** den Wert **false** zurück, so gibt CheckManagerResponseStatus einen Nullverweis zurück.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Object CheckManagerResponseStatus(Outlook.AppointmentItem appt)
{
    try
    {
        if (appt == null)
        {
            throw new ArgumentNullException();
        }
        Outlook.AddressEntry user =
            Application.Session.CurrentUser.AddressEntry;
        Outlook.ExchangeUser userEx = user.GetExchangeUser();
        if (userEx == null)
        {
            return null;
        }
        Outlook.ExchangeUser manager =
            userEx.GetExchangeUserManager();
        if (manager == null)
        {
            return null;
        }
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            if (Application.Session.CompareEntryIDs(
                recip.AddressEntry.ID, manager.ID))
            {
                return recip.MeetingResponseStatus;
            }
        }
        return null;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
        return null;
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Exchange-Benutzer](exchange-users.md)

