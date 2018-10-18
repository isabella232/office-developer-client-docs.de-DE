---
title: Abrufen und Aufzählen von ausgewählten Unterhaltungen
TOCTitle: Get and enumerate selected conversations
ms:assetid: 835312ea-2b29-49a5-b128-f69cf8d4427c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184621(v=office.15)
ms:contentKeyID: 55119833
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: cf36003f183c9ddfe40cb2c27a9feab2962324d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405595"
---
# <a name="get-and-enumerate-selected-conversations"></a>Abrufen und Aufzählen von ausgewählten Unterhaltungen

In diesem Beispiel werden ausgewählte Unterhaltungen mithilfe der [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\))-Methode abgerufen und aufgezählt.

## <a name="example"></a>Beispiel

In Microsoft Outlook können Elemente im Posteingang nach Unterhaltungen angezeigt werden. Wenn ein Benutzer im Posteingang eine Auswahl trifft, können Sie diese programmgesteuert einschließlich Unterhaltungskopfzeilen und -elementen abrufen. Das Codebeispiel in diesem Thema zeigt, wie eine Auswahl im Posteingang abgerufen wird und die E-Mail-Elemente in jeder Unterhaltung der Auswahl aufgezählt werden.

Das Beispiel enthält eine Methode: DemoConversationHeadersFromSelection. Die Methode legt die aktuelle Ansicht auf den Posteingang fest und prüft dann, ob es sich bei der aktuellen Ansicht um eine Tabellenansicht handelt, in der Unterhaltungen nach Datum sortiert angezeigt werden. Zum Abrufen einer Auswahl, einschließlich ausgewählter [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\))-Objekte, verwendet DemoConversationHeadersFromSelection die **GetSelection**-Methode des [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\))-Objekts, wobei die [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) -Konstante als Argument angegeben wird. Wenn Unterhaltungskopfzeilen ausgewählt wurden, verwendet DemoConversationHeadersFromSelection das [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\))-Objekt zum Aufzählen der Elemente in jeder ausgewählten Unterhaltung und zeigt dann den Betreff der Unterhaltungselemente an, die [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))-Objekte darstellen.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

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

## <a name="see-also"></a>Siehe auch

- [Unterhaltungen](conversations.md)

