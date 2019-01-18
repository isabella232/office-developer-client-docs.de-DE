---
title: Erstellen eines sendbaren Elements für ein bestimmtes Konto auf der Basis des aktuellen Ordners
TOCTitle: Create a sendable item for a specific account based on the current folder
ms:assetid: 665ebdc5-2912-4d85-ac40-835c9ef9a439
ms:contentKeyID: 55119796
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ccbbaab10dc88d50c1fad3c1eefeb5c222bc8446
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702159"
---
# <a name="create-a-sendable-item-for-a-specific-account-based-on-the-current-folder"></a>Erstellen eines sendbaren Elements für ein bestimmtes Konto auf der Basis des aktuellen Ordners

Dieser Abschnitt enthält zwei Codebeispiele, die zeigen, wie ein versendbares E-Mailelement und eine Besprechungsanfrage erstellt werden, und wie sie mithilfe eines bestimmten Kontos, das auf dem aktuellen Ordner basiert, gesendet werden.

## <a name="example"></a>Beispiel

Wenn Sie die [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\))-Methode des [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) -Objekts zum Erstellen des Outlook-Elements verwenden, wird das Element für das primäre Konto dieser Sitzung erstellt. In einer Sitzung mit mehreren im Profil definierten Konten können Sie ein Element für ein bestimmtes IMAP-, POP- oder Exchange-Konto erstellen. 

Wenn Sie bei mehreren Konten im aktuellen Profil ein versendbares E-Mailelement über die Benutzeroberfläche erstellen, indem Sie auf **Neue E-Mail** oder **Neue Besprechung** klicken, wird ein neues E-Mailelement oder einen Besprechungsanfrage im Erstellmodus angezeigt und Sie können das Konto auswählen, über das Sie das Element senden möchten. 

In diesem Thema wird erläutert, wie ein versendbares Element erstellt und über ein bestimmtes Konto gesendet wird. Das Thema enthält zwei Codebeispiele, die zeigen, wie [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) und [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) für ein bestimmtes Konto erstellt werden, das vom aktuellen Ordner im aktiven Explorer festgelegt wird.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

In der ersten Methode wird durch CreateMailItemFromAccount das entsprechende Konto identifiziert, indem der Speicher des aktuellen Ordners (abgerufen durch die [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))-Eigenschaft) mit dem Standardzustellspeicher aller Konten (abgerufen durch die [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))-Eigenschaft), die in der [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\))-Sammlung für die Sitzung definiert wurden, abgeglichen wird. CreateMailItemFromAccount erstellt das **MailItem**-Objekt. 

Um das Element dem Konto zuzuordnen, wird durch CreateMailItemFromAccount der Benutzer des Kontos dem Absender des Elements zugewiesen, indem die account.CurrentUser.AddressEntry property-Eigenschaft auf die [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\))-Eigenschaft von **MailItem** festgelegt wird. Das Zuweisen der Sender-Eigenschaft ist der entscheidende Schritt; wenn Sie den Absender nicht festlegen, wird das **MailItem** standardmäßig für das primäre Konto erstellt. Am Ende der Methode zeigt CreateMailItemFromAccount das **MailItem**-Objekt an. Handelt es sich bei dem aktuellen Ordner nicht um einen Zustellordner, erstellt CreateMailItemFromAccount das **MailItem** für das primäre Konto für die Sitzung.

```csharp
private void CreateMailItemFromAccount()
{
    Outlook.AddressEntry addrEntry = null;
    // Get the Store for CurrentFolder.
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder 
        as Outlook.Folder;
    Outlook.Store store = folder.Store;
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    // Enumerate accounts to find
    // account.DeliveryStore for store.
    foreach (Outlook.Account account in accounts)
    {
        if (account.DeliveryStore.StoreID == 
            store.StoreID)
        {
            addrEntry =
                account.CurrentUser.AddressEntry;
            break;
        }
    }
    // Create MailItem.
    Outlook.MailItem mail =
        Application.CreateItem(
        Outlook.OlItemType.olMailItem)
        as Outlook.MailItem;
    if (addrEntry != null)
    {
        // Set Sender property.
        mail.Sender = addrEntry;
        mail.Display(false);
    }
}
```

Die nächste Methode, CreateMeetingRequestFromAccount, ähnelt CreateMailItemFromAccount mit dem Unterschied, dass ein AppointmentItem statt eines MailItem-Objekts erstellt wird. Mit CreateMeetingRequestFromAccount wird zunächst das entsprechende Konto identifiziert, indem der Speicher des aktuellen Ordners (abgerufen durch die [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))-Eigenschaft) mit dem Standardzustellspeicher aller Konten (abgerufen durch die [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))-Eigenschaft), die in der Accounts-Sammlung für die Sitzung definiert wurden, abgeglichen wird. CreateMeetingRequestFromAccount erstellt dann das AppointmentItem-Objekt. 

Um das Element dem Konto zuzuordnen, wird durch CreateMeetingRequestFromAccount der Benutzer des Kontos dem Absender des Elements zugewiesen, indem das [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\))-Objekt der [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\))-Eigenschaft von AppointmentItem zugewiesen wird. Das Zuweisen der SendUsingAccount-Eigenschaft ist der entscheidende Schritt; wenn Sie das Konto nicht festlegen, wird das AppointmentItem standardmäßig für das primäre Konto erstellt. Am Ende der Methode zeigt CreateMeetingRequestFromAccount das AppointmentItem-Objekt an. Handelt es sich bei dem aktuellen Ordner nicht um einen Zustellordner, erstellt CreateMeetingRequestFromAccount das AppointmentItem für das primäre Konto der Sitzung.

```csharp
private void CreateMeetingRequestFromAccount()
{
    Outlook.Account acct = null;
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store store = folder.Store;
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    foreach (Outlook.Account account in accounts)
    {
        if (account.DeliveryStore.StoreID ==
            store.StoreID)
        {
            acct = account;
            break;
        }
    }
    Outlook.AppointmentItem appt =
        Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = 
        Outlook.OlMeetingStatus.olMeeting;
    if (acct != null)
    {
        // Set SendUsingAccount property.
        appt.SendUsingAccount=acct;
        appt.Display(false);
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Accounts](accounts.md)

