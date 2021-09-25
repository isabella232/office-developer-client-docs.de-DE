---
title: Anzeigen eines freigegebenen Kalenders eines Empfängers
TOCTitle: Display a shared calendar of a recipient
ms:assetid: 3dcfec17-c836-4bd0-a177-33c911a94b1f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184606(v=office.15)
ms:contentKeyID: 55119825
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5775c7856ecf5d4e163f5c27e9aeca3ab55920bb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560606"
---
# <a name="display-a-shared-calendar-of-a-recipient"></a>Anzeigen eines freigegebenen Kalenders eines Empfängers

Dieses Beispiel zeigt, wie Sie mithilfe der Methoden [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) und [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) den freigegebenen Kalender eines Empfängers anzeigen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Versendbare Elemente wie [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) -Objekte legen immer die [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) -Eigenschaft offen, die es Ihnen ermöglicht, auf die [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) -Sammlung für das versendbare Element zuzugreifen. Zum Erstellen eines [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) -Objekts, das nicht mit der **Recipients**-Sammlung eines Elements gebunden ist, verwenden Sie die [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) -Methode des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekts.Übermitteln Sie dann das ungebundene **Recipient**-Objekt an die [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) -Methode, die einen freigegebenen Exchange-Ordner zurückgibt. Öffnen Sie dann den freigegebenen Exchange-Ordner und zeigen Sie diesen Ordner in einem Explorer-Fenster an. GetSharedDefaultFolder wird in Exchange-Stellvertreterszenarios verwendet, in denen der Stellvertreter die Zugriffsberechtigung für den Stellvertreterordner hat. Bevor Sie das **Recipient**-Objekt an die GetSharedDefaultFolder-Methode übermitteln, müssen Sie es auflösen. Zum Auflösen eines **Recipient**-Objekts rufen Sie seine [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) -Methode auf.

Im folgenden Codebeispiel wird von DisplayManagerCalendarder Kalenderordner des Vorgesetzten des aktuellen Benutzers geöffnet, indem **CreateRecipient** und **GetSharedDefaultFolder** aufgerufen wird. Es wird ein Sicherheitswarnungs-Dialogfeld angezeigt, wenn der Benutzer nicht über die entsprechenden Berechtigungen zum Öffnen des Kalenderordners des Vorgesetzten verfügt oder ein Fehler auftritt. 


> [!NOTE]
> Wenn Sie ein **Recipient**-Objekt mithilfe der **CreateRecipient**-Methode des **Namespace**-Objekts oder der [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) -Methode der **Recipients**-Sammlung erstellen müssen Sie einen Empfängernamen angeben. **Recipient** wird dann in diesen Namen aufgelöst. Ein Empfängername kann eines der folgenden Formate aufweisen:
> - Anzeigename
> - Alias
> - SMTP-Adresse (Simple Mail Transfer Protocol)

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

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

## <a name="see-also"></a>Siehe auch

- [Calendar](calendar.md)

