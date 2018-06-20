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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fd77473ce728a51220a4c039f1d12d03d90e7f36
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795717"
---
# <a name="tablenotification"></a><span data-ttu-id="1eeee-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1eeee-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="1eeee-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1eeee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1eeee-105">Beschreibt eine Zeile in einer Tabelle, die mit einem Typ des Ereignisses, wie eine Änderung oder einen Fehler betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="1eeee-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="1eeee-106">Daraufhin wird eine Tabelle Benachrichtigung generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1eeee-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1eeee-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1eeee-107">Header file:</span></span>  <br/> |<span data-ttu-id="1eeee-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1eeee-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="1eeee-109">Members</span><span class="sxs-lookup"><span data-stu-id="1eeee-109">Members</span></span>

<span data-ttu-id="1eeee-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="1eeee-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="1eeee-111">Bitmaske aus Flags verwendet, um den Ereignistyp Tabelle darstellen.</span><span class="sxs-lookup"><span data-stu-id="1eeee-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="1eeee-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1eeee-112">The following flags can be set:</span></span>
    
<span data-ttu-id="1eeee-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="1eeee-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="1eeee-114">Gibt auf allgemeiner Ebene, dass etwas über die Tabelle geändert hat.</span><span class="sxs-lookup"><span data-stu-id="1eeee-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="1eeee-115">Die Tabelle festgelegt ist, wie er vor dem das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1eeee-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="1eeee-116">Dies bedeutet, dass alle Eigenschaften **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), Lesezeichen, aktuellen Positionierung und Schnittstelle Benutzerauswahl noch gültig sind.</span><span class="sxs-lookup"><span data-stu-id="1eeee-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="1eeee-117">Behandeln Sie dieses Ereignis wird durch erneutes Lesen der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1eeee-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="1eeee-118">Dienstanbieter, die keine rich Tabelle Benachrichtigungen implementieren möchten, senden TABLE_CHANGED Ereignisse anstelle von ausführlichere Ereignisse zum Angeben eines bestimmten Typs der Änderung.</span><span class="sxs-lookup"><span data-stu-id="1eeee-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="1eeee-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="1eeee-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="1eeee-120">In der Regel während der Verarbeitung eines asynchronen Vorgangs ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1eeee-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="1eeee-121">Fehler bei der Verarbeitung der folgenden Methoden können dieses Ereignis generieren:</span><span class="sxs-lookup"><span data-stu-id="1eeee-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="1eeee-122">SortTable</span><span class="sxs-lookup"><span data-stu-id="1eeee-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="1eeee-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="1eeee-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="1eeee-124">Methode IMAPITable:: Restrict</span><span class="sxs-lookup"><span data-stu-id="1eeee-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="1eeee-125">Ein Client kann nicht nach dem Empfang ein TABLE_ERROR-Ereignis, auf die Genauigkeit der Inhalt der Tabelle verlassen.</span><span class="sxs-lookup"><span data-stu-id="1eeee-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="1eeee-126">Darüber hinaus möglicherweise ausstehende Benachrichtigungen zu anderen Änderungen verloren.</span><span class="sxs-lookup"><span data-stu-id="1eeee-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="1eeee-127">Die [IMAPITable::GetLastError](imapitable-getlasterror.md) -Methode bietet zusätzliche Informationen zu dem Fehler möglicherweise nicht, da es zu einem Zeitpunkt, was nicht notwendigerweise vom letzten Methodenaufruf generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1eeee-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="1eeee-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="1eeee-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="1eeee-129">Die Daten in der Tabelle sollte erneut geladen werden.</span><span class="sxs-lookup"><span data-stu-id="1eeee-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="1eeee-130">Dienstanbieter senden TABLE_RELOAD, wenn beispielsweise die zugrunde liegenden Daten in einer Datenbank gespeichert ist und die Datenbank ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="1eeee-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="1eeee-131">Behandeln Sie dieses Ereignis von, unter der Annahme, dass nichts über die Tabelle noch gültig ist und durch erneutes Lesen der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1eeee-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="1eeee-132">Alle Lesezeichen, Instanzenschlüssel, Status und Positionierung Informationen sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="1eeee-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="1eeee-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="1eeee-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="1eeee-134">Eine Einschränkung, die mit einem Aufruf der **Methode IMAPITable:: Restrict** -Methode initiiert wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1eeee-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="1eeee-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="1eeee-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="1eeee-136">Eine neue Zeile wurde der Tabelle und das entsprechende Objekt gespeichert hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1eeee-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="1eeee-137">TABLE_ROW_ADDED Ereignisse werden nach einem Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode generiert.</span><span class="sxs-lookup"><span data-stu-id="1eeee-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="1eeee-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="1eeee-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="1eeee-139">Eine Zeile wurde aus der Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="1eeee-139">A row has been removed from the table.</span></span> <span data-ttu-id="1eeee-140">Das **PropPrior** -Element wird auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1eeee-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="1eeee-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="1eeee-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="1eeee-142">Eine Zeile wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="1eeee-142">A row has been changed.</span></span> <span data-ttu-id="1eeee-143">**Das Zeilenelement** enthält die betroffenen Eigenschaften für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="1eeee-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="1eeee-144">Mehrere TABLE_ROW_MODIFIED-Ereignisse werden in der Reihenfolge gesendet, die sie in der Tabellenansicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1eeee-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="1eeee-145">TABLE_ROW_MODIFIED Ereignisse werden gesendet, nachdem Änderungen an das entsprechende Objekt mit einem Aufruf der **IMAPIProp::SaveChanges** -Methode übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="1eeee-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="1eeee-146">Wenn die geänderte Zeile jetzt die erste Zeile in der Tabelle ist, ist der Wert des Tags-Eigenschaft im **PropPrior** -Member **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1eeee-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="1eeee-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="1eeee-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="1eeee-148">Eine Spalte Einstellung, die mit einem Aufruf der **IMAPITable::SetColumns** -Methode initiiert wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1eeee-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="1eeee-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="1eeee-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="1eeee-150">Eine Tabelle sortieren Vorgang mit einem Aufruf der **SortTable** -Methode initiiert wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1eeee-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="1eeee-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="1eeee-151">**hResult**</span></span>
  
