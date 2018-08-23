---
title: PidTagStoreState (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreState
api_type:
- COM
ms.assetid: 36e49cf5-1411-42c5-9112-09958243996d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7348d0395952036ee6b356b013072324b64e4b98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570821"
---
# <a name="pidtagstorestate-canonical-property"></a><span data-ttu-id="e1ea4-103">PidTagStoreState (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e1ea4-103">PidTagStoreState Canonical Property</span></span>

  
  
<span data-ttu-id="e1ea4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1ea4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1ea4-105">Enthält ein Flag, das den Zustand des Nachrichtenspeichers beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e1ea4-105">Contains a flag that describes the state of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1ea4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e1ea4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1ea4-107">PR_STORE_STATE</span><span class="sxs-lookup"><span data-stu-id="e1ea4-107">PR_STORE_STATE</span></span>  <br/> |
|<span data-ttu-id="e1ea4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e1ea4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1ea4-109">0x340E</span><span class="sxs-lookup"><span data-stu-id="e1ea4-109">0x340E</span></span>  <br/> |
|<span data-ttu-id="e1ea4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e1ea4-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1ea4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e1ea4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e1ea4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e1ea4-112">Area:</span></span>  <br/> |<span data-ttu-id="e1ea4-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="e1ea4-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1ea4-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="e1ea4-114">Remarks</span></span>

<span data-ttu-id="e1ea4-115">Diese Eigenschaft ist dynamisch und kann basierend auf Benutzeraktionen, im Gegensatz zu der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft ändern.</span><span class="sxs-lookup"><span data-stu-id="e1ea4-115">This property is dynamic and can change based on user actions, unlike the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="e1ea4-116">Der folgende Wert kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e1ea4-116">The following value can be set:</span></span>
  
<span data-ttu-id="e1ea4-117">STORE_HAS_SEARCHES</span><span class="sxs-lookup"><span data-stu-id="e1ea4-117">STORE_HAS_SEARCHES</span></span> 
  
> <span data-ttu-id="e1ea4-118">Der Benutzer hat einen oder mehrere aktive Suchvorgänge im Speicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1ea4-118">The user has created one or more active searches in the store.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="e1ea4-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e1ea4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1ea4-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e1ea4-120">Protocol specifications</span></span>

<span data-ttu-id="e1ea4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1ea4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1ea4-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e1ea4-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1ea4-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1ea4-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1ea4-124">Gibt die zulässige Vorgänge für die Hauptobjekte der Nachricht Store.</span><span class="sxs-lookup"><span data-stu-id="e1ea4-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1ea4-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e1ea4-125">Header files</span></span>

<span data-ttu-id="e1ea4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1ea4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1ea4-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e1ea4-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1ea4-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e1ea4-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e1ea4-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e1ea4-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1ea4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1ea4-130">See also</span></span>



[<span data-ttu-id="e1ea4-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1ea4-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1ea4-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1ea4-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1ea4-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e1ea4-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1ea4-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e1ea4-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

