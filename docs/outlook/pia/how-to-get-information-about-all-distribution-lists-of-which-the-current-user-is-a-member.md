---
title: Abrufen von Informationen über alle Verteilerlisten, in denen der aktuelle Benutzer Mitglied ist
TOCTitle: Get information about all distribution lists of which the current user is a member
ms:assetid: c5be6aa8-8d85-463e-a377-2a4d57e2106b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184638(v=office.15)
ms:contentKeyID: 55119836
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ef170173111287efb3eb96ad0882b9fb50a1aa5b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629291"
---
# <a name="get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member"></a>Abrufen von Informationen über alle Verteilerlisten, in denen der aktuelle Benutzer Mitglied ist

In diesem Beispiel wird die [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\))-Methode zum Abrufen von Informationen über alle Verteilerlisten verwendet, in denen der aktuelle Benutzer Mitglied ist.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Im folgenden Beispiel ruft GetCurrentUserMembership die **GetMemberOfList**-Methode zum Abrufen einer [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\))-Auflistung für alle Verteilerlisten ab, in denen der Exchange-Benutzer Mitglied ist. Wenn der Benutzer kein Mitglied einer Verteilerliste ist, gibt **GetMemberOfList** eine **AddressEntries**-Auflistung zurück, die Anzahl 0 aufweist. Der Benutzer muss online sein, damit **GetMemberOfList** eine **AddressEntries**-Auflistung zurückgibt; andernfalls gibt **GetMemberOfList** einen NULL-Verweis zurück. GetCurrentUserMembership verwendet die [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\))-Methode, die das aktuelle [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\))-Objekt zurückgibt, um zu testen, ob der Benutzer online ist. Nachdem die Adresseinträge abgerufen wurden, schreibt das Beispiel Informationen zu den Verteilerlisten jedes Benutzers in die Listener der Ablaufverfolgung der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserMembership()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser exchUser =
            currentUser.GetExchangeUser();
        if (exchUser != null)
        {
            Outlook.AddressEntries addrEntries =
                exchUser.GetMemberOfList();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Debug.WriteLine(addrEntry.Name);
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Exchange-Benutzer](exchange-users.md)

