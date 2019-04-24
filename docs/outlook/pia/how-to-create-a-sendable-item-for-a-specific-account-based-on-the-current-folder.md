---
title: Erstellen eines sendbaren Elements für ein bestimmtes Konto auf der Basis des aktuellen Ordners
TOCTitle: Create a sendable item for a specific account based on the current folder
ms:assetid: 665ebdc5-2912-4d85-ac40-835c9ef9a439
ms:contentKeyID: 55119796
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ccbbaab10dc88d50c1fad3c1eefeb5c222bc8446
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349532"
---
# <a name="create-a-sendable-item-for-a-specific-account-based-on-the-current-folder"></a><span data-ttu-id="0fb3e-102">Erstellen eines sendbaren Elements für ein bestimmtes Konto auf der Basis des aktuellen Ordners</span><span class="sxs-lookup"><span data-stu-id="0fb3e-102">Create a sendable item for a specific account based on the current folder</span></span>

<span data-ttu-id="0fb3e-103">Dieser Abschnitt enthält zwei Codebeispiele, die zeigen, wie ein versendbares E-Mailelement und eine Besprechungsanfrage erstellt werden, und wie sie mithilfe eines bestimmten Kontos, das auf dem aktuellen Ordner basiert, gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-103">This topic contains two code examples that show how to create a sendable email item and meeting request, and then how to send them by using a specific account that is based on the current folder.</span></span>

## <a name="example"></a><span data-ttu-id="0fb3e-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0fb3e-104">Example</span></span>

<span data-ttu-id="0fb3e-105">Wenn Sie die [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\))-Methode des [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) -Objekts zum Erstellen des Outlook-Elements verwenden, wird das Element für das primäre Konto dieser Sitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-105">When you use the [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) method of the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object to create an Outlook item, the item is created for the primary account for that session.</span></span> <span data-ttu-id="0fb3e-106">In einer Sitzung mit mehreren im Profil definierten Konten können Sie ein Element für ein bestimmtes IMAP-, POP- oder Exchange-Konto erstellen.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-106">In a session where multiple accounts are defined in the profile, you can create an item for a specific IMAP, POP, or Exchange account.</span></span> 

<span data-ttu-id="0fb3e-107">Wenn Sie bei mehreren Konten im aktuellen Profil ein versendbares E-Mailelement über die Benutzeroberfläche erstellen, indem Sie auf **Neue E-Mail** oder **Neue Besprechung** klicken, wird ein neues E-Mailelement oder einen Besprechungsanfrage im Erstellmodus angezeigt und Sie können das Konto auswählen, über das Sie das Element senden möchten.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-107">If there are multiple accounts in the current profile and you create a sendable item in the user interface, for example, by clicking **New Email** or **New Meeting**, an inspector displays a new mail item or meeting request in compose mode, and then you can select the account from which to send the item.</span></span> 

<span data-ttu-id="0fb3e-108">In diesem Thema wird erläutert, wie ein versendbares Element erstellt und über ein bestimmtes Konto gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-108">This topic shows how to programmatically create a sendable item and send it by using a specific sending account.</span></span> <span data-ttu-id="0fb3e-109">Das Thema enthält zwei Codebeispiele, die zeigen, wie [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) und [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) für ein bestimmtes Konto erstellt werden, das vom aktuellen Ordner im aktiven Explorer festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-109">The topic has two code examples that show how to create a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) and an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) for a specific account that is determined by the current folder in the active explorer.</span></span>

<span data-ttu-id="0fb3e-110">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="0fb3e-111">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0fb3e-112">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="0fb3e-113">In der ersten Methode wird durch CreateMailItemFromAccount das entsprechende Konto identifiziert, indem der Speicher des aktuellen Ordners (abgerufen durch die [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))-Eigenschaft) mit dem Standardzustellspeicher aller Konten (abgerufen durch die [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))-Eigenschaft), die in der [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\))-Sammlung für die Sitzung definiert wurden, abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-113">In the first method, CreateMailItemFromAccount first identifies the appropriate account by matching the store of the current folder (obtained from the [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) property) with the default delivery store of each account (obtained with the [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) property) that is defined in the [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) collection for the session.</span></span> <span data-ttu-id="0fb3e-114">CreateMailItemFromAccount erstellt das **MailItem**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-114">CreateMailItemFromAccount then creates the **MailItem**.</span></span> 

