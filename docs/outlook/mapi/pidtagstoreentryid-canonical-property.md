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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392949"
---
# <a name="pidtagstoreentryid-canonical-property"></a><span data-ttu-id="5528f-103">PidTagStoreEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5528f-103">PidTagStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5528f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5528f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5528f-105">Enthält die eindeutige Eintrags-ID des Nachrichtenspeichers an, in dem ein Objekt befindet.</span><span class="sxs-lookup"><span data-stu-id="5528f-105">Contains the unique entry identifier of the message store where an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5528f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5528f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5528f-107">PR_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5528f-107">PR_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5528f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5528f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5528f-109">0x0FFB</span><span class="sxs-lookup"><span data-stu-id="5528f-109">0x0FFB</span></span>  <br/> |
|<span data-ttu-id="5528f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5528f-110">Data type:</span></span>  <br/> |<span data-ttu-id="5528f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5528f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5528f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5528f-112">Area:</span></span>  <br/> |<span data-ttu-id="5528f-113">ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5528f-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5528f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5528f-114">Remarks</span></span>

<span data-ttu-id="5528f-115">Diese Eigenschaft wird verwendet, um einen Nachrichtenspeicher mit der [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) -Methode zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5528f-115">This property is used to open a message store with the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="5528f-116">Es wird auch ein beliebiges Objekt öffnen, die gehört verwendet, durch die Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="5528f-116">It is also used to open any object that is owned by the message store.</span></span> 
  
<span data-ttu-id="5528f-117">Für einen Nachrichtenspeicher ist diese Eigenschaft mit der des Speichers **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft identisch.</span><span class="sxs-lookup"><span data-stu-id="5528f-117">For a message store, this property is identical to the store's own **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="5528f-118">Eine Clientanwendung kann die beiden Eigenschaften mithilfe der Methode [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) vergleichen.</span><span class="sxs-lookup"><span data-stu-id="5528f-118">A client application can compare the two properties using the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5528f-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5528f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5528f-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5528f-120">Protocol specifications</span></span>

<span data-ttu-id="5528f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5528f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5528f-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5528f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5528f-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5528f-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5528f-124">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="5528f-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="5528f-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5528f-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5528f-126">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="5528f-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="5528f-127">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5528f-127">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5528f-128">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="5528f-128">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="5528f-129">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5528f-129">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5528f-130">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="5528f-130">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5528f-131">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5528f-131">Header files</span></span>

<span data-ttu-id="5528f-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5528f-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="5528f-133">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5528f-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="5528f-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5528f-134">Mapitags.h</span></span>
  
> <span data-ttu-id="5528f-135">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5528f-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5528f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5528f-136">See also</span></span>



[<span data-ttu-id="5528f-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5528f-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5528f-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5528f-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5528f-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5528f-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5528f-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5528f-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

