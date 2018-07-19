---
title: PidTagServiceExtraUids (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 71f802014200d4b767c346c14df53f1193d44b0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795160"
---
# <a name="pidtagserviceextrauids-canonical-property"></a><span data-ttu-id="27185-103">PidTagServiceExtraUids (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="27185-103">PidTagServiceExtraUids Canonical Property</span></span>

  
  
<span data-ttu-id="27185-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27185-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27185-105">Enthält eine Liste von [MAPIUID](mapiuid.md) -Strukturen, die zusätzliche Profil Abschnitte für den Dienst zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="27185-105">Contains a list of [MAPIUID](mapiuid.md) structures that identify additional profile sections for the message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27185-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="27185-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27185-107">PR_SERVICE_EXTRA_UIDS</span><span class="sxs-lookup"><span data-stu-id="27185-107">PR_SERVICE_EXTRA_UIDS</span></span>  <br/> |
|<span data-ttu-id="27185-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="27185-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27185-109">0x3D0D</span><span class="sxs-lookup"><span data-stu-id="27185-109">0x3D0D</span></span>  <br/> |
|<span data-ttu-id="27185-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="27185-110">Data type:</span></span>  <br/> |<span data-ttu-id="27185-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="27185-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="27185-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="27185-112">Area:</span></span>  <br/> |<span data-ttu-id="27185-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="27185-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27185-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27185-114">Remarks</span></span>

<span data-ttu-id="27185-115">Neue Profil Abschnitte können für jede Nachrichtenfilter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="27185-115">New profile sections can be created for each message filter.</span></span> <span data-ttu-id="27185-116">Wenn die Informationen über den Dienst ist in einem anderen Profil kopiert werden, ist es wichtig, die zusätzliche Profil Abschnitte für die Filter sowie kopieren.</span><span class="sxs-lookup"><span data-stu-id="27185-116">When the information about the message service is to be copied to another profile, it is important to copy the additional profile sections for the filters as well.</span></span> <span data-ttu-id="27185-117">Ein Dienstanbieter, der zusätzliche Profil Abschnitten verwendet kann die **MAPIUID** Strukturen Abschnitten Profil in **PR_SERVICE_EXTRA_UIDS**, speichern, die MAPI zum Kopieren von Informationen für den Dienst zusätzliche Nachricht ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="27185-117">A service provider that uses additional profile sections can store the **MAPIUID** structures of those profile sections in **PR_SERVICE_EXTRA_UIDS**, which allows MAPI to copy the additional message service information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27185-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="27185-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="27185-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="27185-119">Header files</span></span>

<span data-ttu-id="27185-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27185-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="27185-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="27185-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="27185-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="27185-122">Mapitags.h</span></span>
  
> <span data-ttu-id="27185-123">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="27185-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27185-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27185-124">See also</span></span>



[<span data-ttu-id="27185-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27185-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27185-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27185-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27185-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="27185-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27185-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="27185-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

