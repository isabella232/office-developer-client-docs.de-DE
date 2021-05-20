---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436573"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="85dda-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="85dda-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="85dda-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85dda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85dda-105">Fügt einem Nachrichtenspeicher standardmäßige IPM-Ordner (Interpersonal Message) hinzu.</span><span class="sxs-lookup"><span data-stu-id="85dda-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85dda-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="85dda-106">Header file:</span></span>  <br/> |<span data-ttu-id="85dda-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="85dda-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="85dda-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="85dda-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="85dda-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="85dda-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="85dda-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="85dda-110">Called by:</span></span>  <br/> |<span data-ttu-id="85dda-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="85dda-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="85dda-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="85dda-112">Parameters</span></span>

 <span data-ttu-id="85dda-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="85dda-113">_lpMDB_</span></span>
  
> <span data-ttu-id="85dda-114">[in] Zeiger auf das Nachrichtenspeicherobjekt, dem die Ordner hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="85dda-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="85dda-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="85dda-115">_ulFlags_</span></span>
  
> <span data-ttu-id="85dda-116">[in] Bitmaske von Flags, die verwendet werden, um zu steuern, wie die Ordner erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="85dda-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="85dda-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="85dda-117">The following flags can be set:</span></span>
    
<span data-ttu-id="85dda-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="85dda-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="85dda-119">Die Ordner sollten vor der Erstellung überprüft werden, auch wenn Nachrichtenspeichereigenschaften angeben, dass sie gültig sind.</span><span class="sxs-lookup"><span data-stu-id="85dda-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="85dda-120">Eine Clientanwendung legt dieses Flag in der Regel fest, wenn ein Fehler darauf hinweist, dass die Struktur eines vorhandenen Ordners beschädigt wurde.</span><span class="sxs-lookup"><span data-stu-id="85dda-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="85dda-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="85dda-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="85dda-122">Der vollständige Satz von IPM-Ordnern sollte im Stammordner des Nachrichtenspeichers erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="85dda-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="85dda-123">Die Ordnertitel in der Hierarchie sind:</span><span class="sxs-lookup"><span data-stu-id="85dda-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="85dda-124">Ordneransichten</span><span class="sxs-lookup"><span data-stu-id="85dda-124">Folder Views</span></span>
    
    - <span data-ttu-id="85dda-125">Allgemeine Ansichten</span><span class="sxs-lookup"><span data-stu-id="85dda-125">Common Views</span></span>
    
    - <span data-ttu-id="85dda-126">Suchstamm\*</span><span class="sxs-lookup"><span data-stu-id="85dda-126">Search Root\*</span></span>
    
    - <span data-ttu-id="85dda-127">IPM-Unterstruktur\*</span><span class="sxs-lookup"><span data-stu-id="85dda-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="85dda-128">Posteingang</span><span class="sxs-lookup"><span data-stu-id="85dda-128">Inbox</span></span>
    
    - <span data-ttu-id="85dda-129">Postausgang</span><span class="sxs-lookup"><span data-stu-id="85dda-129">Outbox</span></span>
    
    - <span data-ttu-id="85dda-130">Gelöschte Elemente\*</span><span class="sxs-lookup"><span data-stu-id="85dda-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="85dda-131">Gesendete Elemente</span><span class="sxs-lookup"><span data-stu-id="85dda-131">Sent Items</span></span>
    
    <span data-ttu-id="85dda-132">dabei sind die drei mit markierten Ordner die Mindestanzahl, die auch dann erstellt wird, wenn das MAPI_FULL_IPM_TREE nicht \* festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="85dda-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="85dda-133">Eine Clientanwendung legt dieses Flag in der Regel fest, wenn der Nachrichtenspeicher, in dem die Ordner erstellt werden sollen, der Standardspeicher ist.</span><span class="sxs-lookup"><span data-stu-id="85dda-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="85dda-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="85dda-134">_lpcValues_</span></span>
  
> <span data-ttu-id="85dda-135">[in, out] Zeiger auf die Anzahl [der SPropValue-Strukturen](spropvalue.md) im Array, das im  _lppProps-Parameter zurückgegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="85dda-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="85dda-136">Der Wert des  _lpcValues-Parameters_ kann null sein, wenn  _lppProps_ NULL ist.</span><span class="sxs-lookup"><span data-stu-id="85dda-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="85dda-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="85dda-137">_lppProps_</span></span>
  
