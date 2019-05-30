---
title: Abrufen des Organisators einer Besprechung
TOCTitle: Get the organizer of a meeting
ms:assetid: 6a33db84-573b-4d1b-a91a-903f30630ec9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184615(v=office.15)
ms:contentKeyID: 55119872
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e19b293b581984e9dbb1fe27c9564cb78a73caa1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542535"
---
# <a name="get-the-organizer-of-a-meeting"></a><span data-ttu-id="0be42-102">Abrufen des Organisators einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="0be42-102">Get the organizer of a meeting</span></span>

<span data-ttu-id="0be42-103">Dieses Beispiel zeigt, wie Sie den Organisator einer Besprechung programmgesteuert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0be42-103">This example shows how to programmatically return the organizer of a meeting.</span></span>

## <a name="example"></a><span data-ttu-id="0be42-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0be42-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0be42-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="0be42-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="0be42-106">Im folgenden Codebeispiel verwendet GetMeetingOrganizer einen Parameter vom Typ [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), der eine Besprechung darstellt, und das [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\))-Objekt und die [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\))-Methode zum Abrufen der [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) des **AppointmentItem**-Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="0be42-106">In the following code example, GetMeetingOrganizer takes a parameter of type [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) that represents a meeting, and uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object and the [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) method to obtain the [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) for the **AppointmentItem** object.</span></span> <span data-ttu-id="0be42-107">Sobald die **EntryID** abgerufen wurde, wird im Beispiel die [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\))-Methode verwendet, um das [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\))-Objekt zurückzugeben, das den Organisator der Besprechung darstellt.</span><span class="sxs-lookup"><span data-stu-id="0be42-107">Once the **EntryID** is obtained, the example uses the [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)) method to return the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object that represents the organizer of the meeting.</span></span>

<span data-ttu-id="0be42-108">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="0be42-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="0be42-109">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0be42-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0be42-110">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="0be42-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="0be42-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0be42-111">See also</span></span>

- [<span data-ttu-id="0be42-112">Besprechungsanfragen</span><span class="sxs-lookup"><span data-stu-id="0be42-112">Meeting requests</span></span>](meeting-requests.md)

