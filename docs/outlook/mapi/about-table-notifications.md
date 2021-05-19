---
title: Informationen zu Tabellenbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9a42ed1e196e8ac498ab5889b4419ff407db4748
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417952"
---
# <a name="about-table-notifications"></a><span data-ttu-id="0c7a6-103">Informationen zu Tabellenbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="0c7a6-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="0c7a6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c7a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c7a6-105">Clients verlassen sich häufig auf Tabellenbenachrichtigungen, um Änderungen an Objekten zu erfahren, anstatt sich für den direkten Empfang von Benachrichtigungen von den Objekten zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="0c7a6-106">Typische Änderungen, die dazu führen, dass Benachrichtigungen gesendet werden, umfassen das Hinzu-, Löschen oder Ändern einer Zeile sowie alle kritischen Fehler.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="0c7a6-107">Wenn Benachrichtigungen eintreffen, können Clients bestimmen, ob sie einen weiteren Aufruf zum Erneutladen der Tabelle senden möchten.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="0c7a6-108">Da Tabellenbenachrichtigungen asynchron sind, gibt es einige Probleme, die die Behandlung von Benachrichtigungen weniger einfach machen können:</span><span class="sxs-lookup"><span data-stu-id="0c7a6-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="0c7a6-109">Die in der TABLE_NOTIFICATION [übergebenen](table_notification.md) Daten stellen möglicherweise nicht den aktuellen Zustand der Tabelle dar.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="0c7a6-110">Ein Client kann z. B. eine Änderung an einer Nachricht vor sich nehmen und dann entscheiden, sie zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="0c7a6-111">Der Nachrichtenspeicheranbieter, der die Inhaltstabelle, in der die Nachricht enthalten ist, implementieren, sendet zwei Benachrichtigungen: ein TABLE_ROW_MODIFIED-Ereignis gefolgt von einem TABLE_ROW_DELETED Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="0c7a6-112">Je nachdem, wie der Nachrichtenspeicheranbieter Benachrichtigungen einbekommt, erhält der Client die TABLE_ROW_MODIFIED nach dem Löschen der Zeile.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="0c7a6-113">Der Spaltensatz, der in einer Benachrichtigung enthalten ist, kann sich vom aktuellen Spaltensatz der Tabelle unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="0c7a6-114">MAPI erfordert, dass der Benachrichtigungsspaltensatz mit dem Spaltensatz übereinstimmen, der zum Zeitpunkt der Benachrichtigung generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="0c7a6-115">Da ein Client [IMAPITable::SetColumns](imapitable-setcolumns.md) aufrufen kann, um den Spaltensatz jederzeit zu ändern , auch nach einer Benachrichtigung, werden die beiden Spaltensätze möglicherweise nicht synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="0c7a6-116">Tabellenbenachrichtigungen werden nur für Zeilen gesendet, die Teil der Ansicht sind.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="0c7a6-117">Das heißt, wenn eine Zeile aufgrund einer Einschränkung aus der Ansicht ausgeschlossen wird oder sich die Tabelle in einem reduzierten Zustand befindet, wird keine Benachrichtigung gesendet, wenn diese Zeile geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="0c7a6-118">Außerdem werden keine Benachrichtigungen gesendet, um einen Client über eine Änderung des Kategoriestatus zu informieren.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="0c7a6-119">Clients sollten beachten, dass nicht alle Tabellen die Benachrichtigung TABLE_SORT_DONE unterstützen und bereit sein sollten, diese Bedingung zu behandeln:</span><span class="sxs-lookup"><span data-stu-id="0c7a6-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="0c7a6-120">Erzwingen, dass die Sortierung synchron ist.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="0c7a6-121">Erneutes Laden der Zeilen der Tabelle, wenn [IMAPITable::SortTable zurückgegeben](imapitable-sorttable.md) wird.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0c7a6-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c7a6-122">See also</span></span>



[<span data-ttu-id="0c7a6-123">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="0c7a6-123">MAPI Tables</span></span>](mapi-tables.md)

