---
title: Abrufen von Informationen über alle Verteilerlisten, in denen der aktuelle Benutzer Mitglied ist
TOCTitle: Get information about all distribution lists of which the current user is a member
ms:assetid: c5be6aa8-8d85-463e-a377-2a4d57e2106b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184638(v=office.15)
ms:contentKeyID: 55119836
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f98d7a338866624e67d745e66a66e864fb9bbf99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406764"
---
# <a name="get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member"></a><span data-ttu-id="9f5da-102">Abrufen von Informationen über alle Verteilerlisten, in denen der aktuelle Benutzer Mitglied ist</span><span class="sxs-lookup"><span data-stu-id="9f5da-102">Get information about all distribution lists of which the current user is a member</span></span>

<span data-ttu-id="9f5da-103">In diesem Beispiel wird die [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\))-Methode zum Abrufen von Informationen über alle Verteilerlisten verwendet, in denen der aktuelle Benutzer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="9f5da-103">This example uses the [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) method to get information about all distribution lists of which the current user is a member.</span></span>

## <a name="example"></a><span data-ttu-id="9f5da-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9f5da-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="9f5da-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="9f5da-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="9f5da-106">Im folgenden Beispiel ruft GetCurrentUserMembership die **GetMemberOfList**-Methode zum Abrufen einer [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\))-Auflistung für alle Verteilerlisten ab, in denen der Exchange-Benutzer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="9f5da-106">In the following example, GetCurrentUserMembership calls the **GetMemberOfList** method to get an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection for all distribution lists of which the Exchange user is a member.</span></span> <span data-ttu-id="9f5da-107">Wenn der Benutzer kein Mitglied einer Verteilerliste ist, gibt **GetMemberOfList** eine **AddressEntries**-Auflistung zurück, die Anzahl 0 aufweist.</span><span class="sxs-lookup"><span data-stu-id="9f5da-107">If the user is not a member of any distribution lists, **GetMemberOfList** returns an **AddressEntries** collection that has a count of zero.</span></span> <span data-ttu-id="9f5da-108">Der Benutzer muss online sein, damit **GetMemberOfList** eine **AddressEntries**-Auflistung zurückgibt; andernfalls gibt **GetMemberOfList** einen NULL-Verweis zurück.</span><span class="sxs-lookup"><span data-stu-id="9f5da-108">The user must be online for **GetMemberOfList** to return an **AddressEntries** collection; otherwise, **GetMemberOfList** returns a null reference.</span></span> <span data-ttu-id="9f5da-109">GetCurrentUserMembership verwendet die [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\))-Methode, die das aktuelle [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\))-Objekt zurückgibt, um zu testen, ob der Benutzer online ist.</span><span class="sxs-lookup"><span data-stu-id="9f5da-109">GetCurrentUserMembership uses the [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) method, which returns the current [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object, to test whether the user is online.</span></span> <span data-ttu-id="9f5da-110">Nachdem die Adresseinträge abgerufen wurden, schreibt das Beispiel Informationen zu den Verteilerlisten jedes Benutzers in die Listener der Ablaufverfolgung der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="9f5da-110">Once the address entries are obtained, the example writes information about each of the user’s distribution lists to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="9f5da-111">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="9f5da-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="9f5da-112">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9f5da-112">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="9f5da-113">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="9f5da-113">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="9f5da-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f5da-114">See also</span></span>

- [<span data-ttu-id="9f5da-115">Exchange-Benutzer</span><span class="sxs-lookup"><span data-stu-id="9f5da-115">Exchange Users</span></span>](exchange-users.md)

