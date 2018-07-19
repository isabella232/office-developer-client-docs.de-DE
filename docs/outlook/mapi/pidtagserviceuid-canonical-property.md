---
title: PidTagServiceUid (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 304efc3f4ea903f9ed0e9fcf95c7100fa6ebfc95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795176"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="a9018-103">PidTagServiceUid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a9018-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="a9018-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a9018-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a9018-105">Enthält die [MAPIUID](mapiuid.md) -Struktur für einen Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="a9018-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9018-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a9018-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9018-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="a9018-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="a9018-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="a9018-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a9018-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="a9018-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="a9018-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a9018-110">Data type:</span></span>  <br/> |<span data-ttu-id="a9018-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9018-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a9018-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a9018-112">Area:</span></span>  <br/> |<span data-ttu-id="a9018-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="a9018-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9018-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9018-114">Remarks</span></span>

<span data-ttu-id="a9018-115">Diese Eigenschaft wird von MAPI auf Profil Section-Objekten berechnet.</span><span class="sxs-lookup"><span data-stu-id="a9018-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="a9018-116">MAPI wird verwendet, um alle Anbieter zu gruppieren, die den Dienst angehören.</span><span class="sxs-lookup"><span data-stu-id="a9018-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="a9018-117">Diese Eigenschaft wird als Parameter für die meisten [IMsgServiceAdmin](imsgserviceadminiunknown.md) Methoden bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a9018-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="a9018-118">Sie müssen nicht Mapisvc.inf angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a9018-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a9018-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a9018-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a9018-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a9018-120">Header files</span></span>

<span data-ttu-id="a9018-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9018-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9018-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a9018-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a9018-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a9018-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a9018-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a9018-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9018-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9018-125">See also</span></span>



[<span data-ttu-id="a9018-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9018-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="a9018-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9018-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9018-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9018-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9018-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a9018-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9018-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a9018-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

