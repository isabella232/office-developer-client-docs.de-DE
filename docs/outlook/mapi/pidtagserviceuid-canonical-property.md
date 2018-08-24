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
ms.openlocfilehash: eabcaaf1db6149ef200e640f5af152758261581b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582252"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="70c7c-103">PidTagServiceUid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="70c7c-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="70c7c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70c7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70c7c-105">Enthält die [MAPIUID](mapiuid.md) -Struktur für einen Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="70c7c-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70c7c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="70c7c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70c7c-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="70c7c-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="70c7c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="70c7c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="70c7c-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="70c7c-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="70c7c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="70c7c-110">Data type:</span></span>  <br/> |<span data-ttu-id="70c7c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="70c7c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="70c7c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="70c7c-112">Area:</span></span>  <br/> |<span data-ttu-id="70c7c-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="70c7c-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70c7c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70c7c-114">Remarks</span></span>

<span data-ttu-id="70c7c-115">Diese Eigenschaft wird von MAPI auf Profil Section-Objekten berechnet.</span><span class="sxs-lookup"><span data-stu-id="70c7c-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="70c7c-116">MAPI wird verwendet, um alle Anbieter zu gruppieren, die den Dienst angehören.</span><span class="sxs-lookup"><span data-stu-id="70c7c-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="70c7c-117">Diese Eigenschaft wird als Parameter für die meisten [IMsgServiceAdmin](imsgserviceadminiunknown.md) Methoden bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="70c7c-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="70c7c-118">Sie müssen nicht Mapisvc.inf angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70c7c-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="70c7c-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="70c7c-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="70c7c-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="70c7c-120">Header files</span></span>

<span data-ttu-id="70c7c-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70c7c-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="70c7c-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="70c7c-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="70c7c-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="70c7c-123">Mapitags.h</span></span>
  
> <span data-ttu-id="70c7c-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="70c7c-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70c7c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70c7c-125">See also</span></span>



[<span data-ttu-id="70c7c-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="70c7c-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="70c7c-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="70c7c-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70c7c-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="70c7c-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70c7c-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="70c7c-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70c7c-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="70c7c-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

