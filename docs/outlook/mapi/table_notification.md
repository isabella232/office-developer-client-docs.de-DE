---
title: TABLE_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TABLE_NOTIFICATION
api_type:
- COM
ms.assetid: 48e478c4-6e9a-40ab-a7bb-e6219b743b08
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6c35220529fb88b470c563a0b004bfcf7e63ef76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415957"
---
# <a name="tablenotification"></a><span data-ttu-id="7ed34-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7ed34-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="7ed34-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ed34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ed34-105">Beschreibt eine Zeile in einer Tabelle, die von einer Art von Ereignis beeinflusst wurde, beispielsweise eine Änderung oder ein Fehler.</span><span class="sxs-lookup"><span data-stu-id="7ed34-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="7ed34-106">Dadurch wird eine Tabellenbenachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="7ed34-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ed34-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7ed34-107">Header file:</span></span>  <br/> |<span data-ttu-id="7ed34-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7ed34-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _TABLE_NOTIFICATION
{
  ULONG ulTableEvent;
  HRESULT hResult;
  SPropValue propIndex;
  SPropValue propPrior;
  SRow row;
} TABLE_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="7ed34-109">Members</span><span class="sxs-lookup"><span data-stu-id="7ed34-109">Members</span></span>

<span data-ttu-id="7ed34-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="7ed34-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="7ed34-111">Bitmaske der Flags, die zum Darstellen des Table-Ereignistyps verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ed34-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="7ed34-112">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7ed34-112">The following flags can be set:</span></span>
    
