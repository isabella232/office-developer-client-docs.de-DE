---
title: Suchen und Abrufen von Elementen in einer aggregierten Ansicht
TOCTitle: Search and obtain items in an aggregated view
ms:assetid: 1a875dc8-dd52-4e9c-b292-5f6ba3d7a940
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184592(v=office.15)
ms:contentKeyID: 55119925
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 540557973d395c23d26a87502ed6ba43176a0a3c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407576"
---
# <a name="search-and-obtain-items-in-an-aggregated-view"></a><span data-ttu-id="c7679-102">Suchen und Abrufen von Elementen in einer aggregierten Ansicht</span><span class="sxs-lookup"><span data-stu-id="c7679-102">Search and Obtain Items in an Aggregated View</span></span>

<span data-ttu-id="c7679-103">In diesem Beispiel wird gezeigt, wie in mehreren Ordnern nach Elementen gesucht wird und wie diese Elemente in einer aggregierten Tabellenansicht gespeichert und zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c7679-103">This example shows how to search for items in multiple folders and stores and to return those items in an aggregated table view.</span></span>

## <a name="example"></a><span data-ttu-id="c7679-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c7679-104">Example</span></span>

<span data-ttu-id="c7679-p101">Die [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) -Methode des [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) -Objekts kann in einer aggregierten Ansicht ein [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) -Objekt zurückgeben, das Elemente aus einem oder mehreren Ordnern in einem oder mehreren Speichern enthält. Dies ist besonders dann nützlich, wenn Sie auf die von einer Suche (z. B. nach allen E-Mail-Elementen in einem Speicher) zurückgegebenen Elemente zugreifen möchten. In diesem Thema wird anhand eines Beispiels veranschaulicht, wie Sie mithilfe der Funktion **Sofortsuche** nach allen als wichtig gekennzeichneten Elementen suchen, die vom Vorgesetzten des aktuellen Benutzers gesendet wurden, und dann den Betreff jedes Suchergebnisses anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c7679-p101">The [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method of the [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) object can return, in an aggregated view, a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object that contains items from one or more folders in the same store or spanning over multiple stores. This is particularly useful when you want to access items returned from a search (for example, a search on all mail items in a store). This topic shows an example of how to use **Instant Search** to search for all items received from the manager of the current user that are marked important, and then display the subject of each search result.</span></span>

<span data-ttu-id="c7679-108">Im folgenden Codebeispiel prüft die **GetItemsInView**-Methode, ob das Konto des aktuellen Benutzers für den primären Zustellungsspeicher ein Exchange-Konto ist, ob der aktuelle Benutzer einen Vorgesetzten hat und ob **Sofortsuche** im Standardspeicher der Sitzung ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c7679-108">In the following code example, the  \*\*\*\* method checks whether the current user's primary delivery store account is an Exchange account, whether the current user has a manager, and whether **Instant Search** is operational in the default store of the session.</span></span> <span data-ttu-id="c7679-109">Da für die Suche die [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) -Methode des [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) -Objekts verwendet wird und das Suchergebnis mithilfe der **GetTable**-Methode abgerufen wird, erstellt **GetItemsInView** ein **Explorer**-Objekt, zeigt den Posteingang in diesem Objekt an und richtet anhand von diesem die Suche ein.</span><span class="sxs-lookup"><span data-stu-id="c7679-109">Because the search relies on the [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method of the [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object, and the search result is obtained by using the **GetTable** method,  \*\*\*\* creates an **Explorer** object, displays the Inbox in this object, and uses it to set up the search.</span></span> 

<span data-ttu-id="c7679-110">**GetItemsInView** durchsucht alle Ordner vom Typ [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) nach Elementen, die vom Vorgesetzten des aktuellen Benutzers stammen und als wichtig markiert sind.</span><span class="sxs-lookup"><span data-stu-id="c7679-110">\*\*\*\* searches all folders of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) type for items from the current user's manager that are marked as important.</span></span> <span data-ttu-id="c7679-111">Nachdem **GetItemsInView** die [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) -Methode aufgerufen hat, werden alle Suchergebnisse im Explorer angezeigt, darunter auch Elemente aus anderen Ordnern und Speichern, die die Suchkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c7679-111">After  \*\*\*\* calls the [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method, any search results are displayed in the explorer, including items from other folders and stores that meet the search criteria.</span></span> <span data-ttu-id="c7679-112">**GetItemsInView** ruft ein **TableView**-Objekt ab, das diese Exploreransicht der Suchergebnisse enthält.</span><span class="sxs-lookup"><span data-stu-id="c7679-112">\*\*\*\* gets a **TableView** object that contains this explorer view of the search results.</span></span> <span data-ttu-id="c7679-113">Mithilfe der **GetTable**-Methode dieses **TableView**-Objekts ruft **GetItemsInView** dann ein **Table**-Objekt ab, das die von der Suche zurückgegebenen aggregierten Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="c7679-113">By using the **GetTable** method of this **TableView** object,  \*\*\*\* then gets a **Table** object that contains the aggregated items returned from the search.</span></span> <span data-ttu-id="c7679-114">Und schließlich zeigt **GetItemsInView** die Betreffspalte jeder Zeile des **Table**-Objekts an, die ein Element in den Suchergebnissen darstellt.</span><span class="sxs-lookup"><span data-stu-id="c7679-114">Finally  \*\*\*\* displays the subject column of each row of the **Table** object that represents an item in the search results.</span></span>

<span data-ttu-id="c7679-115">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="c7679-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="c7679-116">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c7679-116">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="c7679-117">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="c7679-117">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetItemsInView()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;

    // Check whether the current user uses the Exchange Server.
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();

        // Check whether the current user has a manager.
        if (manager != null)
        {
            string managerName = manager.Name;

            // Check whether Instant Search is enabled and 
            // operational in the default store.
            if (Application.Session.DefaultStore.IsInstantSearchEnabled)
            {
                Outlook.Folder inbox =
                    Application.Session.GetDefaultFolder(
                    Outlook.OlDefaultFolders.olFolderInbox);

                // Create a new explorer to display the Inbox as
                // the current folder.
                Outlook.Explorer explorer =
                    Application.Explorers.Add(inbox,
                    Outlook.OlFolderDisplayMode.olFolderDisplayNormal);

                // Make the new explorer visible.
                explorer.Display;

                // Search for items from the manager marked important, 
                // from all folders of the same item type as the current folder, 
                // which is the MailItem item type.
                string searchFor =
                    "from:" + "\"" + managerName 
                    + "\"" + " importance:high";
                explorer.Search(searchFor,
                    Outlook.OlSearchScope.olSearchScopeAllFolders);

                // Any search results are displayed in that new explorer
                // in an aggregated table view.
                Outlook.TableView tableView = 
                    explorer.CurrentView as Outlook.TableView;

                // Use GetTable of that table view to obtain items in that
                // aggregated view in a Table object.
                Outlook.Table table = tableView.GetTable();
                while (!table.EndOfTable)
                {
                    // Then display each row in the Table object
                    // that represents an item in the search results.
                    Outlook.Row nextRow = table.GetNextRow();
                    Debug.WriteLine(nextRow["Subject"]);
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="c7679-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7679-118">See also</span></span>

- [<span data-ttu-id="c7679-119">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="c7679-119">Search and Filter</span></span>](search-and-filter.md)

