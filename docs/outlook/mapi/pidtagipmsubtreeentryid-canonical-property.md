---
title: PidTagIpmSubtreeEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9635c06ffa5638e370312e3b2b29e0c98161a766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794520"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="4c959-103">PidTagIpmSubtreeEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4c959-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="4c959-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4c959-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4c959-105">Enthält die Eintrags-ID der Stamm des untergeordneten Ordner zwischen Personen Nachricht (IPM) in der Nachrichtenspeicher Ordnerstruktur.</span><span class="sxs-lookup"><span data-stu-id="4c959-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c959-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4c959-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c959-107">PR_IPM_SUBTREE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4c959-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="4c959-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="4c959-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c959-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="4c959-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="4c959-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4c959-110">Data type:</span></span>  <br/> |<span data-ttu-id="4c959-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4c959-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4c959-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4c959-112">Area:</span></span>  <br/> |<span data-ttu-id="4c959-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="4c959-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c959-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c959-114">Remarks</span></span>

<span data-ttu-id="4c959-115">Diese Eigenschaft stellt den Stamm der Hierarchie IPM.</span><span class="sxs-lookup"><span data-stu-id="4c959-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="4c959-116">IPM Clients keine Ordner angezeigt werden sollen, die nicht Unterordner des durch diese Eigenschaft dargestellt wird sind.</span><span class="sxs-lookup"><span data-stu-id="4c959-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4c959-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4c959-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4c959-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4c959-118">Header files</span></span>

<span data-ttu-id="4c959-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c959-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c959-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4c959-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c959-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4c959-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4c959-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4c959-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c959-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c959-123">See also</span></span>



[<span data-ttu-id="4c959-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4c959-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c959-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4c959-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c959-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4c959-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c959-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4c959-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

