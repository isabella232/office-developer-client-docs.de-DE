---
title: Kanonische Pidtagipmsubtreeentryid (-Eigenschaft
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
ms.openlocfilehash: 815685696dfc93bb6241f608ca0157e87e758e7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412730"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="08f54-103">Kanonische Pidtagipmsubtreeentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="08f54-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="08f54-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08f54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08f54-105">Enthält die Eintrags-ID des Stamms der Unterstruktur des Ordners "zwischenmenschlichen Nachrichten" (IPM) in der Ordnerstruktur des Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="08f54-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08f54-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="08f54-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08f54-107">PR_IPM_SUBTREE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="08f54-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="08f54-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="08f54-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08f54-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="08f54-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="08f54-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="08f54-110">Data type:</span></span>  <br/> |<span data-ttu-id="08f54-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="08f54-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="08f54-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="08f54-112">Area:</span></span>  <br/> |<span data-ttu-id="08f54-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="08f54-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08f54-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08f54-114">Remarks</span></span>

<span data-ttu-id="08f54-115">Diese Eigenschaft stellt den Stamm der IPM-Hierarchie dar.</span><span class="sxs-lookup"><span data-stu-id="08f54-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="08f54-116">IPM-Clients sollten keine Ordner anzeigen, die keine Unterordner des durch diese Eigenschaft dargestellten Ordners sind.</span><span class="sxs-lookup"><span data-stu-id="08f54-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="08f54-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="08f54-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="08f54-118">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="08f54-118">Header files</span></span>

<span data-ttu-id="08f54-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="08f54-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="08f54-120">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="08f54-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="08f54-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="08f54-121">Mapitags.h</span></span>
  
> <span data-ttu-id="08f54-122">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="08f54-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08f54-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08f54-123">See also</span></span>



[<span data-ttu-id="08f54-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08f54-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08f54-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08f54-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08f54-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="08f54-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08f54-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="08f54-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

