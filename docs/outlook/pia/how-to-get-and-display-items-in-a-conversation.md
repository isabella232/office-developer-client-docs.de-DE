---
title: Abrufen und Anzeigen von Elementen in einer Unterhaltung
TOCTitle: Get and display items in a conversation
ms:assetid: 8f30a7cb-0949-46d7-bc51-2d93dbb22bf8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184625(v=office.15)
ms:contentKeyID: 55119832
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: dd48437e0b2092d905cf870451b59aea9ef66c5d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407443"
---
# <a name="get-and-display-items-in-a-conversation"></a><span data-ttu-id="8cb94-102">Abrufen und Anzeigen von Elementen in einer Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="8cb94-102">Get and display items in a conversation</span></span>

<span data-ttu-id="8cb94-103">In diesem Beispiel wird veranschaulicht, wie E-Mail-Elemente in einer Unterhaltung abgerufen und angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8cb94-103">This example shows how to get and display mail items in a conversation.</span></span>

## <a name="example"></a><span data-ttu-id="8cb94-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8cb94-104">Example</span></span>

<span data-ttu-id="8cb94-105">Im folgenden Codebeispiel ruft DemoConversation ein [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))-Objekt ab und ermittelt dann den Speicher des **MailItem**-Objekts unter Verwendung der [Store](https://msdn.microsoft.com/library/bb609093\(v=office.15\))-Eigenschaft des [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8cb94-105">In the following code example, DemoConversation gets a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object and then determines the store of the **MailItem** object by using the [Store](https://msdn.microsoft.com/library/bb609093\(v=office.15\)) property of the [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span> <span data-ttu-id="8cb94-106">DemoConversation überprüft dann, ob die [IsConversationEnabled](https://msdn.microsoft.com/library/ff185030\(v=office.15\))-Eigenschaft auf **true** festgelegt it; wenn sie auf **true** festgelegt ist, ruft das Codebeispiel das [Conversation](https://msdn.microsoft.com/library/ff184711\(v=office.15\))-Objekt mithilfe der [GetConversation()](https://msdn.microsoft.com/library/ff184974\(v=office.15\))-Methode ab.</span><span class="sxs-lookup"><span data-stu-id="8cb94-106">DemoConversation then checks whether the [IsConversationEnabled](https://msdn.microsoft.com/library/ff185030\(v=office.15\)) property is **true**; if it is **true**, the code example gets [Conversation](https://msdn.microsoft.com/library/ff184711\(v=office.15\)) object by using the [GetConversation()](https://msdn.microsoft.com/library/ff184974\(v=office.15\)) method.</span></span> <span data-ttu-id="8cb94-107">Wenn das **Conversation**-Objekt kein Nullverweis ist, ruft das Beispiel das zugeordnete [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt mithilfe der [GetTable()](https://msdn.microsoft.com/library/ff185184\(v=office.15\))-Methode ab, das jedes Element in der Unterhaltung enthält.</span><span class="sxs-lookup"><span data-stu-id="8cb94-107">If the **Conversation** object is not a null reference, the example gets the associated [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object that contains each item in the conversation by using the [GetTable()](https://msdn.microsoft.com/library/ff185184\(v=office.15\)) method.</span></span> 

<span data-ttu-id="8cb94-108">Im Beispiel wird dann jedes Element in der **Tabelle** aufgeführt und EnumerateConversation für jedes Element aufgerufen, um auf die untergeordneten Knoten jedes Elements zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="8cb94-108">The example then enumerates each item in the **Table** and calls EnumerateConversation on each item to access the child nodes of each item.</span></span> <span data-ttu-id="8cb94-109">EnumerateConversation verwendet ein **Conversation**-Objekt und ruft die untergeordneten Knoten mit der [GetChildren(Object)](https://msdn.microsoft.com/library/ff184854\(v=office.15\))-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="8cb94-109">EnumerateConversation takes a **Conversation** object and gets the child nodes by using the [GetChildren(Object)](https://msdn.microsoft.com/library/ff184854\(v=office.15\)) method.</span></span> <span data-ttu-id="8cb94-110">EnumerateConversation wird rekursiv aufgerufen, bis keine weiteren untergeordneten Knoten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8cb94-110">EnumerateConversation is called recursively until there are no more child nodes.</span></span> <span data-ttu-id="8cb94-111">Jedes Element der Unterhaltung wird dann für den Benutzer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8cb94-111">Each conversation item is then displayed to the user.</span></span>

<span data-ttu-id="8cb94-112">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="8cb94-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="8cb94-113">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8cb94-113">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="8cb94-114">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="8cb94-114">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="8cb94-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cb94-115">See also</span></span>

- [<span data-ttu-id="8cb94-116">Unterhaltungen</span><span class="sxs-lookup"><span data-stu-id="8cb94-116">Conversations</span></span>](conversations.md)

