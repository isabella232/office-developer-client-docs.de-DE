---
title: Anzeigen eines freigegebenen Kalenders eines Empfängers
TOCTitle: Display a shared calendar of a recipient
ms:assetid: 3dcfec17-c836-4bd0-a177-33c911a94b1f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184606(v=office.15)
ms:contentKeyID: 55119825
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 10101a3eff1b0507c1fe562f175bace7026143fb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406883"
---
# <a name="display-a-shared-calendar-of-a-recipient"></a><span data-ttu-id="eb063-102">Anzeigen eines freigegebenen Kalenders eines Empfängers</span><span class="sxs-lookup"><span data-stu-id="eb063-102">Display a shared calendar of a recipient</span></span>

<span data-ttu-id="eb063-103">Dieses Beispiel zeigt, wie Sie mithilfe der Methoden [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) und [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) den freigegebenen Kalender eines Empfängers anzeigen.</span><span class="sxs-lookup"><span data-stu-id="eb063-103">This example shows how to display a recipient's shared calendar by using the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) and [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) methods.</span></span>

## <a name="example"></a><span data-ttu-id="eb063-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="eb063-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="eb063-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="eb063-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="eb063-p101">Versendbare Elemente wie [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) -Objekte legen immer die [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) -Eigenschaft offen, die es Ihnen ermöglicht, auf die [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) -Sammlung für das versendbare Element zuzugreifen. Zum Erstellen eines [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) -Objekts, das nicht mit der **Recipients**-Sammlung eines Elements gebunden ist, verwenden Sie die [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) -Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekts.Übermitteln Sie dann das ungebundene **Recipient**-Objekt an die [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) -Methode, die einen freigegebenen Exchange-Ordner zurückgibt. Öffnen Sie dann den freigegebenen Exchange-Ordner und zeigen Sie diesen Ordner in einem Explorer-Fenster an. GetSharedDefaultFolder wird in Exchange-Stellvertreterszenarios verwendet, in denen der Stellvertreter die Zugriffsberechtigung für den Stellvertreterordner hat. Bevor Sie das **Recipient**-Objekt an die GetSharedDefaultFolder-Methode übermitteln, müssen Sie es auflösen. Zum Auflösen eines **Recipient**-Objekts rufen Sie seine [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="eb063-p101">Sendable items such as [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) objects always expose the [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) property which, in turn, enables you to access the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection for the sendable item. To create a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object that is not bound to the **Recipients** collection of an item, use the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object. Then pass this unbound **Recipient** object to the [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) method, which returns a shared Exchange folder. You can then open the shared Exchange folder and display that folder in an explorer window. GetSharedDefaultFolder is used in Exchange delegate scenarios where the delegate has permission to access the folder of the delegator. Before you pass the **Recipient** object to the GetSharedDefaultFolder method, you must resolve it. To resolve a **Recipient** object, call its [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) method.</span></span>

<span data-ttu-id="eb063-p102">Im folgenden Codebeispiel wird von DisplayManagerCalendarder Kalenderordner des Vorgesetzten des aktuellen Benutzers geöffnet, indem **CreateRecipient** und **GetSharedDefaultFolder** aufgerufen wird. Es wird ein Sicherheitswarnungs-Dialogfeld angezeigt, wenn der Benutzer nicht über die entsprechenden Berechtigungen zum Öffnen des Kalenderordners des Vorgesetzten verfügt oder ein Fehler auftritt. </span><span class="sxs-lookup"><span data-stu-id="eb063-p102">In the following code example, DisplayManagerCalendar opens and displays the Calendar folder of the current user’s manager by calling **CreateRecipient** and **GetSharedDefaultFolder**. An alert dialog box is displayed if the user does not have permission to open the manager’s Calendar folder or an error occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="eb063-115">Wenn Sie ein **Recipient**-Objekt mithilfe der **CreateRecipient**-Methode des **Namespace**-Objekts oder der [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) -Methode der **Recipients**-Sammlung erstellen müssen Sie einen Empfängernamen angeben.</span><span class="sxs-lookup"><span data-stu-id="eb063-115">When you create a **Recipient** object by using the **CreateRecipient** method of the **Namespace** object or the [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) method of the **Recipients** collection, you must provide a recipient name.</span></span> <span data-ttu-id="eb063-116">**Recipient** wird dann in diesen Namen aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="eb063-116">The **Recipient** is then resolved against this name.</span></span> <span data-ttu-id="eb063-117">Ein Empfängername kann eines der folgenden Formate aufweisen:</span><span class="sxs-lookup"><span data-stu-id="eb063-117">A recipient name can take any of the following formats: >  Display name >  Alias >  Simple Mail Transfer Protocol (SMTP) address</span></span>
> - <span data-ttu-id="eb063-118">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="eb063-118">Display name</span></span>
> - <span data-ttu-id="eb063-119">Alias</span><span class="sxs-lookup"><span data-stu-id="eb063-119">Alias</span></span>
> - <span data-ttu-id="eb063-120">SMTP-Adresse (Simple Mail Transfer Protocol)</span><span class="sxs-lookup"><span data-stu-id="eb063-120">Simple Mail Transfer Protocol (SMTP) address</span></span>

<span data-ttu-id="eb063-121">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="eb063-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="eb063-122">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="eb063-122">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="eb063-123">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="eb063-123">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayManagerCalendar()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.Recipient recip =
                Application.Session.CreateRecipient(manager.Name);
            if (recip.Resolve())
            {
                try
                {
                    Outlook.Folder folder =
                        Application.Session.GetSharedDefaultFolder(
                        recip, Outlook.OlDefaultFolders.olFolderCalendar)
                        as Outlook.Folder;
                    folder.Display();
                }
                catch
                {
                    MessageBox.Show("Could not open manager's calendar.",
                        "GetSharedDefaultFolder Example",
                        MessageBoxButtons.OK,
                        MessageBoxIcon.Error);
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="eb063-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb063-124">See also</span></span>

- [<span data-ttu-id="eb063-125">Kalender</span><span class="sxs-lookup"><span data-stu-id="eb063-125">Calendar</span></span>](calendar.md)

