---
title: Abrufen von Informationen über alle Verteilerlisten, in denen der aktuelle Benutzer Mitglied ist
TOCTitle: Get information about all distribution lists of which the current user is a member
ms:assetid: c5be6aa8-8d85-463e-a377-2a4d57e2106b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184638(v=office.15)
ms:contentKeyID: 55119836
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bbc87250ab77f662e0fc5a71f9857e734637dd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349427"
---
# <a name="get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member"></a><span data-ttu-id="94eef-102">Abrufen von Informationen über alle Verteilerlisten, in denen der aktuelle Benutzer Mitglied ist</span><span class="sxs-lookup"><span data-stu-id="94eef-102">Get information about all distribution lists of which the current user is a member</span></span>

<span data-ttu-id="94eef-103">In diesem Beispiel wird die [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\))-Methode zum Abrufen von Informationen über alle Verteilerlisten verwendet, in denen der aktuelle Benutzer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="94eef-103">This example uses the [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) method to get information about all distribution lists of which the current user is a member.</span></span>

## <a name="example"></a><span data-ttu-id="94eef-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="94eef-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="94eef-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="94eef-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="94eef-106">Im folgenden Beispiel ruft GetCurrentUserMembership die **GetMemberOfList**-Methode zum Abrufen einer [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\))-Auflistung für alle Verteilerlisten ab, in denen der Exchange-Benutzer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="94eef-106">In the following example, GetCurrentUserMembership calls the **GetMemberOfList** method to get an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection for all distribution lists of which the Exchange user is a member.</span></span> <span data-ttu-id="94eef-107">Wenn der Benutzer kein Mitglied einer Verteilerliste ist, gibt **GetMemberOfList** eine **AddressEntries**-Auflistung zurück, die Anzahl 0 aufweist.</span><span class="sxs-lookup"><span data-stu-id="94eef-107">If the user is not a member of any distribution lists, **GetMemberOfList** returns an **AddressEntries** collection that has a count of zero.</span></span> <span data-ttu-id="94eef-108">Der Benutzer muss online sein, damit **GetMemberOfList** eine **AddressEntries**-Auflistung zurückgibt; andernfalls gibt **GetMemberOfList** einen NULL-Verweis zurück.</span><span class="sxs-lookup"><span data-stu-id="94eef-108">The user must be online for **GetMemberOfList** to return an **AddressEntries** collection; otherwise, **GetMemberOfList** returns a null reference.</span></span> <span data-ttu-id="94eef-109">GetCurrentUserMembership verwendet die [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\))-Methode, die das aktuelle [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\))-Objekt zurückgibt, um zu testen, ob der Benutzer online ist.</span><span class="sxs-lookup"><span data-stu-id="94eef-109">GetCurrentUserMembership uses the [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) method, which returns the current [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object, to test whether the user is online.</span></span> <span data-ttu-id="94eef-110">Nachdem die Adresseinträge abgerufen wurden, schreibt das Beispiel Informationen zu den Verteilerlisten jedes Benutzers in die Listener der Ablaufverfolgung der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="94eef-110">Once the address entries are obtained, the example writes information about each of the user’s distribution lists to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="94eef-111">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="94eef-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="94eef-112">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="94eef-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="94eef-113">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="94eef-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="94eef-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94eef-114">See also</span></span>

- [<span data-ttu-id="94eef-115">Exchange-Benutzer</span><span class="sxs-lookup"><span data-stu-id="94eef-115">Exchange users</span></span>](exchange-users.md)

