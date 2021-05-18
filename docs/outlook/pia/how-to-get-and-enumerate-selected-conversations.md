---
title: Abrufen und Aufzählen von ausgewählten Unterhaltungen
TOCTitle: Get and enumerate selected conversations
ms:assetid: 835312ea-2b29-49a5-b128-f69cf8d4427c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184621(v=office.15)
ms:contentKeyID: 55119833
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d71fc1d582abebc8cb00f4885ec5b5ba348228c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320314"
---
# <a name="get-and-enumerate-selected-conversations"></a><span data-ttu-id="91bef-102">Abrufen und Aufzählen von ausgewählten Unterhaltungen</span><span class="sxs-lookup"><span data-stu-id="91bef-102">Get and enumerate selected conversations</span></span>

<span data-ttu-id="91bef-103">In diesem Beispiel werden ausgewählte Unterhaltungen mithilfe der [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\))-Methode abgerufen und aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="91bef-103">This example obtains and enumerates selected conversations by using the [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="91bef-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="91bef-104">Example</span></span>

<span data-ttu-id="91bef-p101">In Microsoft Outlook können Elemente im Posteingang nach Unterhaltungen angezeigt werden. Wenn ein Benutzer im Posteingang eine Auswahl trifft, können Sie diese programmgesteuert einschließlich Unterhaltungskopfzeilen und -elementen abrufen. Das Codebeispiel in diesem Thema zeigt, wie eine Auswahl im Posteingang abgerufen wird und die E-Mail-Elemente in jeder Unterhaltung der Auswahl aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="91bef-p101">Microsoft Outlook can be set to display items in the Inbox by conversation. If a user makes a selection in the Inbox, you can obtain the selection programmatically, including conversation headers and conversation items. The code example in this topic shows how to obtain a selection in the Inbox and enumerate the mail items in each conversation in the selection.</span></span>

<span data-ttu-id="91bef-108">Das Beispiel enthält eine Methode: DemoConversationHeadersFromSelection.</span><span class="sxs-lookup"><span data-stu-id="91bef-108">The example contains one method, DemoConversationHeadersFromSelection.</span></span> <span data-ttu-id="91bef-109">Die Methode legt die aktuelle Ansicht auf den Posteingang fest und prüft dann, ob es sich bei der aktuellen Ansicht um eine Tabellenansicht handelt, in der Unterhaltungen nach Datum sortiert angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="91bef-109">The method sets the current view to the Inbox, and then checks whether the current view is a table view that displays conversations sorted by date.</span></span> <span data-ttu-id="91bef-110">Zum Abrufen einer Auswahl, einschließlich ausgewählter [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\))-Objekte, verwendet DemoConversationHeadersFromSelection die **GetSelection**-Methode des [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\))-Objekts, wobei die [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) -Konstante als Argument angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="91bef-110">To obtain a selection, including any selected [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)) objects, DemoConversationHeadersFromSelection uses the **GetSelection** method of the [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) object, specifying the [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) constant as an argument.</span></span> <span data-ttu-id="91bef-111">Wenn Unterhaltungskopfzeilen ausgewählt wurden, verwendet DemoConversationHeadersFromSelection das [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\))-Objekt zum Aufzählen der Elemente in jeder ausgewählten Unterhaltung und zeigt dann den Betreff der Unterhaltungselemente an, die [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))-Objekte darstellen.</span><span class="sxs-lookup"><span data-stu-id="91bef-111">If conversation headers are selected, DemoConversationHeadersFromSelection uses the [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\)) object to enumerate items in each selected conversation, and then displays the subject of those conversation items that are [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) objects.</span></span>

<span data-ttu-id="91bef-112">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="91bef-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="91bef-113">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="91bef-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="91bef-114">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="91bef-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoConversationHeadersFromSelection()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType ==
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view =
            inbox.CurrentView as Outlook.TableView;
        if (view.ShowConversationByDate == true)
        {
            Outlook.Selection selection =
                Application.ActiveExplorer().Selection;
            Debug.WriteLine("Selection.Count = " + selection.Count);
            // Call GetSelection to create a Selection object
            // that contains ConversationHeader objects.
            Outlook.Selection convHeaders =
                selection.GetSelection(
                Outlook.OlSelectionContents.olConversationHeaders)
                as Outlook.Selection;
            Debug.WriteLine("Selection.Count (ConversationHeaders) = " 
                + convHeaders.Count);
            if (convHeaders.Count >= 1)
            {
                foreach (Outlook.ConversationHeader convHeader in convHeaders)
                {
                    // Enumerate the items in the ConversationHeader.
                    Outlook.SimpleItems items = convHeader.GetItems();
                    for (int i = 1; i <= items.Count; i++)
                    {
                        // Enumerate only MailItems in this example.
                        if (items[i] is Outlook.MailItem)
                        {
                            Outlook.MailItem mail = 
                                items[i] as Outlook.MailItem;
                            Debug.WriteLine(mail.Subject 
                                + " Received:" + mail.ReceivedTime);
                        }
                    }
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="91bef-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91bef-115">See also</span></span>

- [<span data-ttu-id="91bef-116">Unterhaltungen</span><span class="sxs-lookup"><span data-stu-id="91bef-116">Conversations</span></span>](conversations.md)

