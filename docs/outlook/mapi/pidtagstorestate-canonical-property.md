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
ms.openlocfilehash: 8f00addf7abdd765d97c54350e46979f788f06ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341153"
---
# <a name="pidtagstorestate-canonical-property"></a><span data-ttu-id="ecc7b-103">PidTagStoreState (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ecc7b-103">PidTagStoreState Canonical Property</span></span>

  
  
<span data-ttu-id="ecc7b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecc7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecc7b-105">Enthält ein Flag, das den Status des Nachrichtenspeichers beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ecc7b-105">Contains a flag that describes the state of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ecc7b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ecc7b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ecc7b-107">PR_STORE_STATE</span><span class="sxs-lookup"><span data-stu-id="ecc7b-107">PR_STORE_STATE</span></span>  <br/> |
|<span data-ttu-id="ecc7b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ecc7b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ecc7b-109">0x340E</span><span class="sxs-lookup"><span data-stu-id="ecc7b-109">0x340E</span></span>  <br/> |
|<span data-ttu-id="ecc7b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ecc7b-110">Data type:</span></span>  <br/> |<span data-ttu-id="ecc7b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ecc7b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ecc7b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ecc7b-112">Area:</span></span>  <br/> |<span data-ttu-id="ecc7b-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="ecc7b-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecc7b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ecc7b-114">Remarks</span></span>

<span data-ttu-id="ecc7b-115">Diese Eigenschaft ist dynamisch und kann sich basierend auf Benutzeraktionen ändern, im Gegensatz zur **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ecc7b-115">This property is dynamic and can change based on user actions, unlike the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="ecc7b-116">Der folgende Wert kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ecc7b-116">The following value can be set:</span></span>
  
<span data-ttu-id="ecc7b-117">STORE_HAS_SEARCHES</span><span class="sxs-lookup"><span data-stu-id="ecc7b-117">STORE_HAS_SEARCHES</span></span> 
  
> <span data-ttu-id="ecc7b-118">Der Benutzer hat mindestens eine aktive Suche im Store erstellt.</span><span class="sxs-lookup"><span data-stu-id="ecc7b-118">The user has created one or more active searches in the store.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="ecc7b-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ecc7b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ecc7b-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ecc7b-120">Protocol specifications</span></span>

<span data-ttu-id="ecc7b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecc7b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecc7b-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ecc7b-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ecc7b-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecc7b-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecc7b-124">Gibt zulässige Vorgänge für die Zentralen Nachrichtenspeicherobjekte an.</span><span class="sxs-lookup"><span data-stu-id="ecc7b-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ecc7b-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ecc7b-125">Header files</span></span>

<span data-ttu-id="ecc7b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecc7b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ecc7b-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ecc7b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="ecc7b-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ecc7b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="ecc7b-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ecc7b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecc7b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecc7b-130">See also</span></span>



[<span data-ttu-id="ecc7b-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ecc7b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ecc7b-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ecc7b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ecc7b-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ecc7b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ecc7b-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ecc7b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

