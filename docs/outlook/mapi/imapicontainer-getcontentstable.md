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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431106"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="c64fd-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="c64fd-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="c64fd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c64fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c64fd-105">Gibt einen Zeiger auf die Inhaltstabelle des Containers zurück.</span><span class="sxs-lookup"><span data-stu-id="c64fd-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="c64fd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c64fd-106">Parameters</span></span>

 <span data-ttu-id="c64fd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c64fd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c64fd-108">in Eine Bitmaske von Flags, die steuert, wie die Inhaltstabelle zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c64fd-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="c64fd-109">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c64fd-109">The following flags can be set:</span></span>
    
<span data-ttu-id="c64fd-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="c64fd-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="c64fd-111">Die Tabelle mit den zugeordneten Inhalten des Containers sollte anstelle der Standardinhalts Tabelle zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c64fd-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="c64fd-112">Dieses Flag wird nur mit Ordnern verwendet.</span><span class="sxs-lookup"><span data-stu-id="c64fd-112">This flag is used only with folders.</span></span> <span data-ttu-id="c64fd-113">Die Nachrichten, die in der Tabelle zugeordnete Inhalte enthalten sind, wurden mit dem MAPI_ASSOCIATED-Flag erstellt, das im Aufruf der [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="c64fd-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="c64fd-114">Clients verwenden in der Regel die zugeordnete Inhaltstabelle, um Formulare, Ansichten und andere ausgeblendete Nachrichten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c64fd-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="c64fd-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="c64fd-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="c64fd-116">Ermöglicht den Zugriff auf die frightsFreeBusySimple-und frightsFreeBusyDetailed-Rechte in **PR_MEMBER_RIGHTS**.</span><span class="sxs-lookup"><span data-stu-id="c64fd-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="c64fd-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c64fd-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c64fd-118">\*\*\*\* Getcontentable kann erfolgreich zurückgegeben werden, bevor die Tabelle dem Aufrufer zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c64fd-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="c64fd-119">Wenn die Tabelle nicht verfügbar ist, kann durch einen nachfolgenden Tabellen Aufruf ein Fehler ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="c64fd-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="c64fd-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c64fd-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c64fd-121">Fordert an, dass die Spalten, die Zeichenfolgendaten enthalten, im Unicode-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c64fd-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="c64fd-122">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c64fd-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="c64fd-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="c64fd-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="c64fd-124">Zeigt Elemente an, die derzeit als weich gelöscht markiert sind, d. h., Sie befinden sich in der Aufbewahrungszeit für gelöschte Elemente.</span><span class="sxs-lookup"><span data-stu-id="c64fd-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="c64fd-125">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="c64fd-125">_lppTable_</span></span>
  
> <span data-ttu-id="c64fd-126">Out Ein Zeiger auf einen Zeiger auf die Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="c64fd-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c64fd-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c64fd-127">Return value</span></span>

<span data-ttu-id="c64fd-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="c64fd-128">S_OK</span></span> 
  
> <span data-ttu-id="c64fd-129">Die Inhaltstabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c64fd-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="c64fd-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c64fd-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c64fd-131">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="c64fd-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="c64fd-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c64fd-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c64fd-133">Der Container hat keinen Inhalt und kann keine Inhaltstabelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c64fd-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c64fd-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c64fd-134">Remarks</span></span>

<span data-ttu-id="c64fd-135">Die **IMAPIContainer::** getcontentable-Methode gibt einen Zeiger auf die Inhaltstabelle eines Containers zurück.</span><span class="sxs-lookup"><span data-stu-id="c64fd-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="c64fd-136">Eine Inhaltstabelle enthält zusammenfassende Informationen zu Objekten im Container.</span><span class="sxs-lookup"><span data-stu-id="c64fd-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="c64fd-137">Inhaltstabellen haben lange Spaltensätze.</span><span class="sxs-lookup"><span data-stu-id="c64fd-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="c64fd-138">Eine vollständige Liste der erforderlichen und optionalen Spalten in Inhaltstabellen finden Sie unter [Inhaltstabellen](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c64fd-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="c64fd-139">Es ist möglich, dass einige Container keinen Inhalt haben.</span><span class="sxs-lookup"><span data-stu-id="c64fd-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="c64fd-140">Diese Container geben MAPI_E_NO_SUPPORT aus ihren Implementierungen \*\*\*\* von getcontentable zurück.</span><span class="sxs-lookup"><span data-stu-id="c64fd-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c64fd-141">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="c64fd-141">Notes to implementers</span></span>

<span data-ttu-id="c64fd-142">Wenn Sie eine Inhaltstabelle für ihren Container unterstützen, müssen Sie auch Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="c64fd-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="c64fd-143">Unterstützen Sie Aufrufe der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Containers, um die **PR_CONTAINER_CONTENTS** ([pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md))-Eigenschaft zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c64fd-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="c64fd-144">Zurückgeben von **PR_CONTAINER_CONTENTS** als Reaktion auf einen Aufruf des Containers</span><span class="sxs-lookup"><span data-stu-id="c64fd-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="c64fd-145">[IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methoden.</span><span class="sxs-lookup"><span data-stu-id="c64fd-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="c64fd-146">Die Implementierung dieser Methode durch einen Remote Transportanbieter muss einen Zeiger auf eine [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle im _ppTable_ -Parameter zurückgeben, der an die getcontentable-Methode übergeben wird. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c64fd-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="c64fd-147">Wenn Ihr Transportanbieter über eine vorhandene Inhaltstabelle verfügt, genügt es, einen Zeiger darauf zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c64fd-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="c64fd-148">Wenn dies nicht der Fall ist, muss diese Methode ein neues [IMAPITable: IUnknown](imapitableiunknown.md) -Objekt erstellen, die Tabelle mit Nachrichtenheadern Auffüllen (sofern vorhanden), und einen Zeiger auf die neue Tabelle zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c64fd-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="c64fd-149">Die [ITableData:: HrGetView](itabledata-hrgetview.md) -Methode ist nützlich, um einen Rückgabewert zu generieren und den Tabellen Zeiger im _ppTable_ -Parameter zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c64fd-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="c64fd-150">Die Contents-Tabelle muss mindestens die folgenden Eigenschaftsspalten unterstützen:</span><span class="sxs-lookup"><span data-stu-id="c64fd-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="c64fd-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-155">**PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-158">**PR_MESSAGE_SIZE** ([Pidtagmessagesize (](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-159">**PR_PRIORITY** ([Pidtagpriority (](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-162">**PR_MESSAGE_DELIVERY_TIME** ([Pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-163">**PR_MSG_STATUS** ([Pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-164">**PR_MESSAGE_DOWNLOAD_TIME** ([Pidtagmessagedownloadtime (](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-165">**PR_HASATTACH** ([Pidtaghasattachments (](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-166">**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-167">**PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="c64fd-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c64fd-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="c64fd-169">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c64fd-169">Notes to callers</span></span>

<span data-ttu-id="c64fd-170">Tabellenspalten für String-und Binary-Inhalte können abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="c64fd-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="c64fd-171">In der Regel geben Anbieter 255 Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="c64fd-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="c64fd-172">Da Sie nicht vorher wissen können, ob eine Tabelle abgeschnittene Spalten enthält, wird davon ausgegangen, dass eine Spalte abgeschnitten wird, wenn die Länge der Spalte 255 oder 510 Byte beträgt.</span><span class="sxs-lookup"><span data-stu-id="c64fd-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="c64fd-173">Sie können den vollständigen Wert einer abgeschnittenen Spalte, falls erforderlich, jederzeit direkt aus dem Objekt abrufen, indem Sie die Eintrags-ID verwenden, um Sie zu öffnen und dann die **IMAPIProp::** GetProps-Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c64fd-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="c64fd-174">Abhängig von der Implementierung des Anbieters können Einschränkungen und Sortiervorgänge für alle Zeichenfolgen oder die gekürzte Version dieser Zeichenfolge gelten.</span><span class="sxs-lookup"><span data-stu-id="c64fd-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c64fd-175">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="c64fd-175">MFCMAPI reference</span></span>

<span data-ttu-id="c64fd-176">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c64fd-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c64fd-177">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c64fd-177">**File**</span></span>|<span data-ttu-id="c64fd-178">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c64fd-178">**Function**</span></span>|<span data-ttu-id="c64fd-179">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c64fd-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c64fd-180">ContentsTableDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="c64fd-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="c64fd-181">CContentsTableDlg:: CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="c64fd-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="c64fd-182">Die **CContentsTableDlg** -Klasse \*\*\*\* verwendet getcontentable, um die Einträge in einer Inhaltstabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c64fd-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c64fd-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c64fd-183">See also</span></span>



[<span data-ttu-id="c64fd-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="c64fd-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="c64fd-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="c64fd-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="c64fd-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="c64fd-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="c64fd-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c64fd-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="c64fd-188">Kanonische Pidtagcontainercontents (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c64fd-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="c64fd-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c64fd-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="c64fd-190">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c64fd-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

