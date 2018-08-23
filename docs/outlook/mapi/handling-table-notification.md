---
title: Behandeln von Tabelle Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b36e4697bfd4360f4ea6ea47c70eaaae434696d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595132"
---
# <a name="handling-table-notification"></a><span data-ttu-id="042ae-103">Behandeln von Tabelle Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="042ae-103">Handling table notification</span></span>

<span data-ttu-id="042ae-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="042ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="042ae-105">Ein Client kann als Alternative zum Registrieren direkt mit einer Advise-Quellobjekt, beispielsweise einen Ordner oder ein messaging-Benutzer für Benachrichtigungen auf einem Inhalt registrieren oder Hierarchietabelle.</span><span class="sxs-lookup"><span data-stu-id="042ae-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="042ae-106">Einträge, Ordner und Nachrichten über eine Inhalt zum Nachverfolgen von Änderungen an-Adresse Buch oder Hierarchietabelle sind einfacher als auch einfacher, als über die einzelnen Objekte.</span><span class="sxs-lookup"><span data-stu-id="042ae-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="042ae-107">Beispielsweise können Sie [IMAPITable::Advise](imapitable-advise.md) für einen Ordner Hierarchietabelle ermitteln können, falls sich ein Unterordner aufrufen.</span><span class="sxs-lookup"><span data-stu-id="042ae-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="042ae-108">Wenn Sie das Anzeigen von remote-Nachrichten unterstützen, registrieren Sie die Statustabelle auf Aktivität von Anbietern für Transport, und die MAPI-Warteschlange einzuhalten.</span><span class="sxs-lookup"><span data-stu-id="042ae-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="042ae-109">Es ist jedoch nicht immer vorzuziehen Tabelle Benachrichtigungen anstelle von Benachrichtigungen Objekt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="042ae-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="042ae-110">Überwachen von Änderungen in die Anzahl der Nachrichten in einem Ordner ist ein Beispiel für bei Ihrem Client möglicherweise für Objekt Benachrichtigungen auf einen Ordner und nicht auf einer Tabelle, die durch den Ordner implementiert registriert.</span><span class="sxs-lookup"><span data-stu-id="042ae-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

