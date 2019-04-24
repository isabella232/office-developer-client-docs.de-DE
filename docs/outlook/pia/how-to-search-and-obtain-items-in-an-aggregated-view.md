---
title: Suchen und Abrufen von Elementen in einer aggregierten Ansicht
TOCTitle: Search and obtain items in an aggregated view
ms:assetid: 1a875dc8-dd52-4e9c-b292-5f6ba3d7a940
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184592(v=office.15)
ms:contentKeyID: 55119925
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92f99069dae2976a00ac075f605754fe8704ae60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342763"
---
# <a name="search-and-obtain-items-in-an-aggregated-view"></a>Suchen und Abrufen von Elementen in einer aggregierten Ansicht

In diesem Beispiel wird gezeigt, wie in mehreren Ordnern nach Elementen gesucht wird und wie diese Elemente in einer aggregierten Tabellenansicht gespeichert und zurückgegeben werden.

## <a name="example"></a>Beispiel

Die [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) -Methode des [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) -Objekts kann in einer aggregierten Ansicht ein [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) -Objekt zurückgeben, das Elemente aus einem oder mehreren Ordnern in einem oder mehreren Speichern enthält. Dies ist besonders dann nützlich, wenn Sie auf die von einer Suche (z. B. nach allen E-Mail-Elementen in einem Speicher) zurückgegebenen Elemente zugreifen möchten. In diesem Thema wird anhand eines Beispiels veranschaulicht, wie Sie mithilfe der Funktion **Sofortsuche** nach allen als wichtig gekennzeichneten Elementen suchen, die vom Vorgesetzten des aktuellen Benutzers gesendet wurden, und dann den Betreff jedes Suchergebnisses anzeigen.

Im folgenden Codebeispiel prüft die **GetItemsInView**-Methode, ob das Konto des aktuellen Benutzers für den primären Zustellungsspeicher ein Exchange-Konto ist, ob der aktuelle Benutzer einen Vorgesetzten hat und ob **Sofortsuche** im Standardspeicher der Sitzung ordnungsgemäß funktioniert. Da für die Suche die [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) -Methode des [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) -Objekts verwendet wird und das Suchergebnis mithilfe der **GetTable**-Methode abgerufen wird, erstellt **GetItemsInView** ein **Explorer**-Objekt, zeigt den Posteingang in diesem Objekt an und richtet anhand von diesem die Suche ein. 

**GetItemsInView** durchsucht alle Ordner vom Typ [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) nach Elementen, die vom Vorgesetzten des aktuellen Benutzers stammen und als wichtig markiert sind. Nachdem **GetItemsInView** die [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) -Methode aufgerufen hat, werden alle Suchergebnisse im Explorer angezeigt, darunter auch Elemente aus anderen Ordnern und Speichern, die die Suchkriterien erfüllen. **GetItemsInView** ruft ein **TableView**-Objekt ab, das diese Exploreransicht der Suchergebnisse enthält. Mithilfe der **GetTable**-Methode dieses **TableView**-Objekts ruft **GetItemsInView** dann ein **Table**-Objekt ab, das die von der Suche zurückgegebenen aggregierten Elemente enthält. Und schließlich zeigt **GetItemsInView** die Betreffspalte jeder Zeile des **Table**-Objekts an, die ein Element in den Suchergebnissen darstellt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

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

## <a name="see-also"></a>Siehe auch

- [Suchen und Filtern](search-and-filter.md)

