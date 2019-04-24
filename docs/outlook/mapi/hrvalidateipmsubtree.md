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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346767"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="8e40d-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="8e40d-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="8e40d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e40d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e40d-105">Fügt einem Nachrichtenspeicher standardmäßige zwischenmenschliche Nachrichten-Ordner hinzu.</span><span class="sxs-lookup"><span data-stu-id="8e40d-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e40d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8e40d-106">Header file:</span></span>  <br/> |<span data-ttu-id="8e40d-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="8e40d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8e40d-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="8e40d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8e40d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8e40d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8e40d-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="8e40d-110">Called by:</span></span>  <br/> |<span data-ttu-id="8e40d-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="8e40d-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="8e40d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e40d-112">Parameters</span></span>

 <span data-ttu-id="8e40d-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="8e40d-113">_lpMDB_</span></span>
  
> <span data-ttu-id="8e40d-114">in Zeiger auf das Nachrichtenspeicherobjekt, dem die Ordner hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8e40d-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="8e40d-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e40d-115">_ulFlags_</span></span>
  
> <span data-ttu-id="8e40d-116">in Bitmaske der Flags, die verwendet werden, um zu steuern, wie die Ordner erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8e40d-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="8e40d-117">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="8e40d-117">The following flags can be set:</span></span>
    
<span data-ttu-id="8e40d-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="8e40d-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="8e40d-119">Die Ordner sollten vor der Erstellung überprüft werden, auch wenn die Eigenschaften des Nachrichtenspeichers darauf hinweisen, dass Sie gültig sind.</span><span class="sxs-lookup"><span data-stu-id="8e40d-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="8e40d-120">Eine Clientanwendung legt dieses Flag in der Regel fest, wenn ein Fehler darauf hinweist, dass die Struktur eines vorhandenen Ordners beschädigt wurde.</span><span class="sxs-lookup"><span data-stu-id="8e40d-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="8e40d-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="8e40d-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="8e40d-122">Der vollständige Satz von IPM-Ordnern sollte im Stammordner des Nachrichtenspeichers erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8e40d-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="8e40d-123">Die Ordnertitel in der Hierarchie sind:</span><span class="sxs-lookup"><span data-stu-id="8e40d-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="8e40d-124">Ordneransichten</span><span class="sxs-lookup"><span data-stu-id="8e40d-124">Folder Views</span></span>
    
    - <span data-ttu-id="8e40d-125">Allgemeine Ansichten</span><span class="sxs-lookup"><span data-stu-id="8e40d-125">Common Views</span></span>
    
    - <span data-ttu-id="8e40d-126">Such Stamm\*</span><span class="sxs-lookup"><span data-stu-id="8e40d-126">Search Root\*</span></span>
    
    - <span data-ttu-id="8e40d-127">IPM-unterStruktur\*</span><span class="sxs-lookup"><span data-stu-id="8e40d-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="8e40d-128">Posteingang</span><span class="sxs-lookup"><span data-stu-id="8e40d-128">Inbox</span></span>
    
    - <span data-ttu-id="8e40d-129">Postausgang</span><span class="sxs-lookup"><span data-stu-id="8e40d-129">Outbox</span></span>
    
    - <span data-ttu-id="8e40d-130">Gelöschte Elemente\*</span><span class="sxs-lookup"><span data-stu-id="8e40d-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="8e40d-131">Gesendete Elemente</span><span class="sxs-lookup"><span data-stu-id="8e40d-131">Sent Items</span></span>
    
    <span data-ttu-id="8e40d-132">Dabei sind die drei mit \* gekennzeichneten Ordner der Mindestsatz, der auch dann erstellt wird, wenn das MAPI_FULL_IPM_TREE-Flag nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8e40d-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="8e40d-133">Eine Clientanwendung legt dieses Flag in der Regel fest, wenn der Nachrichtenspeicher, in dem die Ordner erstellt werden sollen, der Standardspeicher ist.</span><span class="sxs-lookup"><span data-stu-id="8e40d-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="8e40d-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="8e40d-134">_lpcValues_</span></span>
  
> <span data-ttu-id="8e40d-135">[in, out] Zeiger auf die Anzahl der [SPropValue](spropvalue.md) -Strukturen im Array, die im _lppProps_ -Parameter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8e40d-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="8e40d-136">Der Wert des _lpcValues_ -Parameters kann NULL sein, wenn _lppProps_ NULL ist.</span><span class="sxs-lookup"><span data-stu-id="8e40d-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="8e40d-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="8e40d-137">_lppProps_</span></span>
  
