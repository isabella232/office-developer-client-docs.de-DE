---
title: Suchen des einer Besprechungsanfrage zugeordneten Terminelements
TOCTitle: Find the appointment item associated with a meeting request
ms:assetid: ff356fcf-0980-4567-8570-4bbcb14381e7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184658(v=office.15)
ms:contentKeyID: 55119875
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43bc64dbbed14dae2e185ea89d15b6061858de42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320300"
---
# <a name="find-the-appointment-item-associated-with-a-meeting-request"></a>Suchen des einer Besprechungsanfrage zugeordneten Terminelements

In diesem Beispiel wird gezeigt, wie die [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\))-Methode verwendet wird, um den Termin zu finden, der einer Besprechungsanfrage zugeordnet ist.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Ein [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\))-Objekt stellt keinen Termin dar, sondern eine Nachricht mit einer Anfrage, dem Kalender des Empfängers einen Termin hinzuzufügen. Im folgenden Codebeispiel verwendet MeetingRequestExample die [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\))-Methode des **MeetingItem**-Objekts für jedes **MeetingItem**-Objekt aus dem Posteingang des Benutzers. Das zurückgegebene [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt wird dann verwendet, um den Betreff des Termins in die Ablaufverfolgungslistener der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung zu schreiben.


> [!NOTE]
> Beachten Sie, dass das **GetAssociatedAppointment**-Argument auf **false** festgelegt wird, sodass der Termin dem Kalender des Benutzers nicht hinzugefügt wird.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void MeetingRequestsExample()
{
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(false);
        if (appt != null)
        {
            Debug.WriteLine(appt.Subject);
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Besprechungsanfragen](meeting-requests.md)

