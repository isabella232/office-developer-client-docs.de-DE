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
ms.openlocfilehash: 8b6d4fa1d9ffa6ab5f800bad9f02ac5aa9abd8c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791942"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="26f07-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="26f07-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="26f07-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26f07-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26f07-105">Einen Nachrichtenspeicher hinzugefügt standard zwischen Personen (IPM) Nachrichtenordner.</span><span class="sxs-lookup"><span data-stu-id="26f07-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26f07-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="26f07-106">Header file:</span></span>  <br/> |<span data-ttu-id="26f07-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="26f07-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="26f07-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="26f07-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="26f07-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="26f07-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="26f07-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="26f07-110">Called by:</span></span>  <br/> |<span data-ttu-id="26f07-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="26f07-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="26f07-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="26f07-112">Parameters</span></span>

 <span data-ttu-id="26f07-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="26f07-113">_lpMDB_</span></span>
  
> <span data-ttu-id="26f07-114">[in] Zeiger auf die Nachricht speichern-Objekt, dem der Ordner hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="26f07-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="26f07-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="26f07-115">_ulFlags_</span></span>
  
> <span data-ttu-id="26f07-116">[in] Bitmaske aus Flags verwendet, um zu steuern, wie die Ordner erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="26f07-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="26f07-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="26f07-117">The following flags can be set:</span></span>
    
<span data-ttu-id="26f07-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="26f07-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="26f07-119">Die Ordner sollte vor dem Erstellen der, überprüft werden, selbst wenn die Eigenschaften des Nachrichtenspeichers Geben Sie an, dass sie gültig sind.</span><span class="sxs-lookup"><span data-stu-id="26f07-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="26f07-120">Eine Clientanwendung wird dieses Flag in der Regel, wenn ein Fehler weist darauf hin, dass die Struktur eines vorhandenen Ordners beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="26f07-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="26f07-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="26f07-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="26f07-122">Der vollständige Satz IPM Ordner sollte im Stammordner der Nachrichtenspeicher erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="26f07-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="26f07-123">Der Ordner Titel in der Hierarchie sind:</span><span class="sxs-lookup"><span data-stu-id="26f07-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="26f07-124">Ordneransichten</span><span class="sxs-lookup"><span data-stu-id="26f07-124">Folder Views</span></span>
    
    - <span data-ttu-id="26f07-125">Allgemeine Ansichten</span><span class="sxs-lookup"><span data-stu-id="26f07-125">Common Views</span></span>
    
    - <span data-ttu-id="26f07-126">Stamm der Suche\*</span><span class="sxs-lookup"><span data-stu-id="26f07-126">Search Root\*</span></span>
    
    - <span data-ttu-id="26f07-127">IPM-Teilstruktur\*</span><span class="sxs-lookup"><span data-stu-id="26f07-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="26f07-128">Posteingang</span><span class="sxs-lookup"><span data-stu-id="26f07-128">Inbox</span></span>
    
    - <span data-ttu-id="26f07-129">Postausgang</span><span class="sxs-lookup"><span data-stu-id="26f07-129">Outbox</span></span>
    
    - <span data-ttu-id="26f07-130">Gelöschte Elemente\*</span><span class="sxs-lookup"><span data-stu-id="26f07-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="26f07-131">Gesendete Elemente</span><span class="sxs-lookup"><span data-stu-id="26f07-131">Sent Items</span></span>
    
    <span data-ttu-id="26f07-132">die drei Ordner, in dem mit markiert \* werden den Mindestsatz erstellt, auch wenn das Flag MAPI_FULL_IPM_TREE nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="26f07-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="26f07-133">Eine Clientanwendung wird dieses Flag in der Regel, wenn der Nachrichtenspeicher, in dem der Ordner sind zu erstellenden, des Standard-Informationsspeichers ist.</span><span class="sxs-lookup"><span data-stu-id="26f07-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="26f07-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="26f07-134">_lpcValues_</span></span>
  
> <span data-ttu-id="26f07-135">[in, out] Zeiger auf die Anzahl der [SPropValue](spropvalue.md) Strukturen in das im Parameter _LppProps_ zurückgegebene Array.</span><span class="sxs-lookup"><span data-stu-id="26f07-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="26f07-136">Der Wert des Parameters _LpcValues_ kann 0 (null) sein, wenn _LppProps_ NULL ist.</span><span class="sxs-lookup"><span data-stu-id="26f07-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="26f07-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="26f07-137">_lppProps_</span></span>
  
