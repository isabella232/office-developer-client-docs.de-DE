---
title: Aufzählen der Einträge in der globalen Adressliste
TOCTitle: Enumerate the entries in the Global Address List
ms:assetid: f3dfe312-fe91-475d-8435-1c7a0bb2b725
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184654(v=office.15)
ms:contentKeyID: 55119801
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f9e392710940a63f5d7723d303d5cf48569ad92f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407548"
---
# <a name="enumerate-the-entries-in-the-global-address-list"></a><span data-ttu-id="66c54-102">Aufzählen der Einträge in der globalen Adressliste</span><span class="sxs-lookup"><span data-stu-id="66c54-102">How to: Enumerate the Entries in the Global Address List</span></span>

<span data-ttu-id="66c54-103">In diesem Beispiel werden die ersten 100 primären SMTP-Adressen (Simple Mail Transfer Protocol) in der globalen Adressliste (GAL) aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="66c54-103">This example enumerates the first 100 primary Simple Mail Transfer Protocol (SMTP) addresses in the Global Address List (GAL).</span></span>

## <a name="example"></a><span data-ttu-id="66c54-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="66c54-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="66c54-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="66c54-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="66c54-106">Im folgenden Codebeispiel wird die SMTP-Adresse für ein [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) -Objekt abgerufen, indem sie in einem Aufruf der Methoden [GetExchangeUser()](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) oder [GetExchangeDistributionList()](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) in ein [ExchangeUser](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) - oder [ExchangeDistributionList](https://msdn.microsoft.com/library/bb611805\(v=office.15\)) -Objekt umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="66c54-106">In the following code example, the SMTP address for an [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object is obtained by casting it to an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) or [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) object in a call to the [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) or [GetExchangeDistributionList()](https://msdn.microsoft.com/library/bb611805\(v=office.15\)) methods.</span></span> <span data-ttu-id="66c54-107">Stellt das **AddressEntry**-Objekt einen Exchange-Benutzer dar, gibt EnumerateGAL ein **ExchangeUser**-Objekt zurück, das Eigenschaften des **AddressEntry**-Objekts verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="66c54-107">If the AddressEntry object represents an Exchange user,   returns an ExchangeUser object that exposes properties of the AddressEntry object.</span></span> <span data-ttu-id="66c54-108">Verwenden Sie ExchangeUser-Eigenschaften wie [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [Alias](https://msdn.microsoft.com/library/bb610682\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)) oder [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)), um diese verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="66c54-108">Use ExchangeUser properties such as JobTitle , Department , Alias , BusinessTelephoneNumber , or PrimarySmtpAddress to expose them.</span></span>

<span data-ttu-id="66c54-109">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="66c54-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="66c54-110">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="66c54-110">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="66c54-111">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="66c54-111">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateGAL()
{
    Outlook.AddressList gal =
        Application.Session.GetGlobalAddressList();
    if (gal != null)
    {
        for (int i = 1; 
            i <= Math.Min(100, gal.AddressEntries.Count - 1); i++)
        {
            Outlook.AddressEntry addrEntry =
                gal.AddressEntries[i];
            if (addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeUserAddressEntry
                || addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeRemoteUserAddressEntry)
            {
                Outlook.ExchangeUser exchUser =
                    addrEntry.GetExchangeUser();
                Debug.WriteLine(exchUser.Name + " "
                    + exchUser.PrimarySmtpAddress);
            }
            if (addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeDistributionListAddressEntry)
            {
                Outlook.ExchangeDistributionList exchDL =
                    addrEntry.GetExchangeDistributionList();
                Debug.WriteLine(exchDL.Name + " "
                    + exchDL.PrimarySmtpAddress);
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="66c54-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66c54-112">See also</span></span>

[<span data-ttu-id="66c54-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="66c54-113">Address Book</span></span>](address-book.md)

