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
# <a name="table_notification"></a><span data-ttu-id="badaf-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="badaf-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="badaf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="badaf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="badaf-105">Beschreibt eine Zeile in einer Tabelle, die von einem bestimmten Ereignistyp betroffen ist, z. B. eine Änderung oder einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="badaf-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="badaf-106">Dadurch wird eine Tabellenbenachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="badaf-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="badaf-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="badaf-107">Header file:</span></span>  <br/> |<span data-ttu-id="badaf-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="badaf-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="badaf-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="badaf-109">Members</span></span>

<span data-ttu-id="badaf-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="badaf-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="badaf-111">Bitmaske von Flags, die zum Darstellen des Tabellenereignistyps verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="badaf-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="badaf-112">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="badaf-112">The following flags can be set:</span></span>
    
<span data-ttu-id="badaf-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="badaf-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="badaf-114">Gibt auf einer hohen Ebene an, dass sich etwas an der Tabelle geändert hat.</span><span class="sxs-lookup"><span data-stu-id="badaf-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="badaf-115">Der Zustand der Tabelle ist so wie vor dem Ereignis.</span><span class="sxs-lookup"><span data-stu-id="badaf-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="badaf-116">Dies bedeutet, **dass PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) -Eigenschaften, Lesezeichen, aktuelle Positionierung und Auswahl der Benutzeroberflächen weiterhin gültig sind.</span><span class="sxs-lookup"><span data-stu-id="badaf-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="badaf-117">Behandeln Sie dieses Ereignis, indem Sie die Tabelle erneut lesen.</span><span class="sxs-lookup"><span data-stu-id="badaf-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="badaf-118">Dienstanbieter, die keine Rich-Table-Benachrichtigungen implementieren möchten, senden TABLE_CHANGED anstatt ausführlichere Ereignisse, um einen bestimmten Änderungstyp anzugeben.</span><span class="sxs-lookup"><span data-stu-id="badaf-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="badaf-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="badaf-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="badaf-120">Ein Fehler ist aufgetreten, in der Regel während der Verarbeitung eines asynchronen Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="badaf-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="badaf-121">Fehler bei der Verarbeitung der folgenden Methoden können dieses Ereignis generieren:</span><span class="sxs-lookup"><span data-stu-id="badaf-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="badaf-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="badaf-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="badaf-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="badaf-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="badaf-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="badaf-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="badaf-125">Nachdem ein TABLE_ERROR empfangen wurde, kann sich ein Client nicht mehr auf die Genauigkeit des Tabelleninhalts verlassen.</span><span class="sxs-lookup"><span data-stu-id="badaf-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="badaf-126">Außerdem gehen ausstehende Benachrichtigungen zu anderen Änderungen möglicherweise verloren.</span><span class="sxs-lookup"><span data-stu-id="badaf-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="badaf-127">Die [IMAPITable::GetLastError-Methode](imapitable-getlasterror.md) stellt möglicherweise keine zusätzlichen Informationen zu dem Fehler zur Verfügung, da er an einem früheren Punkt generiert wurde, nicht unbedingt aus dem letzten Methodenaufruf.</span><span class="sxs-lookup"><span data-stu-id="badaf-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="badaf-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="badaf-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="badaf-129">Die Daten in der Tabelle sollten neu geladen werden.</span><span class="sxs-lookup"><span data-stu-id="badaf-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="badaf-130">Dienstanbieter senden TABLE_RELOAD, wenn beispielsweise die zugrunde liegenden Daten in einer Datenbank gespeichert und die Datenbank ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="badaf-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="badaf-131">Behandeln Sie dieses Ereignis, indem Sie davon ausgegangen werden, dass nichts über die Tabelle noch gültig ist, und indem Sie die Tabelle erneut lesen.</span><span class="sxs-lookup"><span data-stu-id="badaf-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="badaf-132">Alle Lesezeichen, Instanzschlüssel, Status- und Positionierungsinformationen sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="badaf-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="badaf-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="badaf-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="badaf-134">Ein Einschränkungsvorgang, der mit einem **IMAPITable::Restrict-Methodenaufruf** initiiert wurde, wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="badaf-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="badaf-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="badaf-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="badaf-136">Der Tabelle wurde eine neue Zeile hinzugefügt und das entsprechende Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="badaf-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="badaf-137">TABLE_ROW_ADDED werden nach einem Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) generiert.</span><span class="sxs-lookup"><span data-stu-id="badaf-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="badaf-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="badaf-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="badaf-139">Eine Zeile wurde aus der Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="badaf-139">A row has been removed from the table.</span></span> <span data-ttu-id="badaf-140">Das **propPrior-Element** ist auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="badaf-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="badaf-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="badaf-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="badaf-142">Eine Zeile wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="badaf-142">A row has been changed.</span></span> <span data-ttu-id="badaf-143">Das **Zeilenm** member enthält die betroffenen Eigenschaften für die Zeile.</span><span class="sxs-lookup"><span data-stu-id="badaf-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="badaf-144">Mehrere TABLE_ROW_MODIFIED werden in der Reihenfolge gesendet, in der sie in der Tabellenansicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="badaf-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="badaf-145">TABLE_ROW_MODIFIED werden gesendet, nachdem Änderungen am entsprechenden Objekt mit einem Aufruf der **IMAPIProp::SaveChanges-Methode ausgeführt** wurden.</span><span class="sxs-lookup"><span data-stu-id="badaf-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="badaf-146">Wenn die geänderte Zeile jetzt die erste Zeile in der Tabelle ist, ist der Wert des Eigenschaftstags im **propPrior-Element** **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="badaf-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="badaf-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="badaf-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="badaf-148">Ein Spalteneinstellungsvorgang, der mit einem **IMAPITable::SetColumns-Methodenaufruf** initiiert wurde, wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="badaf-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="badaf-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="badaf-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="badaf-150">Ein mit einem **IMAPITable::SortTable-Methodenaufruf** initiierter Tabellensortierungsvorgang wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="badaf-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="badaf-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="badaf-151">**hResult**</span></span>
  
