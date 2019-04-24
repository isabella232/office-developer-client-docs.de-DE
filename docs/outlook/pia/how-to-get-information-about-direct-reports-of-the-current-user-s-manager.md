---
title: Abrufen von Informationen zu direkten Mitarbeitern des Vorgesetzten des aktuellen Benutzers
TOCTitle: Get information about direct reports of the current user's manager
ms:assetid: 768bf573-1b10-4776-8947-a7f8dc3ebde0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184617(v=office.15)
ms:contentKeyID: 55119842
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d49e96138d8cd2d857c49cc293258e1493afc747
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349434"
---
# <a name="get-information-about-direct-reports-of-the-current-users-manager"></a>Abrufen von Informationen zu direkten Mitarbeitern des Vorgesetzten des aktuellen Benutzers

In diesem Beispiel werden ggf. die Mitarbeiter des Managers des aktuellen Benutzers abgerufen und Informationen zu jedem Mitarbeiter des Managers angezeigt.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Im folgenden Beispiel ruft die GetManagerDirectReports-Prozedur die [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\))-Methode auf, um den Manager des Benutzers abzurufen, der durch ein [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\))-Objekt dargestellt wird. Wenn der aktuelle Benutzer über einen Vorgesetzten verfügt, wird [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)) aufgerufen, um eine [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\))-Auflistung zurückzugeben, die die Adresseinträge für alle Mitarbeiter des Managers des Benutzers darstellt. Wenn der Vorgesetzte keine direkten Mitarbeiter hat, gibt **GetDirectReports** eine **AddressEntries**-Auflistung mit der Anzahl 0 zurück. Nachdem die Mitarbeiter eines Managers abgerufen wurden, schreibt GetManagerDirectReports Informationen zu jedem Mitarbeiter des Managers in die Ablaufverfolgungslistener der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung.


> [!NOTE]
> Der angemeldeten Benutzers muss online sein, damit diese Methode eine **AddressEntries**-Auflistung zurückgibt; andernfalls gibt **GetDirectReports** einen NULL-Verweis zurück. Bei Produktionscode müssen Sie Tests durchführen, wenn der Benutzer offline sind, indem Sie die [\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) -Eigenschaft oder die [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15))-Eigenschaft für mehrere Exchange-Szenarien verwenden.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerDirectReports()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.AddressEntries addrEntries =
                manager.GetDirectReports();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Outlook.ExchangeUser exchUser =
                        addrEntry.GetExchangeUser();
                    StringBuilder sb = new StringBuilder();
                    sb.AppendLine("Name: "
                        + exchUser.Name);
                    sb.AppendLine("Title: "
                        + exchUser.JobTitle);
                    sb.AppendLine("Department: "
                        + exchUser.Department);
                    sb.AppendLine("Location: "
                        + exchUser.OfficeLocation);
                    Debug.WriteLine(sb.ToString());
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Exchange-Benutzer](exchange-users.md)