> <span data-ttu-id="26f07-138">[in, out] Zeiger auf einen Zeiger auf ein Array von **SPropValue** -Strukturen, Eigenschaftswerte für die Eigenschaft **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) und für die entsprechenden Ordner Eintrags-ID-Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="26f07-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="26f07-139">Wenn **HrValidateIPMSubtree** einen Posteingang im Nachrichtenspeicher erstellt, enthält das Array **SPropValue** ein Posteingang Eintrags-ID mit einem speziellen Eigenschaftentag als codierte `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span><span class="sxs-lookup"><span data-stu-id="26f07-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="26f07-140">Der Parameter _LppProps_ möglicherweise NULL-Wert zurück, der angibt, dass die aufrufende Implementierung nicht erfordert, dass ein **SPropValue** Array zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="26f07-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="26f07-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="26f07-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="26f07-142">[out] Zeiger auf einen Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur, die Angaben zu Version, Komponente und Kontext für einen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="26f07-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="26f07-143">Der Parameter _LppMAPIError_ ist auf NULL festgelegt, wenn keine **MAPIERROR** -Struktur zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="26f07-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="26f07-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26f07-144">Return value</span></span>

<span data-ttu-id="26f07-145">None.</span><span class="sxs-lookup"><span data-stu-id="26f07-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26f07-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26f07-146">Remarks</span></span>

<span data-ttu-id="26f07-147">MAPI verwendet die Funktion **HrValidateIPMSubtree** intern standard IPM-Unterstruktur in einem Nachrichtenspeicher erstellt wird, wenn der Informationsspeicher zum ersten Mal geöffnet wird, oder ein Speichers Standard speichern vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="26f07-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="26f07-148">Diese Funktion kann auch verwendet werden von Clientanwendungen überprüfen oder Reparatur von e-Mail-Ordnern.</span><span class="sxs-lookup"><span data-stu-id="26f07-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="26f07-149">**HrValidateIPMSubtree** wird immer die Suche Domänenstamm und in IPM-Unterstruktur Ordner im Stammordner des Speichers und der Ordner Gelöschte Elemente im Ordner "IPM-Unterstruktur" erstellt.</span><span class="sxs-lookup"><span data-stu-id="26f07-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="26f07-150">Der Ordner IPM-Unterstruktur ist der Stamm der Hierarchie IPM in dieser Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="26f07-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="26f07-151">Suche Stammordner kann als Basis für eine Unterstruktur für Suchergebnisse Ordner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26f07-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="26f07-152">IPM Clients sollte ihre Ordneransicht beginnend am IPM Unterstruktur Stammordner und Anzeigen von untergeordneten Ordner darunter angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="26f07-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="26f07-153">Informationen in den Stammordner eines Nachrichtenspeichers sollte nicht in einem Client-Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="26f07-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="26f07-154">Dies bedeutet, dass wenn ein Client Informationen ausblenden muss, die Informationen in das Stammverzeichnis IPM Unterstruktur versetzt werden kann, ist es nicht für den Benutzer sichtbar.</span><span class="sxs-lookup"><span data-stu-id="26f07-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="26f07-155">Im Gegensatz dazu können sie nicht-IPM-Anwendungen, die Nachrichten und Ordnern für den Benutzer, beispielsweise in einem serverbasierten Nachrichtenspeicher, unsichtbar werden müssen, außerhalb der Hierarchie IPM platzieren.</span><span class="sxs-lookup"><span data-stu-id="26f07-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="26f07-156">**HrValidateIPMSubtree** wird die **PR_VALID_FOLDER_MASK** -Eigenschaft, um anzugeben, ob jeder IPM-Ordner erstellt werden, eine gültige Eingabe-ID hat.</span><span class="sxs-lookup"><span data-stu-id="26f07-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="26f07-157">Die folgenden Eigenschaften des Nachrichtenspeichers Eintrag sind der entsprechenden Ordner auf den Eintrag festgelegt und im Parameter _LppProps_ zusammen mit **PR_VALID_FOLDER_MASK**zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="26f07-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="26f07-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="26f07-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="26f07-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="26f07-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="26f07-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="26f07-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="26f07-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="26f07-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="26f07-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="26f07-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="26f07-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="26f07-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="26f07-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="26f07-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="26f07-165">Ein Platzhalter [PROP_TAG](prop_tag.md) für den Posteingang IPM (PT_BINARY, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="26f07-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="26f07-166">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="26f07-166">MFCMAPI reference</span></span>

<span data-ttu-id="26f07-167">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="26f07-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="26f07-168">**Datei**</span><span class="sxs-lookup"><span data-stu-id="26f07-168">**File**</span></span>|<span data-ttu-id="26f07-169">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="26f07-169">**Function**</span></span>|<span data-ttu-id="26f07-170">**Comment**</span><span class="sxs-lookup"><span data-stu-id="26f07-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="26f07-171">MstStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="26f07-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="26f07-172">CMsgStoreDlg::OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="26f07-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="26f07-173">MFCMAPI (engl.) verwendet die **HrValidateIPMSubtree** -Methode, um einen Nachrichtenspeicher standard Ordner hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="26f07-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26f07-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26f07-174">See also</span></span>



[<span data-ttu-id="26f07-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="26f07-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="26f07-176">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="26f07-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

