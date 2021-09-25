---
title: Abrufen und Anzeigen von Elementen in einer Unterhaltung
TOCTitle: Get and display items in a conversation
ms:assetid: 8f30a7cb-0949-46d7-bc51-2d93dbb22bf8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184625(v=office.15)
ms:contentKeyID: 55119832
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5f130edfbfb742f727e9b74779736b380547ff02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623684"
---
# <a name="get-and-display-items-in-a-conversation"></a>Abrufen und Anzeigen von Elementen in einer Unterhaltung

In diesem Beispiel wird veranschaulicht, wie E-Mail-Elemente in einer Unterhaltung abgerufen und angezeigt werden.

## <a name="example"></a>Beispiel

Im folgenden Codebeispiel ruft DemoConversation ein [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))-Objekt ab und ermittelt dann den Speicher des **MailItem**-Objekts unter Verwendung der [Store](https://msdn.microsoft.com/library/bb609093\(v=office.15\))-Eigenschaft des [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekts. DemoConversation überprüft dann, ob die [IsConversationEnabled](https://msdn.microsoft.com/library/ff185030\(v=office.15\))-Eigenschaft auf **true** festgelegt it; wenn sie auf **true** festgelegt ist, ruft das Codebeispiel das [Conversation](https://msdn.microsoft.com/library/ff184711\(v=office.15\))-Objekt mithilfe der [GetConversation()](https://msdn.microsoft.com/library/ff184974\(v=office.15\))-Methode ab. Wenn das **Conversation**-Objekt kein Nullverweis ist, ruft das Beispiel das zugeordnete [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt mithilfe der [GetTable()](https://msdn.microsoft.com/library/ff185184\(v=office.15\))-Methode ab, das jedes Element in der Unterhaltung enthält. 

Im Beispiel wird dann jedes Element in der **Tabelle** aufgeführt und EnumerateConversation für jedes Element aufgerufen, um auf die untergeordneten Knoten jedes Elements zuzugreifen. EnumerateConversation verwendet ein **Conversation**-Objekt und ruft die untergeordneten Knoten mit der [GetChildren(Object)](https://msdn.microsoft.com/library/ff184854\(v=office.15\))-Methode auf. EnumerateConversation wird rekursiv aufgerufen, bis keine weiteren untergeordneten Knoten vorhanden sind. Jedes Element der Unterhaltung wird dann für den Benutzer angezeigt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
void DemoConversation()
{
    object selectedItem = 
        Application.ActiveExplorer().Selection[1];
    // For this example, you will work only with 
    //MailItem. Other item types such as
    //MeetingItem and PostItem can participate 
    //in Conversation.
    if (selectedItem is Outlook.MailItem)
    {
        // Cast selectedItem to MailItem.
        Outlook.MailItem mailItem =
            selectedItem as Outlook.MailItem; ;
        // Determine store of mailItem.
        Outlook.Folder folder = mailItem.Parent
            as Outlook.Folder;
        Outlook.Store store = folder.Store;
        if (store.IsConversationEnabled == true)
        {
            // Obtain a Conversation object.
            Outlook.Conversation conv =
                mailItem.GetConversation();
            // Check for null Conversation.
            if (conv != null)
            {
                // Obtain Table that contains rows 
                // for each item in Conversation.
                Outlook.Table table = conv.GetTable();
                Debug.WriteLine("Conversation Items Count: " +
                    table.GetRowCount().ToString());
                Debug.WriteLine("Conversation Items from Table:");
                while (!table.EndOfTable)
                {
                    Outlook.Row nextRow = table.GetNextRow();
                    Debug.WriteLine(nextRow["Subject"]
                        + " Modified: "
                        + nextRow["LastModificationTime"]);
                }
                Debug.WriteLine("Conversation Items from Root:");
                // Obtain root items and enumerate Conversation.
                Outlook.SimpleItems simpleItems 
                    = conv.GetRootItems();
                foreach (object item in simpleItems)
                {
                    // In this example, enumerate only MailItem type.
                    // Other types such as PostItem or MeetingItem
                    // can appear in Conversation.
                    if (item is Outlook.MailItem)
                    {
                        Outlook.MailItem mail = item
                            as Outlook.MailItem;
                        Outlook.Folder inFolder =
                            mail.Parent as Outlook.Folder;
                        string msg = mail.Subject
                            + " in folder " + inFolder.Name;
                        Debug.WriteLine(msg);
                    }
                    // Call EnumerateConversation 
                    // to access child nodes of root items.
                    EnumerateConversation(item, conv);
                }
            }
        }
    }
}

void EnumerateConversation(object item,
    Outlook.Conversation conversation)
{
    Outlook.SimpleItems items =
        conversation.GetChildren(item);
    if (items.Count > 0)
    {
        foreach (object myItem in items)
        {
            // In this example, enumerate only MailItem type.
            // Other types such as PostItem or MeetingItem
            // can appear in Conversation.
            if (myItem is Outlook.MailItem)
            {
                Outlook.MailItem mailItem =
                    myItem as Outlook.MailItem;
                Outlook.Folder inFolder =
                    mailItem.Parent as Outlook.Folder;
                string msg = mailItem.Subject
                    + " in folder " + inFolder.Name;
                Debug.WriteLine(msg);
            }
            // Continue recursion.
            EnumerateConversation(myItem, conversation);
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Unterhaltungen](conversations.md)

