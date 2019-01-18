---
title: Verwenden der Sofortsuche zum Durchsuchen aller Ordner und aller Stores nach einem Ausdruck im Betreff
TOCTitle: Use instant search to search all folders and all stores for a phrase in the subject
ms:assetid: d3152bfa-6e7d-4b68-8c7e-e2e155a92b49
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424478(v=office.15)
ms:contentKeyID: 55119923
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 07b0ba7a1d488dc1c7e1fcf0e9ae487b04b88755
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709439"
---
# <a name="use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject"></a><span data-ttu-id="53bf3-102">Verwenden der Sofortsuche zum Durchsuchen aller Ordner und aller Stores nach einem Ausdruck im Betreff</span><span class="sxs-lookup"><span data-stu-id="53bf3-102">Use instant search to search all folders and all stores for a phrase in the subject</span></span>

<span data-ttu-id="53bf3-103">In diesem Beispiel werden mithilfe der Sofortsuche alle Ordner und alle Speicher nach einem Ausdruck im Betreff durchsucht und die gefundenen Elemente anschließend in einem Explorer-Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="53bf3-103">This example uses Instant Search to search all folders and all stores for a phrase in the subject, and then displays the items in an explorer window.</span></span>

## <a name="example"></a><span data-ttu-id="53bf3-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="53bf3-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="53bf3-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="53bf3-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="53bf3-106">Die Sofortsuche ist ein Feature von Microsoft Outlook, mit dem durch Ausgeben von Abfragen, die Ergebnisse basierend auf dem Inhalt zurückgeben, Suchvorgänge ausführen können.</span><span class="sxs-lookup"><span data-stu-id="53bf3-106">Instant Search is a feature of Microsoft Outlook that enables you to search by issuing queries that return results based on the content.</span></span> <span data-ttu-id="53bf3-107">Nachdem die Abfrage verarbeitet wurde, können die Ergebnisse in einer Vielzahl von Objekten zurückgegeben werden, einschließlich des [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekts, der [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\))-Auflistung und des [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\))-Objekts.</span><span class="sxs-lookup"><span data-stu-id="53bf3-107">Once your query has been processed, the results can be returned in a variety of objects, including the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection, and the [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="53bf3-108">Sie können Code mithilfe der Advanced Query Syntax (AQS), die von der Microsoft Windows-Desktopsuche angeboten wird, Code schreiben, der die Sofortsuche verwendet.</span><span class="sxs-lookup"><span data-stu-id="53bf3-108">You can write code that uses Instant Search by using the Advanced Query Syntax (AQS) that is offered by Microsoft Windows Desktop Search.</span></span> <span data-ttu-id="53bf3-109">AQS ist eine der drei Abfragesprachen, die Outlook unterstützt.</span><span class="sxs-lookup"><span data-stu-id="53bf3-109">AQS is one of three query languages that Outlook supports.</span></span> <span data-ttu-id="53bf3-110">Sie ist leistungsstark, aber beschränkt auf die [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\))-Methode des [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\))-Objekts.</span><span class="sxs-lookup"><span data-stu-id="53bf3-110">It is powerful, but limited to the [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method of the [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object.</span></span> <span data-ttu-id="53bf3-111">Sie können AQS nicht verwenden, um eine Einschränkung für **Table**- oder **Item**-Objekte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="53bf3-111">You cannot use AQS to provide a restriction for **Table** or **Item** objects.</span></span> <span data-ttu-id="53bf3-112">Außerdem können die von einer AQS-Abfrage zurückgegebenen Ergebnisse nur in der Outlook-Benutzeroberfläche zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="53bf3-112">In addition, the results returned by an AQS query can be displayed only in the Outlook user interface.</span></span> <span data-ttu-id="53bf3-113">In der folgenden Tabelle sind die drei Abfragesprachen aufgeführt, die Outlook unterstützt. In diesem Thema wird jedoch nur die Verwendung von AQS veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="53bf3-113">The following table lists the three query languages that Outlook supports; however, this topic will illustrate the use of only AQS.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53bf3-114">Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="53bf3-114">Query language</span></span></p></th>
<th><p><span data-ttu-id="53bf3-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53bf3-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53bf3-116">AQS</span><span class="sxs-lookup"><span data-stu-id="53bf3-116">AQS</span></span></p></td>
<td><p><span data-ttu-id="53bf3-117">AQS wird von der Windows-Desktopsuche verwendet und ist die Abfragesprache für das Feature Sofortsuche in Outlook.</span><span class="sxs-lookup"><span data-stu-id="53bf3-117">AQS is used by Windows Desktop Search and is the query language for the Instant Search feature in Outlook.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53bf3-118">DASL</span><span class="sxs-lookup"><span data-stu-id="53bf3-118">DASL</span></span></p></td>
<td><p><span data-ttu-id="53bf3-p102">Die Abfragesprache DAV Search and Locating (DASL) basiert auf der Microsoft Exchange-Implementierung von DASL in Outlook. Mit DASL können Ergebnisse im <b>Table</b>-Objekt zurückgegeben werden. </span><span class="sxs-lookup"><span data-stu-id="53bf3-p102">DAV Search and Locating (DASL) query language is based on the Microsoft Exchange implementation of DASL in Outlook. DASL can be used to return results in the <b>Table</b> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53bf3-121">Jet</span><span class="sxs-lookup"><span data-stu-id="53bf3-121">Jet</span></span></p></td>
<td><p><span data-ttu-id="53bf3-p103">Die Abfragesprache Jet stellt eine einfache Abfragesprache für Outlook dar und baut auf dem Microsoft Jet-Ausdrucksdienst auf. Mit Jet werden Filterzeichenfolgen für die <b>Restrict</b>-Methoden der <b>Items</b>-Auflistung und des <b>Table</b>-Objekts erstellt.</span><span class="sxs-lookup"><span data-stu-id="53bf3-p103">Jet query language provides a simple query language for Outlook, and is based on the Microsoft Jet Expression Service. Jet is used to create filter strings for the <b>Restrict</b> methods of the <b>Items</b> collection and the <b>Table</b> object.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="53bf3-124">Im folgenden Codebeispiel ruft DemoInstantSearch mithilfe der [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\))-Eigenschaft des [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\))-Objekts alle E-Mail-Ordner in allen Speichern ab, in denen die Indizierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="53bf3-124">In the following code example, DemoInstantSearch gets all mail folders in all stores where indexing is enabled by using the [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) property of the [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object.</span></span> <span data-ttu-id="53bf3-125">Anschließend wird mit der **Search**-Methode des **Explorer**-Objekts nach allen Elementen gefiltert, die den genauen Ausdruck "Office 2007" im Betreff enthalten und die im letzten Monat empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="53bf3-125">It then uses the **Search** method of the **Explorer** object to filter for all items that contain the exact phrase “Office 2007” in the subject and that have been received in the last month.</span></span> <span data-ttu-id="53bf3-126">Die Ergebnisse der Suche werden schließlich in einem separaten Explorerfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="53bf3-126">The results of the search are finally displayed in a separate explorer window.</span></span>

<span data-ttu-id="53bf3-127">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="53bf3-127">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="53bf3-128">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="53bf3-128">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="53bf3-129">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="53bf3-129">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoInstantSearch()
{
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        Outlook.Explorer explorer = Application.Explorers.Add(
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            as Outlook.Folder,
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        string filter = "subject:" +
            "\"" + "Office 2007" + "\"" +
            " received:(last month)";
        explorer.Search(filter,
            Outlook.OlSearchScope.olSearchScopeAllFolders);
        explorer.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="53bf3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53bf3-130">See also</span></span>

- [<span data-ttu-id="53bf3-131">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="53bf3-131">Search and filter</span></span>](search-and-filter.md)

