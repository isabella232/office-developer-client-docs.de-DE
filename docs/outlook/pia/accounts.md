---
title: Konten
TOCTitle: Accounts
ms:assetid: 28df6dbd-4d24-42f3-91c1-fd8b3a4ea722
ms:mtpsurl: https://msdn.microsoft.com/library/office/ff184597(v=office.15)
ms:contentKeyID: 55119790
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: eb7c56a8a261f36628c3b440c1aeec31c7aec46e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406820"
---
# <a name="accounts"></a><span data-ttu-id="7438a-102">Konten</span><span class="sxs-lookup"><span data-stu-id="7438a-102">Accounts</span></span> 

<span data-ttu-id="7438a-103">In diesem Abschnitt werden Beispielaufgaben bereitgestellt, die sich auf E-Mail-Konten beziehen.</span><span class="sxs-lookup"><span data-stu-id="7438a-103">This section provides sample tasks that involve e-mail accounts.</span></span> <span data-ttu-id="7438a-104">Beispiele von E-Mail-Konten sind Microsoft Exchange Server-, Post Office Protocol 3 (POP3)-, Internet Message Access Protocol (IMAP)- und Hypertext Transfer Protocol (HTTP)-Konten.</span><span class="sxs-lookup"><span data-stu-id="7438a-104">Examples of e-mail accounts are Microsoft Exchange Server, Post Office Protocol 3 (POP3), Internet Message Access Protocol (IMAP), and Hypertext Transfer Protocol (HTTP) accounts.</span></span> <span data-ttu-id="7438a-105">Ein Konto für das aktuelle Profil wird durch ein [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia)-Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7438a-105">An account for the current profile is represented by an [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia) object.</span></span>


|<span data-ttu-id="7438a-106">Thema</span><span class="sxs-lookup"><span data-stu-id="7438a-106">Topic</span></span>|<span data-ttu-id="7438a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7438a-107">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="7438a-108">Abrufen von Kontoinformationen</span><span class="sxs-lookup"><span data-stu-id="7438a-108">Get account information</span></span>](how-to-get-account-information.md) | <span data-ttu-id="7438a-109">Verwendet als Eingabeargument ein vertrauenswürdiges Microsoft Outlook [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) -Objekt und zeigt mithilfe des **Account**-Objekts die Details aller Konten an, die für das aktuelle Outlook-Profil zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="7438a-109">Takes as an input argument a trusted Microsoft Outlook [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) object, and uses the **Account** object to display the details of each account that is available for the current Outlook profile.</span></span>|
|[<span data-ttu-id="7438a-110">Erstellen eines sendbaren Elements für ein bestimmtes Konto auf der Basis des aktuellen Ordners</span><span class="sxs-lookup"><span data-stu-id="7438a-110">Create a Sendable Item for a Specific Account Based on the Current Folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md) | <span data-ttu-id="7438a-111">Enthält zwei Codebeispiele, die zeigen, wie ein versendbares E-Mail-Element und eine Besprechungsanfrage erstellt werden, und wie sie mithilfe eines bestimmten Kontos, das auf dem aktuellen Ordner basiert, gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7438a-111">Contains two code examples that show how to create a sendable e-mail item and meeting request, and then to send them by using a specific account that is based on the current folder.</span></span>|
|[<span data-ttu-id="7438a-112">Abrufen des Kontos für einen Ordner</span><span class="sxs-lookup"><span data-stu-id="7438a-112">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md) | <span data-ttu-id="7438a-113">Ruft das Konto ab, das einem Ordner in der aktuellen Sitzung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7438a-113">Gets the account that is associated with a folder in the current session.</span></span>|
|[<span data-ttu-id="7438a-114">Abrufen von Informationen über mehrere Konten</span><span class="sxs-lookup"><span data-stu-id="7438a-114">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md) | <span data-ttu-id="7438a-115">Ruft verschiedene Informationen zu jedem Konto im aktuellen Profil ab und zeigt diese an.</span><span class="sxs-lookup"><span data-stu-id="7438a-115">Obtains and displays miscellaneous information about each account in the current profile.</span></span>|
|<span data-ttu-id="7438a-116">[Senden eines E-Mail-Elements mithilfe eines Hotmail-Kontos](how-to-send-a-mail-item-by-using-a-hotmail-account.md)</span><span class="sxs-lookup"><span data-stu-id="7438a-116">Uses the [SendUsingAccount](how-to-send-a-mail-item-by-using-a-hotmail-account.md) property to send a mail item by using a Windows Live Hotmail account.</span></span> | <span data-ttu-id="7438a-117">Verwendet die [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) -Eigenschaft, um ein E-Mail-Element mithilfe eines Windows Live Hotmail-Kontos zu senden.</span><span class="sxs-lookup"><span data-stu-id="7438a-117">Uses the [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) property to send a mail item by using a Windows Live Hotmail account.</span></span>|

## <a name="see-also"></a><span data-ttu-id="7438a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7438a-118">See also</span></span>

- [<span data-ttu-id="7438a-119">Exchange-Benutzer</span><span class="sxs-lookup"><span data-stu-id="7438a-119">Exchange Users</span></span>](exchange-users.md)
- [<span data-ttu-id="7438a-120">Mail</span><span class="sxs-lookup"><span data-stu-id="7438a-120">Mail</span></span>](mail.md)
- [<span data-ttu-id="7438a-121">Empfänger</span><span class="sxs-lookup"><span data-stu-id="7438a-121">Recipients</span></span>](recipients.md)
- [<span data-ttu-id="7438a-122">Gewusst wie... (Outlook 2013 PIA-Referenz)</span><span class="sxs-lookup"><span data-stu-id="7438a-122">How Do I... (Outlook 2013 PIA Reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

