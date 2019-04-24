---
title: Erstellen eines Kontaktelements
TOCTitle: Create a Contact item
ms:assetid: b316294a-7f70-4e54-9375-4dc515e9fd11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184633(v=office.15)
ms:contentKeyID: 55119823
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11bfe40d29832577186712e269f9c0971e1e2be6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359675"
---
# <a name="create-a-contact-item"></a><span data-ttu-id="69af0-102">Erstellen eines Kontaktelements</span><span class="sxs-lookup"><span data-stu-id="69af0-102">Create a Contact item</span></span>

<span data-ttu-id="69af0-103">Dieses Beispiel zeigt, wie Sie ein Kontaktelement erstellen und verschiedene Eigenschaften für den Kontakt festlegen.</span><span class="sxs-lookup"><span data-stu-id="69af0-103">This example shows how to create a contact item and set various properties for the contact.</span></span>

## <a name="example"></a><span data-ttu-id="69af0-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="69af0-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="69af0-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="69af0-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="69af0-106">Ein [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\))-Objekt von Outlook verfügt über mehr als 100 integrierte Eigenschaften, wie [Department](https://msdn.microsoft.com/library/bb610564\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)) und [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="69af0-106">An Outlook [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object has more than 100 built-in properties such as [Department](https://msdn.microsoft.com/library/bb610564\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)), and [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)).</span></span> <span data-ttu-id="69af0-107">Sie können mit der [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\))-Auflistung benutzerdefinierte Eigenschaften hinzufügen, wenn eine integrierte Eigenschaft nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="69af0-107">You can add custom properties, if a built-in property is not available, by using the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection.</span></span> <span data-ttu-id="69af0-108">Nachdem Sie ein **ContactItem** erstellt haben, können Sie seine Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="69af0-108">Once you create a **ContactItem**, you can set its properties.</span></span>

<span data-ttu-id="69af0-109">Im folgenden Codebeispiel erstellt CreateContactExample ein **ContactItem**-Objekt und legt häufig verwendete Eigenschaften für das Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="69af0-109">In the following code example, CreateContactExample creates a **ContactItem** and sets commonly used properties for that object.</span></span> <span data-ttu-id="69af0-110">Dann wird die [ShowCheckPhoneDialog(OlContactPhoneNumber)](https://msdn.microsoft.com/library/bb646168\(v=office.15\))-Methode für das **ContactItem**-Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="69af0-110">It then calls the [ShowCheckPhoneDialog(OlContactPhoneNumber)](https://msdn.microsoft.com/library/bb646168\(v=office.15\)) method on the **ContactItem** object.</span></span> <span data-ttu-id="69af0-111">Die **ShowCheckPhoneDialog**-Methode ermöglicht es dem Benutzer, eine Telefonnummer basierend auf den lokalen Konventionen für Telefonnummern aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="69af0-111">The **ShowCheckPhoneDialog** method allows the user to resolve a phone number based on local dialing conventions.</span></span>

<span data-ttu-id="69af0-112">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="69af0-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="69af0-113">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="69af0-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="69af0-114">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="69af0-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateContactExample()
{
    Outlook.ContactItem contact = Application.CreateItem(
        Outlook.OlItemType.olContactItem) as Outlook.ContactItem;
    contact.FirstName = "Mellissa";
    contact.LastName = "MacBeth";
    contact.JobTitle = "Account Representative";
    contact.CompanyName = "Contoso Ltd.";
    contact.OfficeLocation = "36/2529";
    contact.BusinessTelephoneNumber = "4255551212 x432";
    contact.WebPage = "https://www.contoso.com";
    contact.BusinessAddressStreet = "1 Microsoft Way";
    contact.BusinessAddressCity = "Redmond";
    contact.BusinessAddressState = "WA";
    contact.BusinessAddressPostalCode = "98052";
    contact.BusinessAddressCountry =
        "United States of America";
    contact.Email1Address = "melissa@contoso.com";
    contact.Email1AddressType = "SMTP";
    contact.Email1DisplayName =
        "Melissa MacBeth (mellissa@contoso.com)";
    contact.Display(false);
    contact.ShowCheckPhoneDialog(
        Outlook.OlContactPhoneNumber.
        olContactPhoneBusiness);
}
```

## <a name="see-also"></a><span data-ttu-id="69af0-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69af0-115">See also</span></span>

- [<span data-ttu-id="69af0-116">Kontakte</span><span class="sxs-lookup"><span data-stu-id="69af0-116">Contacts</span></span>](contacts.md)