<span data-ttu-id="0fb3e-115">Um das Element dem Konto zuzuordnen, wird durch CreateMailItemFromAccount der Benutzer des Kontos dem Absender des Elements zugewiesen, indem die account.CurrentUser.AddressEntry property-Eigenschaft auf die [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\))-Eigenschaft von **MailItem** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-115">To associate the item with the account, CreateMailItemFromAccount assigns the user of the account as the sender of the item by setting the account.CurrentUser.AddressEntry property to the [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) property of the **MailItem**.</span></span> <span data-ttu-id="0fb3e-116">Das Zuweisen der Sender-Eigenschaft ist der entscheidende Schritt; wenn Sie den Absender nicht festlegen, wird das **MailItem** standardmäßig für das primäre Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-116">Assigning the Sender property is the important step; if you do not specify the sender, the **MailItem** is created for the primary account by default.</span></span> <span data-ttu-id="0fb3e-117">Am Ende der Methode zeigt CreateMailItemFromAccount das **MailItem**-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-117">At the end of the method, CreateMailItemFromAccount displays the **MailItem**.</span></span> <span data-ttu-id="0fb3e-118">Handelt es sich bei dem aktuellen Ordner nicht um einen Zustellordner, erstellt CreateMailItemFromAccount das **MailItem** für das primäre Konto für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-118">Note that if the current folder is not on a delivery store, CreateMailItemFromAccount creates the **MailItem** for the primary account for the session.</span></span>

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

<span data-ttu-id="0fb3e-119">Die nächste Methode, CreateMeetingRequestFromAccount, ähnelt CreateMailItemFromAccount mit dem Unterschied, dass ein AppointmentItem statt eines MailItem-Objekts erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-119">The next method, CreateMeetingRequestFromAccount, is similar to CreateMailItemFromAccount except that it creates an AppointmentItem instead of a MailItem.</span></span> <span data-ttu-id="0fb3e-120">Mit CreateMeetingRequestFromAccount wird zunächst das entsprechende Konto identifiziert, indem der Speicher des aktuellen Ordners (abgerufen durch die [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))-Eigenschaft) mit dem Standardzustellspeicher aller Konten (abgerufen durch die [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))-Eigenschaft), die in der Accounts-Sammlung für die Sitzung definiert wurden, abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-120">CreateMeetingRequestFromAccount first identifies the appropriate account by matching the store of the current folder (obtained from the [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) property) with the default delivery store of each account (obtained from the [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) property) that is defined in the Accounts collection for the session.</span></span> <span data-ttu-id="0fb3e-121">CreateMeetingRequestFromAccount erstellt dann das AppointmentItem-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-121">CreateMeetingRequestFromAccount then creates the AppointmentItem.</span></span> 

<span data-ttu-id="0fb3e-122">Um das Element dem Konto zuzuordnen, wird durch CreateMeetingRequestFromAccount der Benutzer des Kontos dem Absender des Elements zugewiesen, indem das [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\))-Objekt der [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\))-Eigenschaft von AppointmentItem zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-122">To associate the item with the account, CreateMeetingRequestFromAccount assigns that account as the item's sending account by setting the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object to the [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) property of the AppointmentItem.</span></span> <span data-ttu-id="0fb3e-123">Das Zuweisen der SendUsingAccount-Eigenschaft ist der entscheidende Schritt; wenn Sie das Konto nicht festlegen, wird das AppointmentItem standardmäßig für das primäre Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-123">Assigning the SendUsingAccount property is the important step; if you do not specify the account, the AppointmentItem is created for the primary account by default.</span></span> <span data-ttu-id="0fb3e-124">Am Ende der Methode zeigt CreateMeetingRequestFromAccount das AppointmentItem-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-124">At the end of the method, CreateMeetingRequestFromAccount displays the AppointmentItem.</span></span> <span data-ttu-id="0fb3e-125">Handelt es sich bei dem aktuellen Ordner nicht um einen Zustellordner, erstellt CreateMeetingRequestFromAccount das AppointmentItem für das primäre Konto der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0fb3e-125">Note that if the current folder is not on a delivery store, CreateMeetingRequestFromAccount creates the AppointmentItem for the primary account for the session.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="0fb3e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fb3e-126">See also</span></span>

- [<span data-ttu-id="0fb3e-127">Accounts</span><span class="sxs-lookup"><span data-stu-id="0fb3e-127">Accounts</span></span>](accounts.md)

