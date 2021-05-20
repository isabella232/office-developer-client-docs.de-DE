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
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="4e385-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="4e385-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="4e385-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e385-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e385-105">Gibt einen Zeiger auf die Inhaltstabelle des Containers zurück.</span><span class="sxs-lookup"><span data-stu-id="4e385-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="4e385-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e385-106">Parameters</span></span>

 <span data-ttu-id="4e385-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4e385-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4e385-108">[in] Eine Bitmaske mit Flags, die steuert, wie die Inhaltstabelle zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4e385-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="4e385-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4e385-109">The following flags can be set:</span></span>
    
<span data-ttu-id="4e385-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="4e385-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="4e385-111">Die zugeordnete Inhaltstabelle des Containers sollte anstelle der Standardinhaltstabelle zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4e385-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="4e385-112">Dieses Flag wird nur für Ordner verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e385-112">This flag is used only with folders.</span></span> <span data-ttu-id="4e385-113">Die Nachrichten, die in der zugeordneten Inhaltstabelle enthalten sind, wurden mit dem MAPI_ASSOCIATED im Aufruf der [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e385-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="4e385-114">Clients verwenden in der Regel die zugeordnete Inhaltstabelle, um Formulare, Ansichten und andere ausgeblendete Nachrichten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4e385-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="4e385-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="4e385-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="4e385-116">Ermöglicht den Zugriff auf die Rechte frightsFreeBusySimple und frightsFreeBusyDetailed in **PR_MEMBER_RIGHTS**.</span><span class="sxs-lookup"><span data-stu-id="4e385-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="4e385-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="4e385-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="4e385-118">**GetContentsTable** kann erfolgreich zurückgeben, möglicherweise bevor die Tabelle dem Aufrufer zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="4e385-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="4e385-119">Wenn die Tabelle nicht verfügbar ist, kann durch einen nachfolgenden Tabellenaufruf ein Fehler verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="4e385-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="4e385-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4e385-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4e385-121">Fordert an, dass die Spalten, die Zeichenfolgendaten enthalten, im Unicode-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4e385-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="4e385-122">Wenn das MAPI_UNICODE nicht festgelegt ist, sollten die Zeichenfolgen im ANSI-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4e385-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="4e385-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="4e385-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="4e385-124">Zeigt Elemente an, die derzeit als "soft deleted" gekennzeichnet sind, d. h. sie befinden sich in der Aufbewahrungszeit für gelöschte Elemente.</span><span class="sxs-lookup"><span data-stu-id="4e385-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="4e385-125">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="4e385-125">_lppTable_</span></span>
  
> <span data-ttu-id="4e385-126">[out] Ein Zeiger auf einen Zeiger auf die Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="4e385-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4e385-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e385-127">Return value</span></span>

<span data-ttu-id="4e385-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e385-128">S_OK</span></span> 
  
> <span data-ttu-id="4e385-129">Die Inhaltstabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4e385-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="4e385-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="4e385-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="4e385-131">Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="4e385-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="4e385-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4e385-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4e385-133">Der Container hat keinen Inhalt und kann keine Inhaltstabelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4e385-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e385-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4e385-134">Remarks</span></span>

<span data-ttu-id="4e385-135">Die **IMAPIContainer::GetContentsTable-Methode** gibt einen Zeiger auf das Inhaltsverzeichnis eines Containers zurück.</span><span class="sxs-lookup"><span data-stu-id="4e385-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="4e385-136">Eine Inhaltstabelle enthält Zusammenfassungsinformationen zu Objekten im Container.</span><span class="sxs-lookup"><span data-stu-id="4e385-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="4e385-137">Inhaltstabellen verfügen über lange Spaltensätze.</span><span class="sxs-lookup"><span data-stu-id="4e385-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="4e385-138">Eine vollständige Liste der erforderlichen und optionalen Spalten in Inhaltstabellen finden Sie unter [Contents Tables](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4e385-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="4e385-139">Es ist möglich, dass einige Container keinen Inhalt haben.</span><span class="sxs-lookup"><span data-stu-id="4e385-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="4e385-140">Diese Container geben MAPI_E_NO_SUPPORT ihrer Implementierungen von **GetContentsTable zurück.**</span><span class="sxs-lookup"><span data-stu-id="4e385-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4e385-141">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="4e385-141">Notes to implementers</span></span>