> <span data-ttu-id="85dda-138">[in, out] Zeiger auf einen Zeiger auf ein Array von **SPropValue-Strukturen,** das Eigenschaftswerte für die **PR_VALID_FOLDER_MASK** -[PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)-Eigenschaft und für die entsprechenden Eigenschaften der Ordnereintrags-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="85dda-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="85dda-139">Wenn **HrValidateIPMSubtree** einen Posteingang im Nachrichtenspeicher erstellt, enthält das **SPropValue-Array** einen Posteingangseintragsbezeichner mit einem speziellen Eigenschaftstag, das als codiert  `PROP_TAG(PT_BINARY, PROP_ID_NULL)` ist.</span><span class="sxs-lookup"><span data-stu-id="85dda-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="85dda-140">Der  _lppProps-Parameter_ kann NULL sein, was angibt, dass für die aufrufende Implementierung kein **SPropValue-Array** zurückgegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="85dda-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="85dda-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="85dda-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="85dda-142">[out] Zeiger auf einen Zeiger auf eine [MAPIERROR-Struktur,](mapierror.md) die Versions-, Komponenten- und Kontextinformationen für einen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="85dda-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="85dda-143">Der  _lppMAPIError-Parameter_ ist auf NULL festgelegt, wenn keine **MAPIERROR-Struktur** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="85dda-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="85dda-144">Return value</span><span class="sxs-lookup"><span data-stu-id="85dda-144">Return value</span></span>

<span data-ttu-id="85dda-145">Keine.</span><span class="sxs-lookup"><span data-stu-id="85dda-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85dda-146">Hinweise</span><span class="sxs-lookup"><span data-stu-id="85dda-146">Remarks</span></span>

<span data-ttu-id="85dda-147">MAPI verwendet die **HrValidateIPMSubtree-Funktion** intern, um die standardmäßige IPM-Unterstruktur in einem Nachrichtenspeicher zu erstellen, wenn der Speicher zum ersten Mal geöffnet wird oder wenn ein Speicher zum Standardspeicher gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="85dda-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="85dda-148">Diese Funktion kann auch von Clientanwendungen verwendet werden, um Standardnachrichtenordner zu überprüfen oder zu reparieren.</span><span class="sxs-lookup"><span data-stu-id="85dda-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="85dda-149">**HrValidateIPMSubtree** erstellt immer die Ordner Suchstamm und IPM-Unterstruktur im Stammordner des Speichers und den Ordner Gelöschte Elemente im Ordner "IPM Subtree".</span><span class="sxs-lookup"><span data-stu-id="85dda-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="85dda-150">Der Ordner "IPM-Unterstruktur" ist der Stamm der IPM-Hierarchie in diesem Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="85dda-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="85dda-151">Der Ordner "Suchstamm" kann als Stamm einer Unterstruktur für Suchergebnisordner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85dda-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="85dda-152">IPM-Clients sollten ihre Ordneransicht ab dem Stammordner der IPM-Unterstruktur und untergeordnete Ordner darunter anzeigen.</span><span class="sxs-lookup"><span data-stu-id="85dda-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="85dda-153">Informationen im Stammordner eines Nachrichtenspeichers sollten nicht auf der Benutzeroberfläche eines Clients angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="85dda-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="85dda-154">Diese Funktionalität bedeutet, dass, wenn ein Client Informationen ausblenden muss, die Informationen im Stammverzeichnis der IPM-Unterstruktur gespeichert werden können, wo sie für den Benutzer nicht sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="85dda-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="85dda-155">Im Gegensatz dazu können Nicht-IPM-Anwendungen, bei denen Nachrichten und Ordner für den Benutzer unsichtbar sein müssen, z. B. in einem serverbasierten Nachrichtenspeicher, diese außerhalb der IPM-Hierarchie setzen.</span><span class="sxs-lookup"><span data-stu-id="85dda-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="85dda-156">**HrValidateIPMSubtree** legt die **PR_VALID_FOLDER_MASK** fest, um anzugeben, ob jeder erstellte IPM-Ordner über einen gültigen Eintragsbezeichner verfügt.</span><span class="sxs-lookup"><span data-stu-id="85dda-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="85dda-157">Die folgenden Eintragsbezeichnereigenschaften des Nachrichtenspeichers werden auf die Eintragsbezeichner der entsprechenden Ordner festgelegt und zusammen mit dem Parameter _"lppProps"_ **PR_VALID_FOLDER_MASK:**</span><span class="sxs-lookup"><span data-stu-id="85dda-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="85dda-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85dda-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="85dda-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85dda-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="85dda-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85dda-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="85dda-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85dda-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="85dda-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85dda-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="85dda-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85dda-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="85dda-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="85dda-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="85dda-165">Ein Platzhalter [PROP_TAG](prop_tag.md) für den IPM-Posteingang (PT_BINARY, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="85dda-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="85dda-166">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="85dda-166">MFCMAPI reference</span></span>

<span data-ttu-id="85dda-167">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="85dda-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="85dda-168">**Datei**</span><span class="sxs-lookup"><span data-stu-id="85dda-168">**File**</span></span>|<span data-ttu-id="85dda-169">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="85dda-169">**Function**</span></span>|<span data-ttu-id="85dda-170">**Comment**</span><span class="sxs-lookup"><span data-stu-id="85dda-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="85dda-171">MstStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="85dda-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="85dda-172">CMsgStoreDlg::OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="85dda-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="85dda-173">MFCMAPI verwendet die **HrValidateIPMSubtree-Methode,** um Einem Nachrichtenspeicher Standardordner hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="85dda-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85dda-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85dda-174">See also</span></span>



[<span data-ttu-id="85dda-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="85dda-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="85dda-176">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="85dda-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