<span data-ttu-id="7ed34-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="7ed34-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="7ed34-114">Gibt auf hoher Ebene an, dass sich etwas in der Tabelle geändert hat.</span><span class="sxs-lookup"><span data-stu-id="7ed34-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="7ed34-115">Der Status der Tabelle ist wie vor dem Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7ed34-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="7ed34-116">Dies führt dazu, dass alle **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md))-Eigenschaften, Lesezeichen, aktuelle Positionierung und Benutzeroberflächenauswahl noch gültig sind.</span><span class="sxs-lookup"><span data-stu-id="7ed34-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="7ed34-117">Behandeln Sie dieses Ereignis, indem Sie die Tabelle erneut lesen.</span><span class="sxs-lookup"><span data-stu-id="7ed34-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="7ed34-118">Dienstanbieter, die Rich-Table-Benachrichtigungen nicht implementieren möchten, senden TABLE_CHANGED-Ereignisse anstelle detaillierter Ereignisse, um einen bestimmten Änderungstyp anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7ed34-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="7ed34-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="7ed34-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="7ed34-120">Es ist ein Fehler aufgetreten, normalerweise während der Verarbeitung eines asynchronen Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="7ed34-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="7ed34-121">Fehler bei der Verarbeitung der folgenden Methoden können dieses Ereignis generieren:</span><span class="sxs-lookup"><span data-stu-id="7ed34-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="7ed34-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="7ed34-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="7ed34-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="7ed34-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="7ed34-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="7ed34-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="7ed34-125">Nachdem ein TABLE_ERROR-Ereignis empfangen wurde, kann sich ein Client nicht auf die Genauigkeit des Tabelleninhalts verlassen.</span><span class="sxs-lookup"><span data-stu-id="7ed34-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="7ed34-126">Außerdem können ausstehende Benachrichtigungen über andere Änderungen verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="7ed34-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="7ed34-127">Die [IMAPITable:: getlasterroraufzurufen](imapitable-getlasterror.md) -Methode bietet möglicherweise keine zusätzlichen Informationen zu dem Fehler, da Sie zu einem früheren Zeitpunkt generiert wurde, nicht unbedingt vom letzten Methodenaufruf.</span><span class="sxs-lookup"><span data-stu-id="7ed34-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="7ed34-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="7ed34-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="7ed34-129">Die Daten in der Tabelle sollten erneut geladen werden.</span><span class="sxs-lookup"><span data-stu-id="7ed34-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="7ed34-130">Dienstanbieter senden TABLE_RELOAD, wenn beispielsweise die zugrunde liegenden Daten in einer Datenbank gespeichert sind und die Datenbank ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="7ed34-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="7ed34-131">Behandeln Sie dieses Ereignis, indem Sie davon ausgehen, dass nichts zur Tabelle noch gültig ist und die Tabelle erneut gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="7ed34-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="7ed34-132">Alle Lesezeichen, Instanzenschlüssel, Status-und Positionierungsinformationen sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="7ed34-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="7ed34-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="7ed34-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="7ed34-134">Ein mit einem **IMAPITable:: Restrict** -Methodenaufruf initiierter Einschränkungs Vorgang wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7ed34-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="7ed34-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="7ed34-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="7ed34-136">Der Tabelle wurde eine neue Zeile hinzugefügt, und das entsprechende Objekt wurde gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7ed34-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="7ed34-137">TABLE_ROW_ADDED-Ereignisse werden nach einem Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode generiert.</span><span class="sxs-lookup"><span data-stu-id="7ed34-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="7ed34-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="7ed34-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="7ed34-139">Eine Zeile wurde aus der Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ed34-139">A row has been removed from the table.</span></span> <span data-ttu-id="7ed34-140">Das **propPrior** -Element ist auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7ed34-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="7ed34-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="7ed34-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="7ed34-142">Eine Zeile wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="7ed34-142">A row has been changed.</span></span> <span data-ttu-id="7ed34-143">Das **Row** -Element enthält die betroffenen Eigenschaften für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="7ed34-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="7ed34-144">Mehrere TABLE_ROW_MODIFIED-Ereignisse werden in der Reihenfolge gesendet, in der Sie in der Tabellenansicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7ed34-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="7ed34-145">TABLE_ROW_MODIFIED-Ereignisse werden gesendet, nachdem Änderungen am entsprechenden Objekt mit einem Aufruf der **IMAPIProp:: SaveChanges** -Methode übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="7ed34-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="7ed34-146">Wenn die geänderte Zeile jetzt die erste Zeile in der Tabelle ist, ist der Wert des Property-Tags im **propPrior** -Element **PR_NULL** ([pidtagnull (](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7ed34-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="7ed34-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="7ed34-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="7ed34-148">Ein mit einem **IMAPITable::** SetColumns-Methodenaufruf initiierter Spalten Einstellungsvorgang wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7ed34-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="7ed34-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="7ed34-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="7ed34-150">Ein Tabellen Sortiervorgang, der mit einem **IMAPITable:: sortable** -Methodenaufruf initiiert wurde, wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7ed34-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="7ed34-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="7ed34-151">**hResult**</span></span>
  
> <span data-ttu-id="7ed34-152">HRESULT-Wert für den aufgetretenen Fehler, wenn das **ulTableEvent** -Element auf TABLE_ERROR festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7ed34-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="7ed34-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="7ed34-153">**propIndex**</span></span>
  
> <span data-ttu-id="7ed34-154">[SPropValue](spropvalue.md) -Struktur für die **PR_INSTANCE_KEY** -Eigenschaft der betroffenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="7ed34-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="7ed34-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="7ed34-155">**propPrior**</span></span>
  
> <span data-ttu-id="7ed34-156">**SPropValue** -Struktur für die **PR_INSTANCE_KEY** -Eigenschaft der Zeile vor dem betroffenen.</span><span class="sxs-lookup"><span data-stu-id="7ed34-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="7ed34-157">Wenn die betroffene Zeile die erste Zeile in der Tabelle ist, muss **propPrior** auf **PR_NULL** und nicht auf NULL festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="7ed34-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="7ed34-158">NULL ist kein gültiges Property-Tag.</span><span class="sxs-lookup"><span data-stu-id="7ed34-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="7ed34-159">**Zeile**</span><span class="sxs-lookup"><span data-stu-id="7ed34-159">**row**</span></span>
  
> <span data-ttu-id="7ed34-160">[SRow](srow.md) -Struktur, die die betroffene Zeile beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7ed34-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="7ed34-161">Diese Struktur wird für alle Benachrichtigungsereignisse für Tabellen ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="7ed34-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="7ed34-162">Für Tabellen Benachrichtigungsereignisse, die keine Zeilendaten überschreiten, wird das **cValues** -Element der **SRow** -Struktur auf NULL festgelegt, und das **LPPROPS** -Element wird auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7ed34-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="7ed34-163">Da diese **SRow** -Struktur schreibgeschützt ist; Clients müssen eine Kopie davon erstellen, wenn Sie Änderungen vornehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="7ed34-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="7ed34-164">Die [ScDupPropset](scduppropset.md) -Funktion kann verwendet werden, um die Kopie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7ed34-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7ed34-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ed34-165">Remarks</span></span>

<span data-ttu-id="7ed34-166">Die **Tabellen\_Benachrichtigungs** Struktur ist ein Mitglied der Vereinigung der Strukturen, die im **Info** -Element der Benachrichtigungs [](notification.md) Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7ed34-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="7ed34-167">Der **Info** -Member enthält **eine\_Tabellen Benachrichtigungs** Struktur, wenn das **ulEventType** -Element der Struktur auf _fnevTableModified_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7ed34-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="7ed34-168">Die Reihenfolge und der Typ der Spalten im row-Element geben die Reihenfolge und den Typ wieder, die zu dem Zeitpunkt wirksam waren, zu dem die Benachrichtigung generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7ed34-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="7ed34-169">Die Reihenfolge und der Typ zu dem Zeitpunkt, zu dem die Benachrichtigung generiert wurde, entsprechen nicht unbedingt dem Zeitpunkt, zu dem die Benachrichtigung übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ed34-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="7ed34-170">Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="7ed34-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="7ed34-171">**Thema**</span><span class="sxs-lookup"><span data-stu-id="7ed34-171">**Topic**</span></span>|<span data-ttu-id="7ed34-172">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7ed34-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ed34-173">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="7ed34-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="7ed34-174">Allgemeine Übersicht über Benachrichtigungs-und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="7ed34-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="7ed34-175">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="7ed34-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="7ed34-176">Erläuterung, wie Clients Benachrichtigungen behandeln sollen.</span><span class="sxs-lookup"><span data-stu-id="7ed34-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="7ed34-177">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="7ed34-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="7ed34-178">Erläuterung, wie Dienstanbieter die **IMAPISupport** -Methode verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7ed34-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="7ed34-179">Da Tabellen Benachrichtigungen asynchron sind, können Clients Benachrichtigungen über eine hinzugefügte Zeile erhalten, nachdem Sie über das Hinzufügen auf eine andere Weise informiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7ed34-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="7ed34-180">Es ist möglich, ein TABLE_ERROR-Ereignis zu empfangen, wenn ein Fehler in einer **IMAPITable:: Sort**, **IMAPITable:: Restrict**oder **IMAPITable::** SetColumns-Methode vorliegt oder wenn ein zugrunde liegender Prozess versucht, eine Tabelle mit zu aktualisieren, beispielsweise neue oder geänderte Zeilen.</span><span class="sxs-lookup"><span data-stu-id="7ed34-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7ed34-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ed34-181">See also</span></span>

- [<span data-ttu-id="7ed34-182">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="7ed34-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="7ed34-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="7ed34-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="7ed34-184">SRow</span><span class="sxs-lookup"><span data-stu-id="7ed34-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="7ed34-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7ed34-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="7ed34-186">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7ed34-186">MAPI Structures</span></span>](mapi-structures.md)

