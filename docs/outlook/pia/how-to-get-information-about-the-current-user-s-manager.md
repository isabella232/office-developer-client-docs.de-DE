---
title: Abrufen von Informationen zum Vorgesetzten des aktuellen Benutzers
TOCTitle: Get information about the current user's manager
ms:assetid: 3a77fa51-e2e3-4544-849f-4267b1762270
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184603(v=office.15)
ms:contentKeyID: 55119846
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 89da7df4aac29b7d308dd0b0f432d8652c5f0127
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407310"
---
# <a name="get-information-about-the-current-users-manager"></a><span data-ttu-id="b0a7b-102">Abrufen von Informationen zum Vorgesetzten des aktuellen Benutzers</span><span class="sxs-lookup"><span data-stu-id="b0a7b-102">Get information about the current user's manager</span></span>

<span data-ttu-id="b0a7b-103">Dieses Beispiel zeigt, wie Sie Informationen (z. B. Namen, berufliche Position und Telefonnummern) zum Vorgesetzten des aktuellen Benutzers abrufen.</span><span class="sxs-lookup"><span data-stu-id="b0a7b-103">This example shows how to get information (such as name, job title, and phone numbers) about the current user’s manager.</span></span>

## <a name="example"></a><span data-ttu-id="b0a7b-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b0a7b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b0a7b-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="b0a7b-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="b0a7b-106">Im folgenden Verfahren ruft GetManagerInfo die [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\))-Methode auf, um ein[ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\))-Objekt abzurufen, das dem Vorgesetzten eines **ExchangeUser** in der Unternehmenshierarchie entspricht.</span><span class="sxs-lookup"><span data-stu-id="b0a7b-106">In the following procedure,   calls the GetExchangeUserManager() method to obtain an ExchangeUser object that represents the manager of an ExchangeUser in the organizational hierarchy.</span></span> <span data-ttu-id="b0a7b-107">Das Verfahren überprüft, ob der angemeldete Benutzer online ist, um sicherzustellen, dass **GetExchangeUserManager** ein **ExchangeUser**-Objekt zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="b0a7b-107">The procedure tests whether the logged-on user is online to ensure that **GetExchangeUserManager** can return an **ExchangeUser** object.</span></span> <span data-ttu-id="b0a7b-108">Wenn der Benutzer nicht online ist, gibt **GetExchangeUserManager** einen NULL-Verweis zurück.</span><span class="sxs-lookup"><span data-stu-id="b0a7b-108">If the user is not online, **GetExchangeUserManager** will return a null reference.</span></span> <span data-ttu-id="b0a7b-109">Durch GetManagerInfo werden dann die Informationen zum Vorgesetzten in die Ablaufverfolgungslistenern der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Sammlung geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b0a7b-109"> then writes manager information to the trace listeners of the Listeners collection.</span></span>

<span data-ttu-id="b0a7b-110">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="b0a7b-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="b0a7b-111">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b0a7b-111">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="b0a7b-112">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="b0a7b-112">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerInfo()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Name: "
                + manager.Name);
            sb.AppendLine("STMP address: "
                + manager.PrimarySmtpAddress);
            sb.AppendLine("Title: "
                + manager.JobTitle);
            sb.AppendLine("Department: "
                + manager.Department);
            sb.AppendLine("Location: "
                + manager.OfficeLocation);
            sb.AppendLine("Business phone: "
                + manager.BusinessTelephoneNumber);
            sb.AppendLine("Mobile phone: "
                + manager.MobileTelephoneNumber);
            Debug.WriteLine(sb.ToString());
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="b0a7b-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0a7b-113">See also</span></span>

- [<span data-ttu-id="b0a7b-114">Exchange-Benutzer</span><span class="sxs-lookup"><span data-stu-id="b0a7b-114">Exchange Users</span></span>](exchange-users.md)