> <span data-ttu-id="badaf-152">HRESULT-Wert für den aufgetretenen Fehler, wenn das **ulTableEvent-Element** auf TABLE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="badaf-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="badaf-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="badaf-153">**propIndex**</span></span>
  
> <span data-ttu-id="badaf-154">[SPropValue-Struktur](spropvalue.md) für **die PR_INSTANCE_KEY-Eigenschaft** der betroffenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="badaf-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="badaf-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="badaf-155">**propPrior**</span></span>
  
> <span data-ttu-id="badaf-156">**SPropValue-Struktur** für **die PR_INSTANCE_KEY-Eigenschaft** der Zeile vor der betroffenen.</span><span class="sxs-lookup"><span data-stu-id="badaf-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="badaf-157">Wenn die betroffene Zeile die erste Zeile in der Tabelle ist, muss **propPrior** auf PR_NULL **und** nicht auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="badaf-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="badaf-158">Null ist kein gültiges Eigenschaftstag.</span><span class="sxs-lookup"><span data-stu-id="badaf-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="badaf-159">**row**</span><span class="sxs-lookup"><span data-stu-id="badaf-159">**row**</span></span>
  
> <span data-ttu-id="badaf-160">[SRow-Struktur,](srow.md) die die betroffene Zeile beschreibt.</span><span class="sxs-lookup"><span data-stu-id="badaf-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="badaf-161">Diese Struktur wird für alle Tabellenbenachrichtigungsereignisse gefüllt.</span><span class="sxs-lookup"><span data-stu-id="badaf-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="badaf-162">Bei Tabellenbenachrichtigungsereignissen, die keine Zeilendaten übergeben, wird **das cValues-Element** der **SRow-Struktur** auf Null und das **lpProps-Element** auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="badaf-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="badaf-163">Da diese **#A0** schreibgeschützt ist; clients must make a copy of it if they want to make modifications.</span><span class="sxs-lookup"><span data-stu-id="badaf-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="badaf-164">Die [ScDupPropset-Funktion](scduppropset.md) kann zum Erstellen der Kopie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="badaf-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="badaf-165">Hinweise</span><span class="sxs-lookup"><span data-stu-id="badaf-165">Remarks</span></span>

<span data-ttu-id="badaf-166">Die **STRUKTUR TABLE \_ NOTIFICATION** ist eines der Mitglieder der Strukturgewerkschaft, die im **Infom** member der [NOTIFICATION-Struktur enthalten](notification.md) ist.</span><span class="sxs-lookup"><span data-stu-id="badaf-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="badaf-167">Das **Element info** enthält eine TABLE **\_ NOTIFICATION-Struktur,** wenn **das ulEventType-Element** der Struktur auf _fnevTableModified festgelegt ist._</span><span class="sxs-lookup"><span data-stu-id="badaf-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="badaf-168">Die Reihenfolge und der Typ der Spalten im Zeilenm member spiegeln die Reihenfolge und den Typ wider, die zum Zeitpunkt der Benachrichtigung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="badaf-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="badaf-169">Die Reihenfolge und der Typ zum Zeitpunkt der Benachrichtigung sind nicht unbedingt identisch mit dem Zeitpunkt, zu dem die Benachrichtigung zugestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="badaf-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="badaf-170">Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.</span><span class="sxs-lookup"><span data-stu-id="badaf-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="badaf-171">**Thema**</span><span class="sxs-lookup"><span data-stu-id="badaf-171">**Topic**</span></span>|<span data-ttu-id="badaf-172">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="badaf-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="badaf-173">Ereignisbenachrichtigung in MAPI</span><span class="sxs-lookup"><span data-stu-id="badaf-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="badaf-174">Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.</span><span class="sxs-lookup"><span data-stu-id="badaf-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="badaf-175">Behandeln von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="badaf-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="badaf-176">Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.</span><span class="sxs-lookup"><span data-stu-id="badaf-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="badaf-177">Unterstützende Ereignisbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="badaf-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="badaf-178">Hier erfahren Sie, wie Dienstanbieter die **IMAPISupport-Methode** zum Generieren von Benachrichtigungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="badaf-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="badaf-179">Da Tabellenbenachrichtigungen asynchron sind, können Clients eine Benachrichtigung über eine hinzugefügte Zeile erhalten, nachdem sie über eine andere Möglichkeit von der Ergänzung gelernt haben.</span><span class="sxs-lookup"><span data-stu-id="badaf-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="badaf-180">Es ist möglich, ein TABLE_ERROR-Ereignis zu empfangen, wenn ein Fehler in einer **IMAPITable::Sort-,** **IMAPITable::Restrict-** oder **IMAPITable::SetColumns-Methode** auftritt oder wenn ein zugrunde liegender Prozess versucht, eine Tabelle mit z. B. neuen oder geänderten Zeilen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="badaf-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="badaf-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="badaf-181">See also</span></span>

- [<span data-ttu-id="badaf-182">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="badaf-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="badaf-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="badaf-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="badaf-184">SRow</span><span class="sxs-lookup"><span data-stu-id="badaf-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="badaf-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="badaf-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="badaf-186">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="badaf-186">MAPI Structures</span></span>](mapi-structures.md)

