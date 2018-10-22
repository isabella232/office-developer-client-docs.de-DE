---
title: Abrufen des Organisators einer Besprechung
TOCTitle: Get the organizer of a meeting
ms:assetid: 6a33db84-573b-4d1b-a91a-903f30630ec9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184615(v=office.15)
ms:contentKeyID: 55119872
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 87d8486b29039f87cb0cbedd2693ce1b4d38b1dc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406771"
---
# <a name="get-the-organizer-of-a-meeting"></a><span data-ttu-id="092c3-102">Abrufen des Organisators einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="092c3-102">Get the organizer of a meeting</span></span>

<span data-ttu-id="092c3-103">Dieses Beispiel zeigt, wie Sie den Organisator einer Besprechung programmgesteuert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="092c3-103">This example shows how to programmatically return the organizer of a meeting.</span></span>

## <a name="example"></a><span data-ttu-id="092c3-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="092c3-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="092c3-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="092c3-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="092c3-106">Im folgenden Codebeispiel verwendet GetMeetingOrganizer einen Parameter vom Typ [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), der eine Besprechung darstellt, und das [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\))-Objekt und die [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\))-Methode zum Abrufen der [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) des **AppointmentItem**-Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="092c3-106">In the following code example,   takes a parameter of type AppointmentItem that represents a meeting, and uses the PropertyAccessor object and the GetProperty(String) method to obtain the EntryID for the AppointmentItem object.</span></span> <span data-ttu-id="092c3-107">Sobald die **EntryID** abgerufen wurde, wird im Beispiel die [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\))-Methode verwendet, um das [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\))-Objekt zurückzugeben, das den Organisator der Besprechung darstellt.</span><span class="sxs-lookup"><span data-stu-id="092c3-107">Once the **EntryID** is obtained, the example uses the [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)) method to return the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object that represents the organizer of the meeting.</span></span>

<span data-ttu-id="092c3-108">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="092c3-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="092c3-109">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="092c3-109">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="092c3-110">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="092c3-110">The following line of code shows how to do the import and assignment in C#.</span></span>

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
        @"https://schemas.microsoft.com/mapi/proptag/0x00410102";
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

## <a name="see-also"></a><span data-ttu-id="092c3-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="092c3-111">See also</span></span>

- [<span data-ttu-id="092c3-112">Besprechungsanfragen</span><span class="sxs-lookup"><span data-stu-id="092c3-112">Meeting Requests</span></span>](meeting-requests.md)