> <span data-ttu-id="1eeee-152">HRESULT-Wert für den, der aufgetretenen Fehler, wenn das Element **UlTableEvent** auf TABLE_ERROR festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1eeee-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="1eeee-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="1eeee-153">**propIndex**</span></span>
  
> <span data-ttu-id="1eeee-154">[SPropValue](spropvalue.md) -Struktur für die **PR_INSTANCE_KEY** -Eigenschaft der betreffenden Zeile.</span><span class="sxs-lookup"><span data-stu-id="1eeee-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="1eeee-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="1eeee-155">**propPrior**</span></span>
  
> <span data-ttu-id="1eeee-156">**SPropValue** -Struktur für die **PR_INSTANCE_KEY** -Eigenschaft der Zeile vor der betroffenen.</span><span class="sxs-lookup"><span data-stu-id="1eeee-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="1eeee-157">Wenn die betroffene Zeile der ersten Zeile in der Tabelle ist, muss **PropPrior** **PR_NULL** und nicht 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1eeee-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="1eeee-158">0 (null) ist eine gültige Eigenschaftentag.</span><span class="sxs-lookup"><span data-stu-id="1eeee-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="1eeee-159">**Zeile**</span><span class="sxs-lookup"><span data-stu-id="1eeee-159">**row**</span></span>
  
> <span data-ttu-id="1eeee-160">[SRow](srow.md) -Struktur, die die betreffenden Zeile beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1eeee-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="1eeee-161">Diese Struktur ist für alle Tabelle Benachrichtigungsereignisse gefüllt.</span><span class="sxs-lookup"><span data-stu-id="1eeee-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="1eeee-162">Für Benachrichtigungsereignisse der Tabelle, die keine Zeilendaten übergeben, das **cValues** Mitglied der **SRow** -Struktur auf 0 (null) festgelegt ist und der **LpProps** Member wird auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1eeee-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="1eeee-163">Da diese Struktur **SRow** schreibgeschützt ist. Clients müssen eine Kopie davon vornehmen, wenn sie Änderungen vornehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="1eeee-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="1eeee-164">Die [ScDupPropset](scduppropset.md) -Funktion kann verwendet werden, um die Kopie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1eeee-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1eeee-165">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1eeee-165">Remarks</span></span>

<span data-ttu-id="1eeee-166">Die **Tabelle\_Benachrichtigung** Struktur ist ein Mitglied der Union der Strukturen, die in der **Info** -Member der Struktur [Benachrichtigung](notification.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="1eeee-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="1eeee-167">Das **Info** -Element enthält eine **Tabelle\_Benachrichtigung** Struktur, wenn der **UlEventType** Member der Struktur auf _FnevTableModified_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1eeee-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="1eeee-168">Die Reihenfolge und den Typ der Spalten in der Zeile Member entsprechen die Reihenfolge und den Typ, der zum Zeitpunkt gültig war, die die Benachrichtigung generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1eeee-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="1eeee-169">Die Reihenfolge und den Typ der Zeitpunkt, die die Benachrichtigung generiert wurde ist nicht unbedingt identisch, wenn die Benachrichtigung übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="1eeee-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="1eeee-170">Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1eeee-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="1eeee-171">**Thema**</span><span class="sxs-lookup"><span data-stu-id="1eeee-171">**Topic**</span></span>|<span data-ttu-id="1eeee-172">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1eeee-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1eeee-173">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="1eeee-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="1eeee-174">Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="1eeee-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="1eeee-175">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="1eeee-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="1eeee-176">Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1eeee-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="1eeee-177">Benachrichtigung bei unterstützenden</span><span class="sxs-lookup"><span data-stu-id="1eeee-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="1eeee-178">Erläuterung der wie-Dienstanbieter die **IMAPISupport** -Methode verwenden können, um Benachrichtigungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1eeee-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="1eeee-179">Da Tabelle Benachrichtigungen asynchron sind, können Clients Benachrichtigung über eine hinzugefügte Zeile nach Informationen über das Hinzufügen auf andere Weise erhalten.</span><span class="sxs-lookup"><span data-stu-id="1eeee-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="1eeee-180">Es ist möglich, erhalten ein TABLE_ERROR-Ereignis, wenn in einer **IMAPITable::Sort**, **IMAPITable::SetColumns** oder **Methode IMAPITable:: Restrict**-Methode ein Fehler aufgetreten ist, oder wenn eine zugrunde liegende versucht, eine Tabelle mit, aktualisieren, beispielsweise neu oder geänderte Zeilen.</span><span class="sxs-lookup"><span data-stu-id="1eeee-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1eeee-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1eeee-181">See also</span></span>

- [<span data-ttu-id="1eeee-182">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="1eeee-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="1eeee-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="1eeee-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="1eeee-184">' Srow '</span><span class="sxs-lookup"><span data-stu-id="1eeee-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="1eeee-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1eeee-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="1eeee-186">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="1eeee-186">MAPI Structures</span></span>](mapi-structures.md)