> <span data-ttu-id="8e40d-138">[in, out] Zeiger auf einen Zeiger auf ein Array von **SPropValue** -Strukturen, die Eigenschaftswerte für die **PR_VALID_FOLDER_MASK** ([pidtagvalidfoldermask (](pidtagvalidfoldermask-canonical-property.md))-Eigenschaft und die entsprechenden Eigenschaften für die Ordnereintrags-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="8e40d-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="8e40d-139">Wenn **HrValidateIPMSubtree** einen Posteingang im Nachrichtenspeicher erstellt, enthält das **SPropValue** -Array eine Posteingangs-ID mit einem speziellen Eigenschafts, das als `PROP_TAG(PT_BINARY, PROP_ID_NULL)`codiert ist.</span><span class="sxs-lookup"><span data-stu-id="8e40d-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="8e40d-140">Der _lppProps_ -Parameter kann NULL sein, wodurch angegeben wird, dass für die aufrufende Implementierung kein **SPropValue** -Array zurückgegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="8e40d-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="8e40d-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="8e40d-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="8e40d-142">Out Zeiger auf einen Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur, die Versions-, Komponenten-und Kontextinformationen für einen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="8e40d-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="8e40d-143">Der Parameter _lppMAPIError_ wird auf NULL festgelegt, wenn keine **MAPIERROR** -Struktur zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8e40d-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8e40d-144">Return value</span><span class="sxs-lookup"><span data-stu-id="8e40d-144">Return value</span></span>

<span data-ttu-id="8e40d-145">Keine.</span><span class="sxs-lookup"><span data-stu-id="8e40d-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8e40d-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e40d-146">Remarks</span></span>

<span data-ttu-id="8e40d-147">MAPI verwendet die **HrValidateIPMSubtree** -Funktion intern, um die standardmäßige IPM-Unterstruktur in einem Nachrichtenspeicher zu erstellen, wenn der Informationsspeicher zum ersten Mal geöffnet wird oder wenn ein Speicher als Standardspeicher erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8e40d-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="8e40d-148">Diese Funktion kann auch von Clientanwendungen verwendet werden, um Standardnachrichten Ordner zu überprüfen oder zu reparieren.</span><span class="sxs-lookup"><span data-stu-id="8e40d-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="8e40d-149">**HrValidateIPMSubtree** erstellt immer die Ordner Search root und IPM Subtree im Stammordner des Stores und im Ordner "Gelöschte Elemente" im Ordner "IPM subtree".</span><span class="sxs-lookup"><span data-stu-id="8e40d-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="8e40d-150">Der IPM-subtree-Ordner ist der Stamm der IPM-Hierarchie in diesem Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="8e40d-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="8e40d-151">Der Stammordner der Suche kann als Stamm einer Unterstruktur für Suchergebnisordner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e40d-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="8e40d-152">IPM-Clients sollten ihre Ordneransicht beginnend beim Stammordner der IPM-Unterstruktur anzeigen und die darunter liegenden Ordner anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8e40d-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="8e40d-153">Informationen im Stammordner eines Nachrichtenspeichers sollten nicht auf der Benutzeroberfläche eines Clients angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8e40d-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="8e40d-154">Diese Funktion bedeutet, dass, wenn ein Clientinformationen ausblenden muss, die Informationen im Stammverzeichnis der IPM-Unterstruktur abgelegt werden können, wo es für den Benutzer nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="8e40d-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="8e40d-155">Im Gegensatz dazu können nicht-IPM-Anwendungen, die Nachrichten und Ordner für den Benutzer unsichtbar sein müssen, beispielsweise in einem Server basierten Nachrichtenspeicher, außerhalb der IPM-Hierarchie platziert werden.</span><span class="sxs-lookup"><span data-stu-id="8e40d-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="8e40d-156">**HrValidateIPMSubtree** legt die **PR_VALID_FOLDER_MASK** -Eigenschaft fest, um anzugeben, ob jeder erstellte IPM-Ordner eine gültige Eintrags-ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="8e40d-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="8e40d-157">Die folgenden Eigenschaften des Eintrags Identifiers des Nachrichtenspeichers werden auf die Eintragsbezeichner der entsprechenden Ordner festgelegt und im _lppProps_ -Parameter zusammen mit **PR_VALID_FOLDER_MASK**zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="8e40d-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="8e40d-158">**PR_COMMON_VIEWS_ENTRYID** ([Pidtagcommonviewsentryid (](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e40d-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="8e40d-159">**PR_FINDER_ENTRYID** ([Pidtagfinderentryid (](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e40d-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="8e40d-160">**PR_IPM_OUTBOX_ENTRYID** ([Pidtagipmoutboxentryid (](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e40d-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="8e40d-161">**PR_IPM_SENTMAIL_ENTRYID** ([Pidtagipmsentmailentryid (](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e40d-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="8e40d-162">**PR_IPM_SUBTREE_ENTRYID** ([Pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e40d-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="8e40d-163">**PR_IPM_WASTEBASKET_ENTRYID** ([Pidtagipmwastebasketentryid (](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e40d-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="8e40d-164">**PR_VIEWS_ENTRYID** ([Pidtagviewsentryid (](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8e40d-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="8e40d-165">Ein Platzhalter- [PROP_TAG](prop_tag.md) für den IPM-Posteingang (PT_BINARY, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="8e40d-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="8e40d-166">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="8e40d-166">MFCMAPI reference</span></span>

<span data-ttu-id="8e40d-167">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8e40d-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8e40d-168">**Datei**</span><span class="sxs-lookup"><span data-stu-id="8e40d-168">**File**</span></span>|<span data-ttu-id="8e40d-169">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="8e40d-169">**Function**</span></span>|<span data-ttu-id="8e40d-170">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8e40d-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8e40d-171">MstStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="8e40d-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="8e40d-172">CMsgStoreDlg:: OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="8e40d-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="8e40d-173">MFCMAPI verwendet die **HrValidateIPMSubtree** -Methode, um einem Nachrichtenspeicher Standardordner hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8e40d-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e40d-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e40d-174">See also</span></span>



[<span data-ttu-id="8e40d-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="8e40d-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="8e40d-176">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="8e40d-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

