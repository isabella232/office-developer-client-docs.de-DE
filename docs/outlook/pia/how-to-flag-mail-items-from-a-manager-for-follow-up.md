---
title: Kennzeichnen von E-Mail-Elementen von einem Vorgesetzten zur Nachverfolgung
TOCTitle: Flag mail items from a manager for follow-up
ms:assetid: 5f7f3678-0f63-451e-ba08-cd973525aa1b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424470(v=office.15)
ms:contentKeyID: 55119898
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 73c4a7ec8118b95edac06ae8ab5bc59902612ebc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406365"
---
# <a name="flag-mail-items-from-a-manager-for-follow-up"></a><span data-ttu-id="c0268-102">Kennzeichnen von E-Mail-Elementen von einem Vorgesetzten zur Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="c0268-102">Flag mail items from a manager for follow-up</span></span>

<span data-ttu-id="c0268-103">Dieses Beispiel zeigt, wie E-Mail-Elemente gekennzeichnet werden, die vom Vorgesetzten des Benutzers zur Nachverfolgung empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="c0268-103">This example shows how to flag e-mail items that were received from the user's manager for follow-up.</span></span>

## <a name="example"></a><span data-ttu-id="c0268-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c0268-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="c0268-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="c0268-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="c0268-106">In Microsoft Outlook wird ein System zur Aufgabenkennzeichnung bereitgestellt, bei dem bestimmte Outlook-Elemente, wie E-Mail- oder Kontaktelemente, zur Nachverfolgung gekennzeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="c0268-106">Microsoft Outlook provides a new task flagging system in which certain Outlook items such as mail items or contact items can be flagged for follow-up.</span></span> <span data-ttu-id="c0268-107">Wenn ein Outlook-Element zur Nachverfolgung gekennzeichnet wird, werden in den Navigationsmodulen **Aufgabenleiste** und Kalender der Outlook-Benutzeroberfläche zusätzlich zu anderen aufgabenspezifischen Angaben auch Informationen zu diesem Outlook-Element angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c0268-107">Flagging an Outlook item for follow-up displays information about that Outlook item, along with other task-based information, on the **To-Do Bar** and Calendar navigation module in the Outlook user interface.The following Outlook item objects have been extended to support the task flagging system:</span></span> <span data-ttu-id="c0268-108">Die **Aufgabenleiste** wird als vertikaler Bereich in einer Standardkonfiguration des Outlook-Explorer-Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c0268-108">The **To-Do Bar** is displayed as a vertical pane in a typical configuration of the Outlook explorer window.</span></span> <span data-ttu-id="c0268-109">Sie enthält ein Steuerelement für den Datumsnavigator, anstehende Termine und Elemente, die zur Nachverfolgung gekennzeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="c0268-109">It contains a date navigator control, upcoming appointments, and items that have been flagged for follow-up.</span></span> <span data-ttu-id="c0268-110">Die **Aufgabenleiste** selbst ist nicht erweiterbar, und Sie können die Konfigurationsoptionen für die **Aufgabenleiste** nur über die Outlook-Benutzeroberfläche festlegen.</span><span class="sxs-lookup"><span data-stu-id="c0268-110">The **To-Do Bar** itself is not extensible, and you can set configuration options for the **To-Do Bar** only through the Outlook user interface.</span></span> <span data-ttu-id="c0268-111">Das Kennzeichnen von Elementen ermöglicht die Organisation und Priorisierung von Aufgaben und Aufgabenelementen.</span><span class="sxs-lookup"><span data-stu-id="c0268-111">Flagging items allows to you organize and prioritize tasks and to-do items.</span></span>

<span data-ttu-id="c0268-112">Im folgenden Codebeispiel wird eine Gruppe von Elementen für ein bestimmtes Zeitintervall zur Nachverfolgung gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="c0268-112">The following code example marks a group of items for a specified follow-up interval.</span></span> <span data-ttu-id="c0268-113">Das Beispiel ruft alle Elemente im Posteingang des aktuellen Benutzers ab, die von dessen Vorgesetzten stammen, indem eine DASL-Abfrage (DAV Searching and Locating) zum Filtern nach Nachrichten vom Typ „IPM.NOTE“ mit dem Namen des Vorgesetzten als Absender ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0268-113">The example gets all items in the current user's Inbox that are from the current user's manager by using a DAV Searching and Locating (DASL) query to filter for messages of type "IPM.NOTE" with the manager's name as the sender.</span></span> <span data-ttu-id="c0268-114">Anschließend werden alle Elemente entsprechend dem [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\))-Wert der [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\))-Eigenschaft gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="c0268-114">It then flags all items according to the [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) value of the [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)) property.</span></span> <span data-ttu-id="c0268-115">Alle Elemente mit hoher Wichtigkeit werden für heute zur Nachverfolgung gekennzeichnet und alle Elemente mit normaler Wichtigkeit werden für diese Woche zur Nachverfolgung mithilfe der [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\))-Methode gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="c0268-115">All high-importance items are flagged for follow-up today and all normal-importance items are flagged for follow-up this week by using the [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) method.</span></span>


> [!NOTE]
> <span data-ttu-id="c0268-116">Die **Importance**-Eigenschaft und die **MarkAsTask**-Methode sind Elemente des **Item**-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c0268-116">The **Importance** property and the **MarkAsTask** method are **Item** object members</span></span>


<span data-ttu-id="c0268-117">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="c0268-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="c0268-118">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c0268-118">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="c0268-119">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="c0268-119">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTaskFlagging()
{
    const string PR_SENT_REPRESENTING_NAME =
        "https://schemas.microsoft.com/mapi/proptag/0x0042001E";
    const string PR_MESSAGE_CLASS =
        "https://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager;
        try
        {
            manager = currentUser.
                GetExchangeUser().GetExchangeUserManager();
        }
        catch
        {
            Debug.WriteLine("Could not obtain user's manager.");
            return;
        }
        if (manager != null)
        {
            string displayName = manager.Name;
            string filter = "@SQL=" + "\""
                + PR_SENT_REPRESENTING_NAME + "\""
                + " = '" + displayName + "'" + " AND " + "\""
                + PR_MESSAGE_CLASS + "\"" + " = 'IPM.NOTE'";
            Outlook.Items items =
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderInbox).
                Items.Restrict(filter);
            foreach (Outlook.MailItem mail in items)
            {
                if (mail.Importance ==
                    Outlook.OlImportance.olImportanceHigh)
                {
                    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkToday);
                    mail.Save();
                }
                if (mail.Importance ==
                    Outlook.OlImportance.olImportanceNormal)
                {
                    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkThisWeek);
                    mail.Save();
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="c0268-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0268-120">See also</span></span>

- [<span data-ttu-id="c0268-121">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="c0268-121">Tasks</span></span>](tasks.md)

