---
title: Kanonische Pidtagserviceuid (-Eigenschaft
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
ms.openlocfilehash: d5c6e1dc30c3ee7862341bce204b4a78bd6d379b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426527"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="bff52-103">Kanonische Pidtagserviceuid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bff52-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="bff52-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bff52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bff52-105">Enthält die [MAPIUID](mapiuid.md) -Struktur für einen Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="bff52-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bff52-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bff52-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bff52-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="bff52-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="bff52-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bff52-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bff52-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="bff52-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="bff52-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bff52-110">Data type:</span></span>  <br/> |<span data-ttu-id="bff52-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bff52-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bff52-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bff52-112">Area:</span></span>  <br/> |<span data-ttu-id="bff52-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="bff52-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bff52-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bff52-114">Remarks</span></span>

<span data-ttu-id="bff52-115">Diese Eigenschaft wird von MAPI für Profile Section-Objekte berechnet.</span><span class="sxs-lookup"><span data-stu-id="bff52-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="bff52-116">MAPI verwendet es, um alle Anbieter zu gruppieren, die zum gleichen Nachrichtendienst gehören.</span><span class="sxs-lookup"><span data-stu-id="bff52-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="bff52-117">Diese Eigenschaft wird als Parameter für die meisten [IMsgServiceAdmin](imsgserviceadminiunknown.md) -Methoden bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="bff52-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="bff52-118">Sie darf nicht in MAPISVC. inf angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bff52-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bff52-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bff52-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bff52-120">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="bff52-120">Header files</span></span>

<span data-ttu-id="bff52-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bff52-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="bff52-122">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="bff52-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="bff52-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bff52-123">Mapitags.h</span></span>
  
> <span data-ttu-id="bff52-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bff52-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bff52-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bff52-125">See also</span></span>



[<span data-ttu-id="bff52-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bff52-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="bff52-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bff52-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bff52-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bff52-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bff52-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bff52-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bff52-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bff52-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

