---
title: Abrufen des Organisators einer Besprechung
TOCTitle: Get the organizer of a meeting
ms:assetid: 6a33db84-573b-4d1b-a91a-903f30630ec9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184615(v=office.15)
ms:contentKeyID: 55119872
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 321cf15e0f1144518d526c3897863e9bf3d681dd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583149"
---
# <a name="get-the-organizer-of-a-meeting"></a>Abrufen des Organisators einer Besprechung

Dieses Beispiel zeigt, wie Sie den Organisator einer Besprechung programmgesteuert zurückgeben.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Im folgenden Codebeispiel verwendet GetMeetingOrganizer einen Parameter vom Typ [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), der eine Besprechung darstellt, und das [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\))-Objekt und die [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\))-Methode zum Abrufen der [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) des **AppointmentItem**-Objekts verwendet. Sobald die **EntryID** abgerufen wurde, wird im Beispiel die [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\))-Methode verwendet, um das [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\))-Objekt zurückzugeben, das den Organisator der Besprechung darstellt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Outlook.AddressEntry GetMeetingOrganizer(Outlook.AppointmentItem appt)
{
    if (appt == null)
    {
        throw new ArgumentNullException();
    }
    string PR_SENT_REPRESENTING_ENTRYID =
        @"http://schemas.microsoft.com/mapi/proptag/0x00410102";
    string organizerEntryID =
        appt.PropertyAccessor.BinaryToString(
            appt.PropertyAccessor.GetProperty(
            PR_SENT_REPRESENTING_ENTRYID));
    Outlook.AddressEntry organizer =
        Application.Session.
        GetAddressEntryFromID(organizerEntryID);
    if (organizer != null)
    {
        return organizer; 
    }
    else
    {
        return null;
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Besprechungsanfragen](meeting-requests.md)