<span data-ttu-id="4e385-142">Wenn Sie eine Inhaltstabelle für Ihren Container unterstützen, müssen Sie auch die folgenden Schritte tun:</span><span class="sxs-lookup"><span data-stu-id="4e385-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="4e385-143">Unterstützt Aufrufe der [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des Containers, um die **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) -Eigenschaft zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4e385-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="4e385-144">Zurückgeben **PR_CONTAINER_CONTENTS** als Reaktion auf einen Aufruf des Containers</span><span class="sxs-lookup"><span data-stu-id="4e385-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="4e385-145">[IMAPIProp::GetProps-](imapiprop-getprops.md) und [IMAPIProp::GetPropList-Methoden.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="4e385-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="4e385-146">Die Implementierung dieser Methode durch einen Remotetransportanbieter muss einen Zeiger auf eine [IMAPITable : IUnknown-Schnittstelle](imapitableiunknown.md) im  _ppTable-Parameter_ zurückgeben, der an die **GetContentsTable-Methode übergeben** wird.</span><span class="sxs-lookup"><span data-stu-id="4e385-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="4e385-147">Wenn Ihr Transportanbieter über eine vorhandene Inhaltstabelle verfügt, reicht es aus, einen Zeiger auf dieses zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="4e385-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="4e385-148">Wenn dies nicht der Fall ist, muss diese Methode ein neues [IMAPITable : IUnknown-Objekt](imapitableiunknown.md) erstellen, die Tabelle mit Nachrichtenkopfzeilen auffüllen (sofern vorhanden) und einen Zeiger auf die neue Tabelle zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4e385-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="4e385-149">Die [ITableData::HrGetView-Methode](itabledata-hrgetview.md) ist nützlich, um einen Rückgabewert zu generieren und den Tabellenzeiger im  _ppTable-Parameter zu_ speichern.</span><span class="sxs-lookup"><span data-stu-id="4e385-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="4e385-150">Die Inhaltstabelle muss mindestens die folgenden Eigenschaftenspalten unterstützen:</span><span class="sxs-lookup"><span data-stu-id="4e385-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="4e385-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="4e385-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4e385-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="4e385-169">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="4e385-169">Notes to callers</span></span>

<span data-ttu-id="4e385-170">Tabellenspalten mit Zeichenfolgen und binären Inhalten können abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="4e385-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="4e385-171">In der Regel geben Anbieter 255 Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="4e385-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="4e385-172">Da Sie vorher nicht wissen können, ob eine Tabelle abgeschnittene Spalten enthält, nehmen Sie an, dass eine Spalte abgeschnitten wird, wenn die Länge der Spalte entweder 255 oder 510 Byte beträgt.</span><span class="sxs-lookup"><span data-stu-id="4e385-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="4e385-173">Sie können jederzeit den vollständigen Wert einer abgeschnittenen Spalte bei Bedarf direkt aus dem Objekt abrufen, indem Sie den Eintragsbezeichner zum Öffnen verwenden und dann die **IMAPIProp::GetProps-Methode** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4e385-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="4e385-174">Abhängig von der Implementierung des Anbieters können Einschränkungen und Sortiervorgänge für alle Zeichenfolgen oder die abgeschnittene Version dieser Zeichenfolge gelten.</span><span class="sxs-lookup"><span data-stu-id="4e385-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4e385-175">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="4e385-175">MFCMAPI reference</span></span>

<span data-ttu-id="4e385-176">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4e385-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4e385-177">**Datei**</span><span class="sxs-lookup"><span data-stu-id="4e385-177">**File**</span></span>|<span data-ttu-id="4e385-178">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="4e385-178">**Function**</span></span>|<span data-ttu-id="4e385-179">**Comment**</span><span class="sxs-lookup"><span data-stu-id="4e385-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4e385-180">ContentsTableDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="4e385-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="4e385-181">CContentsTableDlg::CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="4e385-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="4e385-182">Die **CContentsTableDlg-Klasse** verwendet **GetContentsTable,** um die Einträge in einer Inhaltstabelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4e385-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e385-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e385-183">See also</span></span>



[<span data-ttu-id="4e385-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="4e385-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="4e385-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="4e385-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="4e385-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="4e385-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="4e385-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e385-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="4e385-188">PidTagContainerContents (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4e385-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="4e385-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4e385-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="4e385-190">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="4e385-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

