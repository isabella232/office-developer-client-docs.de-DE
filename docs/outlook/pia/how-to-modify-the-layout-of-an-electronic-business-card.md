---
title: Ändern des Layouts einer elektronischen Visitenkarte
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184653(v=office.15)
ms:contentKeyID: 55119838
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7f85324b31ae865c69e2c40806d9654a0b443f4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320181"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a><span data-ttu-id="39141-102">Ändern des Layouts einer elektronischen Visitenkarte</span><span class="sxs-lookup"><span data-stu-id="39141-102">Modify the layout of an electronic business card</span></span>

<span data-ttu-id="39141-103">Dieses Beispiel zeigt, wie das Layout einer elektronischen Visitenkarte mithilfe der [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\))-Eigenschaft der [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\))-Schnittstelle geändert wird.</span><span class="sxs-lookup"><span data-stu-id="39141-103">This example shows how to modify the layout of an electronic business card by using the [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) property of the [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) interface.</span></span>

## <a name="example"></a><span data-ttu-id="39141-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="39141-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="39141-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="39141-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="39141-106">Eine elektronische Visitenkarte enthält eine Ansicht eines Kontakts, in der bestimmte Informationen aus einem Kontakt erfasst sind.</span><span class="sxs-lookup"><span data-stu-id="39141-106">An electronic business card provides a contact view that captures specific information from that contact.</span></span> <span data-ttu-id="39141-107">Die **ContactItem**-Schnittstelle bietet bestimmte Member, die elektronische Visitenkarten betreffen.</span><span class="sxs-lookup"><span data-stu-id="39141-107">The **ContactItem** interface provides specific members that pertain to electronic business cards.</span></span> <span data-ttu-id="39141-108">Diese Member sind **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)), [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)), [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)), [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)), [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)) und [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="39141-108">These members are **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)), [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)), [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)), [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)), [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)), and [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)).</span></span>

<span data-ttu-id="39141-109">Im folgenden Codebeispiel ändert BusinessCardLayoutExample das Layout einer elektronischen Visitenkarte, indem zuerst ein angegebenes **ContactItem**-Objekt abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="39141-109">In the following code example, BusinessCardLayoutExample modifies the layout of an electronic business card by first obtaining a specified **ContactItem** object.</span></span> <span data-ttu-id="39141-110">In diesem Fall stellt das **ContactItem**-Objekt einen Kontakt dar, dessen [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\))-Eigenschaft den Wert „Melissa MacBeth“ hat.</span><span class="sxs-lookup"><span data-stu-id="39141-110">In this case, the **ContactItem** is a contact with the value of the [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) property equal to “Melissa MacBeth”.</span></span> <span data-ttu-id="39141-111">Anschließend erstellt BusinessCardLayoutExample eine XML-Dokumentklasse [XmlDocument](https://msdn.microsoft.com/en-us/library/6kza7w4k) und ruft dann das Layoutattribut der Klasse in einer Zeichenfolge ab, wobei der **BusinessCardLayoutXML**-Wert für das **ContactItem-Objekt** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39141-111">Next, BusinessCardLayoutExample creates an XML document class [XmlDocument](https://msdn.microsoft.com/en-us/library/6kza7w4k), and then gets the layout attribute of this class in a string by using the **BusinessCardLayoutXML** value for the **ContactItem** object.</span></span> <span data-ttu-id="39141-112">Das Kartenlayout wird dann von links- zu rechtsbündig geändert.</span><span class="sxs-lookup"><span data-stu-id="39141-112">The card layout is then changed from left-aligned to right-aligned.</span></span>

<span data-ttu-id="39141-113">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="39141-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="39141-114">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="39141-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="39141-115">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="39141-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void BusinessCardLayoutExample()
{
    Outlook.ContactItem contact =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Subject] = Melissa MacBeth'")
        as Outlook.ContactItem;
    if (contact != null)
    {
        XmlDocument doc = new XmlDocument();
        doc.LoadXml(contact.BusinessCardLayoutXml);
        XmlElement root = doc.DocumentElement;
        string layoutValue = root.GetAttribute("layout");
        if (layoutValue == "left")
        {
            root.SetAttribute("layout", "right");
            contact.BusinessCardLayoutXml = doc.OuterXml;
            contact.Save();
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="39141-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39141-116">See also</span></span>

- [<span data-ttu-id="39141-117">Elektronische Visitenkarten</span><span class="sxs-lookup"><span data-stu-id="39141-117">Electronic business cards</span></span>](electronic-business-cards.md)

