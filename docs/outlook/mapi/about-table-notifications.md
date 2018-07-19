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
ms.openlocfilehash: 3dfc67c8bcd899396da5371c614fd221cd9b2251
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791229"
---
# <a name="about-table-notifications"></a><span data-ttu-id="7d1e4-103">Informationen zu Tabellenbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="7d1e4-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="7d1e4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d1e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d1e4-105">Clients nutzen häufig Tabelle Benachrichtigungen von Änderungen an Objekten anstelle von Erhalt von Benachrichtigungen direkt über die Objekte registrieren erfahren.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="7d1e4-106">Typische Änderungen, die dazu führen, dass Benachrichtigungen gesendet werden umfassen die hinzufügen, löschen oder Änderung einer Zeile und keinen kritischen Fehler.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="7d1e4-107">Wenn Benachrichtigungen eingehen, können Clients bestimmen, ob stellen Sie einen weiteren Anruf die Tabelle erneut geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="7d1e4-108">Da Tabelle Benachrichtigungen asynchron sind, sind einige Probleme, die Behandlung Benachrichtigungen kleiner als unkomplizierte können:</span><span class="sxs-lookup"><span data-stu-id="7d1e4-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="7d1e4-109">Die Daten in der Struktur [TABLE_NOTIFICATION](table_notification.md) übergeben möglicherweise nicht am aktuellen Status der Tabelle darstellen.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="7d1e4-110">Ein Client kann beispielsweise eine Änderung vornehmen, um eine Nachricht und dann entscheiden, ihn zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="7d1e4-111">Implementieren der Inhaltstabelle, die die Nachricht enthalten Anbieter die Nachricht sendet, zwei Benachrichtigungen: ein Ereignis TABLE_ROW_MODIFIED gefolgt von einem TABLE_ROW_DELETED-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="7d1e4-112">Je nachdem, wie der Nachricht Speicheranbieter Benachrichtigungen auftritt kann der Client TABLE_ROW_MODIFIED nach dem Löschen der Zeile eine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="7d1e4-113">Die Spalte in einer Benachrichtigung enthalten möglicherweise nicht mit der Tabelle aktuellen Spalte abweichen.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="7d1e4-114">MAPI erfordert, dass die Benachrichtigung Spalte Festlegen der Spalte entsprechen, die zum Zeitpunkt gültig war, die die Benachrichtigung generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="7d1e4-115">Da es für einen Client aufrufen, [IMAPITable::SetColumns](imapitable-setcolumns.md) zum Ändern der Spalte festlegen, können Sie jederzeit möglich ist – einschließlich nach einer Benachrichtigung – im zweispaltiges wird möglicherweise nicht synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="7d1e4-116">Tabelle Benachrichtigungen werden nur für Zeilen gesendet, die Teil der Ansicht sind.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="7d1e4-117">D. h., wird eine Zeile aus der Ansicht aufgrund einer Einschränkung ausgeschlossen wird oder, da die Tabelle in einem reduzierten Zustand befindet, keine Benachrichtigung gesendet, wenn diese Zeile geändert wird.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="7d1e4-118">Darüber hinaus sind keine Benachrichtigungen gesendet, um einen Client über eine Änderung in der Kategorie Zustand zu informieren.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="7d1e4-119">Clients Beachten Sie, dass nicht alle Tabellen die Benachrichtigung TABLE_SORT_DONE unterstützen und sollte Seien Sie diese Bedingung durch behandeln:</span><span class="sxs-lookup"><span data-stu-id="7d1e4-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="7d1e4-120">Erzwingen die Sortierung synchrone sein.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="7d1e4-121">Die Zeilen der Tabelle Neuladen, wenn [SortTable](imapitable-sorttable.md) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7d1e4-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7d1e4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d1e4-122">See also</span></span>



[<span data-ttu-id="7d1e4-123">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="7d1e4-123">MAPI Tables</span></span>](mapi-tables.md)

