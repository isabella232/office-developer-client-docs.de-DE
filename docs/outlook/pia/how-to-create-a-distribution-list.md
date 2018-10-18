---
title: Erstellen einer Verteilerliste
TOCTitle: Create a distribution list
ms:assetid: c1fdbf3d-9669-4721-aabf-e8a332b82e0e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184637(v=office.15)
ms:contentKeyID: 55119841
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 19b282a3b3e756814aa2add07cda4be7609206ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407135"
---
# <a name="create-a-distribution-list"></a><span data-ttu-id="5b2af-102">Erstellen einer Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="5b2af-102">Create a distribution list</span></span>

<span data-ttu-id="5b2af-103">In diesem Beispiel wird veranschaulicht, wie eine Verteilerliste erstellt und dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5b2af-103">This example shows how to create a distribution list and display it to the user.</span></span>

## <a name="example"></a><span data-ttu-id="5b2af-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5b2af-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="5b2af-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="5b2af-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="5b2af-106">Im folgenden Codebeispiel wird von CreateDistributionList eine Verteilerliste erstellt, indem durch Aufrufen der [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\))-Methode ein [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\))-Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5b2af-106">In the following code example,   creates a distribution list by calling the CreateItem(OlItemType) method to create a DistListItem object.</span></span> <span data-ttu-id="5b2af-107">Anschließend wird ein [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt erstellt und die [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\))-Methode aufgerufen, um alle Kontakte im Standardordner für Kontakte zu finden, deren Wert der [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\))-Eigenschaft "Top Customer" lautet und deren Wert der [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\))-Eigenschaft nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="5b2af-107">Next it creates a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, and calls the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) method to find all contacts in the default Contacts folder for which the [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) property value is "Top Customer" and the [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) property value is not empty.</span></span> <span data-ttu-id="5b2af-108">Nachdem alle Kontakte identifiziert wurden, wird der **Email1Address**-Name wird als eine Spalte zur **Tabelle** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5b2af-108">Once all contacts are identified, the **Email1Address** name is added as a column to the **Table**.</span></span> <span data-ttu-id="5b2af-109">Dann erstellt CreateDistributionList ein [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\))-Objekt mithilfe der [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\))-Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\))-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5b2af-109"> then creates a Recipient object by using the CreateRecipient(String) method from the NameSpace object.</span></span> <span data-ttu-id="5b2af-110">Schließlich zeigt CreateDistributionList dem Benutzer die Verteilerliste "Top Customers" an.</span><span class="sxs-lookup"><span data-stu-id="5b2af-110"> finally displays the "Top Customers" distribution list to the user.</span></span>

> [!NOTE] 
> <span data-ttu-id="5b2af-111">Sie müssen ein aufgelöstes **Recipient**-Objekt als Parameter für die [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15))-Methode des [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\))-Objekts übergeben.</span><span class="sxs-lookup"><span data-stu-id="5b2af-111">[!C# NOTE] You must pass a resolved **Recipient** object as a parameter to the [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) method of the [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)) object.</span></span> <span data-ttu-id="5b2af-112">Zum Auflösen eines **Empfänger**-Objekts verwenden Sie die [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15))-Methode.</span><span class="sxs-lookup"><span data-stu-id="5b2af-112">To resolve a **Recipient** object, use the [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)) method.</span></span>

<span data-ttu-id="5b2af-113">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="5b2af-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="5b2af-114">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5b2af-114">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="5b2af-115">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="5b2af-115">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateDistributionList()
{
    Outlook.DistListItem distList = Application.CreateItem(
        Outlook.OlItemType.olDistributionListItem)
        as Outlook.DistListItem;
    distList.Subject = "Top Customers";
    //Find top customer category in Contacts folder
    string filter = "[Categories] = 'Top Customer'"
        + " AND [Email1Address] <> ''";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderContacts).
        GetTable(filter, Outlook.OlTableContents.olUserItems);
    table.Columns.Add("Email1Address");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Outlook.Recipient recip =
            Application.Session.CreateRecipient(
            nextRow["Email1Address"].ToString());
        //Resolve the Recipient before calling AddMember
        recip.Resolve();
        distList.AddMember(recip);
    }
    distList.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="5b2af-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b2af-116">See also</span></span>

- [<span data-ttu-id="5b2af-117">Exchange-Benutzer</span><span class="sxs-lookup"><span data-stu-id="5b2af-117">Exchange Users</span></span>](exchange-users.md)

