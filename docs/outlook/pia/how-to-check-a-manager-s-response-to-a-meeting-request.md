---
title: Überprüfen der Antwort eines Vorgesetzten auf eine Besprechungsanfrage
TOCTitle: Check a manager's response to a meeting request
ms:assetid: 7bdb2163-17e3-47b4-95e5-e051b90506c6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184618(v=office.15)
ms:contentKeyID: 55119847
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 14d78a88a0df514bca6782a84bd2c030fc140093
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406351"
---
# <a name="check-a-managers-response-to-a-meeting-request"></a><span data-ttu-id="54438-102">Überprüfen der Antwort eines Vorgesetzten auf eine Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="54438-102">Check a manager's response to a meeting request</span></span>

<span data-ttu-id="54438-103">In diesem Beispiel wird veranschaulicht, wie Sie mithilfe der [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) - und der [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) -Methode den Status der Antwort des Vorgesetzten des aktuellen Benutzers auf eine Besprechungsanfrage überprüfen.</span><span class="sxs-lookup"><span data-stu-id="54438-103">This example illustrates how to use the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) and [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) methods to check the status of the response of the current user's manager to a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="54438-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="54438-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="54438-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="54438-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="54438-106">Wenn Sie ermitteln möchten, ob ein gegebener Empfänger eine Besprechungsanfrage angenommen oder abgelehnt hat, verwenden Sie die [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) -Eigenschaft des [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) -Objekts aus der [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) -Auflistung, die dem [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) -Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="54438-106">To determine whether a given recipient has accepted or declined a requested meeting, use the [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) property of the [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object from the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection associated with the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span>

<span data-ttu-id="54438-107">Im folgenden Codebeispiel nimmt CheckManagerResponseStatus ein **AppointmentItem**-Objekt als Parameter an.</span><span class="sxs-lookup"><span data-stu-id="54438-107">In the following code example,   takes in an AppointmentItem object as a parameter.</span></span> <span data-ttu-id="54438-108">CheckManagerResponseStatus ruft das [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\))-Objekt durch Aufrufen der **GetExchangeUser**-Methode für den aktuellen Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="54438-108"> gets the ExchangeUser object by calling the GetExchangeUser method on the current user.</span></span> <span data-ttu-id="54438-109">Anschließend ruft CheckManagerResponseStatus das **ExchangeUser**-Objekt ab, das dem Vorgesetzten des aktuellen Benutzers zugeordnet ist, indem es die **GetExchangeUserManager**-Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="54438-109"> then gets the ExchangeUser object that is associated with the current user's manager by calling the GetExchangeUserManager method.</span></span> <span data-ttu-id="54438-110">Mithilfe der [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) -Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\))-Objekts wird dann überprüft, ob das dem **AppointmentItem**-Objekt zugeordnete **Recipient**-Objekt identisch ist mit dem **ExchangeUser**-Objekt, das den Vorgesetzten des Benutzers darstellt.</span><span class="sxs-lookup"><span data-stu-id="54438-110">By using the [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object, the example then checks whether the **Recipient** object associated with the **AppointmentItem** object is the same as the **ExchangeUser** object that represents the user's manager.</span></span> <span data-ttu-id="54438-111">Wenn **CompareEntryIDs** den Wert **true** zurückgibt, befindet sich der Vorgesetzte des Benutzers in der **Recipients**-Auflistung, und CheckManagerResponseStatus gibt den **MeetingResponseStatus** des Vorgesetzten zurück.</span><span class="sxs-lookup"><span data-stu-id="54438-111">If CompareEntryIDs returns true, the user's manager is found in the Recipients collection, and   returns the manager's MeetingResponseStatus.</span></span> <span data-ttu-id="54438-112">Gibt **CompareEntryIDs** den Wert **false** zurück, so gibt CheckManagerResponseStatus einen Nullverweis zurück.</span><span class="sxs-lookup"><span data-stu-id="54438-112">If CompareEntryIDs returns false,   returns a null reference.</span></span>

<span data-ttu-id="54438-113">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="54438-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="54438-114">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="54438-114">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="54438-115">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="54438-115">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="54438-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54438-116">See also</span></span>

- [<span data-ttu-id="54438-117">Exchange-Benutzer</span><span class="sxs-lookup"><span data-stu-id="54438-117">Exchange Users</span></span>](exchange-users.md)

