---
title: Kennzeichnen von E-Mail-Elementen von einem Vorgesetzten zur Nachverfolgung
TOCTitle: Flag mail items from a manager for follow-up
ms:assetid: 5f7f3678-0f63-451e-ba08-cd973525aa1b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424470(v=office.15)
ms:contentKeyID: 55119898
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3c2fa97cbf0128544da769a2d990f0b3a66fd3a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574685"
---
# <a name="flag-mail-items-from-a-manager-for-follow-up"></a>Kennzeichnen von E-Mail-Elementen von einem Vorgesetzten zur Nachverfolgung

Dieses Beispiel zeigt, wie E-Mail-Elemente gekennzeichnet werden, die vom Vorgesetzten des Benutzers zur Nachverfolgung empfangen wurden.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Microsoft Outlook provides a task flagging system in which certain Outlook items such as mail items or contact items can be flagged for follow-up. When you flag an Outlook item for follow-up, information about that Outlook item, along with other task-based information, is displayed on the **To-Do Bar** and Calendar navigation module in the Outlook user interface. The **To-Do Bar** is displayed as a vertical pane in a typical configuration of the Outlook explorer window. It contains a date navigator control, upcoming appointments, and items that have been flagged for follow-up. The **To-Do Bar** itself is not extensible, and you can set configuration options for the **To-Do Bar** only through the Outlook user interface. Flagging items allows to you organize and prioritize tasks and to-do items.

Das folgende Codebeispiel markiert eine Gruppe von Elementen für ein angegebenes Nachverfolgungsintervall. Das Beispiel ruft alle Elemente im Posteingang des aktuellen Benutzers ab, die von dessen Vorgesetzten stammen, indem eine DASL-Abfrage (DAV Searching and Locating) zum Filtern nach Nachrichten vom Typ „IPM.NOTE“ mit dem Namen des Vorgesetzten als Absender ausgeführt wird. Anschließend werden alle Elemente entsprechend dem [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\))-Wert der [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\))-Eigenschaft gekennzeichnet. Alle Elemente mit hoher Wichtigkeit werden für heute zur Nachverfolgung gekennzeichnet und alle Elemente mit normaler Wichtigkeit werden für diese Woche zur Nachverfolgung mithilfe der [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\))-Methode gekennzeichnet.


> [!NOTE]
> Die **Importance**-Eigenschaft und die **MarkAsTask**-Methode sind Elemente des **Item**-Objekts.


Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTaskFlagging()
{
    const string PR_SENT_REPRESENTING_NAME =
        "http://schemas.microsoft.com/mapi/proptag/0x0042001E";
    const string PR_MESSAGE_CLASS =
        "http://schemas.microsoft.com/mapi/proptag/0x001A001E";
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

## <a name="see-also"></a>Siehe auch

- [Aufgaben](tasks.md)

