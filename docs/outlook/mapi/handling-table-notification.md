---
title: Behandeln von Tabelle Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 95ef351e4fe906608319a3e25de8f20a44e23d9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791824"
---
# <a name="handling-table-notification"></a><span data-ttu-id="8aa3a-103">Behandeln von Tabelle Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="8aa3a-103">Handling table notification</span></span>

<span data-ttu-id="8aa3a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8aa3a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8aa3a-105">Ein Client kann als Alternative zum Registrieren direkt mit einer Advise-Quellobjekt, beispielsweise einen Ordner oder ein messaging-Benutzer für Benachrichtigungen auf einem Inhalt registrieren oder Hierarchietabelle.</span><span class="sxs-lookup"><span data-stu-id="8aa3a-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="8aa3a-106">Einträge, Ordner und Nachrichten über eine Inhalt zum Nachverfolgen von Änderungen an-Adresse Buch oder Hierarchietabelle sind einfacher als auch einfacher, als über die einzelnen Objekte.</span><span class="sxs-lookup"><span data-stu-id="8aa3a-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="8aa3a-107">Beispielsweise können Sie [IMAPITable::Advise](imapitable-advise.md) für einen Ordner Hierarchietabelle ermitteln können, falls sich ein Unterordner aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8aa3a-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="8aa3a-108">Wenn Sie das Anzeigen von remote-Nachrichten unterstützen, registrieren Sie die Statustabelle auf Aktivität von Anbietern für Transport, und die MAPI-Warteschlange einzuhalten.</span><span class="sxs-lookup"><span data-stu-id="8aa3a-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="8aa3a-109">Es ist jedoch nicht immer vorzuziehen Tabelle Benachrichtigungen anstelle von Benachrichtigungen Objekt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8aa3a-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="8aa3a-110">Überwachen von Änderungen in die Anzahl der Nachrichten in einem Ordner ist ein Beispiel für bei Ihrem Client möglicherweise für Objekt Benachrichtigungen auf einen Ordner und nicht auf einer Tabelle, die durch den Ordner implementiert registriert.</span><span class="sxs-lookup"><span data-stu-id="8aa3a-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

