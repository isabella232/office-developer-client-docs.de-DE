---
title: Erstellen eines benutzerdefinierten Kontaktelements
TOCTitle: Create a custom Contact item
ms:assetid: 24b2a104-a0a7-469b-9676-a07cab613f59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184596(v=office.15)
ms:contentKeyID: 55119831
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4261fffef0934e01cbfbcc7068377cc392af178c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361054"
---
# <a name="create-a-custom-contact-item"></a><span data-ttu-id="7d38d-102">Erstellen eines benutzerdefinierten Kontaktelements</span><span class="sxs-lookup"><span data-stu-id="7d38d-102">Create a custom Contact item</span></span>

<span data-ttu-id="7d38d-103">In diesem Beispiel wird gezeigt, wie ein benutzerdefiniertes Kontaktelement erstellt wird und sowohl vordefinierte als auch benutzerdefinierte Eigenschaften festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7d38d-103">This example shows how to create a custom contact item and set both predefined and user-defined properties.</span></span>

## <a name="example"></a><span data-ttu-id="7d38d-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7d38d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="7d38d-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="7d38d-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="7d38d-106">Ein [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\))-Objekt stellt einen Kontakt im Ordner „Kontakte“ dar und verfügt über mehr als 100 integrierte Eigenschaften, wie z. B. [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) und [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="7d38d-106">A [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object represents a contact in the Contacts folder, and has more than 100 built-in properties such as [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) and [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)).</span></span> <span data-ttu-id="7d38d-107">Manchmal sind die integrierten Eigenschaften nicht ausreichend, und Sie müssen benutzerdefinierte Eigenschaften hinzufügen, wozu Sie die [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\))-Sammlung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7d38d-107">Sometimes, the built-in properties are not sufficient and you need to add custom properties, which you can do by using the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection.</span></span>

<span data-ttu-id="7d38d-108">Im folgenden Codebeispiel erstellt CreateCustomItem erstellt ein benutzerdefiniertes **ContactItem**-Objekt, gibt ihm den Namen „Shoe Store“ und ruft die [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\))-Methode auf, um es einem Ordner mit dem Namen „Shoe Store“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7d38d-108">In the following code example, CreateCustomItem creates a custom **ContactItem** object, names it "Shoe Store", and calls the [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) method to add it to a folder named "Shoe Store".</span></span> <span data-ttu-id="7d38d-109">CreateCustomItem ruft zunächst den Ordner „Shoe Store“ mithilfe der [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\))-Methode ab.</span><span class="sxs-lookup"><span data-stu-id="7d38d-109">CreateCustomItem first gets the "Shoe Store" folder by using the [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) method.</span></span> <span data-ttu-id="7d38d-110">Der Ordner „Shoe Store“ ist ein Unterordner des Standardordners für Kontakte.</span><span class="sxs-lookup"><span data-stu-id="7d38d-110">The "Shoe Store" folder is a subfolder of the default Contacts folder.</span></span> <span data-ttu-id="7d38d-111">CreateCustomItem legt dann die Eigenschaften **FirstName** und **LastName** fest und erstellt eine benutzerdefinierte Eigenschaft („Shoe Size“) mithilfe der **UserProperties**-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="7d38d-111">CreateCustomItem then sets the **FirstName** and **LastName** properties, and creates a user-defined property ("Shoe Size") by using the **UserProperties** collection.</span></span>

<span data-ttu-id="7d38d-112">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="7d38d-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7d38d-113">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7d38d-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7d38d-114">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="7d38d-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateCustomItem()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Folders[
        "Shoe Store"] as Outlook.Folder;
    Outlook.ContactItem contact =
        folder.Items.Add(
        "IPM.Contact.Shoe Store") as Outlook.ContactItem;
    contact.FirstName = "Michael";
    contact.LastName = "Affronti";
    contact.UserProperties["Shoe Size"].Value = "9";
    contact.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="7d38d-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d38d-115">See also</span></span>

- [<span data-ttu-id="7d38d-116">Kontakte</span><span class="sxs-lookup"><span data-stu-id="7d38d-116">Contacts</span></span>](contacts.md)

