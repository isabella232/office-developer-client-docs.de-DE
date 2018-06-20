---
title: IMAPIContainerGetContentsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 871dafd7bf8959cf814d65991fe08fdb2b283c08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792082"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="d1a3a-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="d1a3a-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="d1a3a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1a3a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d1a3a-105">Gibt einen Zeiger auf den Container Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="d1a3a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1a3a-106">Parameters</span></span>

 <span data-ttu-id="d1a3a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d1a3a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d1a3a-108">[in] Eine Bitmaske aus Flags, die steuert, wie die Inhaltstabelle zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="d1a3a-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d1a3a-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d1a3a-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="d1a3a-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="d1a3a-111">Der Container zugeordneten Inhaltstabelle sollten anstelle der standard Inhaltstabelle zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="d1a3a-112">Dieses Kennzeichen werden nur bei Ordnern verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-112">This flag is used only with folders.</span></span> <span data-ttu-id="d1a3a-113">Die Nachrichten, die in der zugehörigen Inhaltstabelle enthalten sind wurden mit dem MAPI_ASSOCIATED-Flag festlegen im Aufruf der [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode erstellt.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="d1a3a-114">Clients verwenden in der Regel die zugehörige Inhaltstabelle, um Formulare, Ansichten und anderen ausgeblendeten Nachrichten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="d1a3a-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="d1a3a-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="d1a3a-116">Ermöglicht den Zugriff auf die Rechte FrightsFreeBusySimple und FrightsFreeBusyDetailed in **PR_MEMBER_RIGHTS**.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="d1a3a-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d1a3a-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d1a3a-118">**GetContentsTable** können erfolgreich, möglicherweise beendet, bevor die Tabelle mit dem Anrufer verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="d1a3a-119">Wenn die Tabelle nicht verfügbar ist, kann die nachfolgenden Tabelle Anrufen ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="d1a3a-120">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d1a3a-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d1a3a-121">Anforderungen, die die Spalten, die Zeichenfolgendaten enthält das Unicode-Format zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="d1a3a-122">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sollte die Zeichenfolgen in ANSI-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="d1a3a-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="d1a3a-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="d1a3a-124">Zeigt Elemente, die derzeit als soft gekennzeichnet sind gelöscht – d. h., sie sind in der Aufbewahrungszeit für gelöschte Elemente Zeit Phase.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="d1a3a-125">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="d1a3a-125">_lppTable_</span></span>
  
> <span data-ttu-id="d1a3a-126">[out] Ein Zeiger auf einen Zeiger auf die Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d1a3a-127">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d1a3a-127">Return value</span></span>

<span data-ttu-id="d1a3a-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1a3a-128">S_OK</span></span> 
  
> <span data-ttu-id="d1a3a-129">Die Inhaltstabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="d1a3a-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d1a3a-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d1a3a-131">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="d1a3a-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d1a3a-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d1a3a-133">Der Container über keinen Inhalt verfügt und eine Inhaltstabelle nicht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1a3a-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d1a3a-134">Remarks</span></span>

<span data-ttu-id="d1a3a-135">Die **IMAPIContainer::GetContentsTable** -Methode gibt einen Zeiger auf die Inhaltstabelle eines Containers.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="d1a3a-136">Eine Inhaltstabelle enthält zusammenfassende Informationen zu Objekten im Container.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="d1a3a-137">Inhalt Tabellen haben langen Spalte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="d1a3a-138">Eine vollständige Liste der erforderlichen und optionalen Spalten in Tabellen Inhalt finden Sie unter [Inhalt Tabellen](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d1a3a-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="d1a3a-139">Es ist möglich, dass einige Container keinen Inhalt haben.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="d1a3a-140">Diese Container zurück MAPI_E_NO_SUPPORT aus ihrer Implementierungen von **GetContentsTable**.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d1a3a-141">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="d1a3a-141">Notes to implementers</span></span>

<span data-ttu-id="d1a3a-142">Wenn Sie eine Inhaltstabelle für den Container unterstützen, müssen Sie auch Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d1a3a-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="d1a3a-143">Supportanrufe an den Container [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Öffnen der **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="d1a3a-144">Zurückgeben von **PR_CONTAINER_CONTENTS** Reaktion auf einen Aufruf an des Containers</span><span class="sxs-lookup"><span data-stu-id="d1a3a-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="d1a3a-145">[IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="d1a3a-146">Eine remote Adressbuchhierarchie Implementierung dieser Methode muss einen Zeiger auf Zurückgeben einer [IMAPITable: IUnknown](imapitableiunknown.md) Schnittstelle in der _PpTable_ -Parameter an **den Befehl GetContentsTable** übergeben.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="d1a3a-147">Wenn Ihre Adressbuchhierarchie eine vorhandenen Inhaltstabelle aufweist, ist es ausreichend, um einen Zeiger darauf zurück.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="d1a3a-148">Wenn nicht, diese Methode ein neues erstellen muss [IMAPITable: IUnknown](imapitableiunknown.md) -Objekts, füllen Sie die Tabelle mit Kopfzeilen (falls verfügbar) und ein Zeiger auf die neue Tabelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="d1a3a-149">Die [ITableData::HrGetView](itabledata-hrgetview.md) -Methode eignet sich für ein Rückgabewert generieren und Speichern von der Tabelle Zeiger in der _PpTable_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="d1a3a-150">Die Inhaltstabelle muss mindestens die folgenden Spalten unterstützen:</span><span class="sxs-lookup"><span data-stu-id="d1a3a-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="d1a3a-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="d1a3a-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d1a3a-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="d1a3a-169">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d1a3a-169">Notes to callers</span></span>

<span data-ttu-id="d1a3a-170">Zeichenfolge und der binären Inhalt Tabellenspalten können abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="d1a3a-171">In der Regel zurückgeben Anbieter 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="d1a3a-172">Da Sie im Voraus wissen können nicht, ob eine Tabelle abgeschnittene Spalten enthält, wird davon ausgegangen Sie, dass eine Spalte abgeschnitten wird, wenn die Länge der Spalte 510 maximal 255 Bytes ist.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="d1a3a-173">Sie können immer den vollständigen Wert der abgeschnittene Spalte an, falls erforderlich, direkt aus dem Objekt mithilfe der Eintrags-ID um zu öffnen und anschließendes Aufrufen der **IMAPIProp::GetProps** -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="d1a3a-174">Je nach der Implementierung des Anbieters, Einschränkungen und Sortierung Vorgänge können auf alle einer Zeichenfolge oder auf die abgeschnittene Version dieser Zeichenfolge anwenden.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d1a3a-175">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="d1a3a-175">MFCMAPI reference</span></span>

<span data-ttu-id="d1a3a-176">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d1a3a-177">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d1a3a-177">**File**</span></span>|<span data-ttu-id="d1a3a-178">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d1a3a-178">**Function**</span></span>|<span data-ttu-id="d1a3a-179">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d1a3a-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d1a3a-180">ContentsTableDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="d1a3a-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="d1a3a-181">CContentsTableDlg::CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="d1a3a-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="d1a3a-182">Die **CContentsTableDlg** -Klasse verwendet **GetContentsTable** , um die Einträge in einer Inhaltstabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d1a3a-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1a3a-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1a3a-183">See also</span></span>



[<span data-ttu-id="d1a3a-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="d1a3a-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="d1a3a-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="d1a3a-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="d1a3a-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="d1a3a-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="d1a3a-187">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d1a3a-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="d1a3a-188">Kanonische PidTagContainerContents-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d1a3a-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="d1a3a-189">IMAPIContainer: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d1a3a-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="d1a3a-190">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="d1a3a-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

