---
title: PidTagStoreEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreEntryId
api_type:
- COM
ms.assetid: 0d705667-19f4-4eda-a068-e65ea8f00d9b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7dc8ea74d36dd8aee4acec426e97d8b5e3ba2234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278750"
---
# <a name="pidtagstoreentryid-canonical-property"></a><span data-ttu-id="201c6-103">PidTagStoreEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="201c6-103">PidTagStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="201c6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="201c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="201c6-105">Enthält den eindeutigen Eintragsbezeichner des Nachrichtenspeichers, in dem sich ein Objekt befindet.</span><span class="sxs-lookup"><span data-stu-id="201c6-105">Contains the unique entry identifier of the message store where an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="201c6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="201c6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="201c6-107">PR_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="201c6-107">PR_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="201c6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="201c6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="201c6-109">0x0FFB</span><span class="sxs-lookup"><span data-stu-id="201c6-109">0x0FFB</span></span>  <br/> |
|<span data-ttu-id="201c6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="201c6-110">Data type:</span></span>  <br/> |<span data-ttu-id="201c6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="201c6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="201c6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="201c6-112">Area:</span></span>  <br/> |<span data-ttu-id="201c6-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="201c6-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="201c6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="201c6-114">Remarks</span></span>

<span data-ttu-id="201c6-115">Diese Eigenschaft wird verwendet, um einen Nachrichtenspeicher mit der [IMAPISession::OpenMsgStore-Methode zu](imapisession-openmsgstore.md) öffnen.</span><span class="sxs-lookup"><span data-stu-id="201c6-115">This property is used to open a message store with the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="201c6-116">Es wird auch verwendet, um alle Objekte zu öffnen, die im Besitz des Nachrichtenspeichers sind.</span><span class="sxs-lookup"><span data-stu-id="201c6-116">It is also used to open any object that is owned by the message store.</span></span> 
  
<span data-ttu-id="201c6-117">Bei einem Nachrichtenspeicher ist diese Eigenschaft mit der eigenen PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)) identisch.</span><span class="sxs-lookup"><span data-stu-id="201c6-117">For a message store, this property is identical to the store's own **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="201c6-118">Eine Clientanwendung kann die beiden Eigenschaften mithilfe der [IMAPISession::CompareEntryIDs-Methode](imapisession-compareentryids.md) vergleichen.</span><span class="sxs-lookup"><span data-stu-id="201c6-118">A client application can compare the two properties using the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="201c6-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="201c6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="201c6-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="201c6-120">Protocol specifications</span></span>

<span data-ttu-id="201c6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="201c6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="201c6-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="201c6-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="201c6-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="201c6-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="201c6-124">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="201c6-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="201c6-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="201c6-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="201c6-126">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="201c6-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="201c6-127">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="201c6-127">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="201c6-128">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="201c6-128">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="201c6-129">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="201c6-129">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="201c6-130">Gibt Postfachordner zwischen Clients zurück.</span><span class="sxs-lookup"><span data-stu-id="201c6-130">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="201c6-131">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="201c6-131">Header files</span></span>

<span data-ttu-id="201c6-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="201c6-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="201c6-133">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="201c6-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="201c6-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="201c6-134">Mapitags.h</span></span>
  
> <span data-ttu-id="201c6-135">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="201c6-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="201c6-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="201c6-136">See also</span></span>



[<span data-ttu-id="201c6-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="201c6-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="201c6-138">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="201c6-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="201c6-139">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="201c6-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="201c6-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="201c6-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

