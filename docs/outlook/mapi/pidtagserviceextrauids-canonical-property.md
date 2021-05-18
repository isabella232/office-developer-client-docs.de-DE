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
ms.openlocfilehash: 0fb688e2a845186224c1802f9df2ac537d5bb4d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422306"
---
# <a name="pidtagserviceextrauids-canonical-property"></a><span data-ttu-id="1defe-103">PidTagServiceExtraUids (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1defe-103">PidTagServiceExtraUids Canonical Property</span></span>

  
  
<span data-ttu-id="1defe-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1defe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1defe-105">Enthält eine Liste der [MAPIUID-Strukturen,](mapiuid.md) die zusätzliche Profilabschnitte für den Nachrichtendienst identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1defe-105">Contains a list of [MAPIUID](mapiuid.md) structures that identify additional profile sections for the message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1defe-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1defe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1defe-107">PR_SERVICE_EXTRA_UIDS</span><span class="sxs-lookup"><span data-stu-id="1defe-107">PR_SERVICE_EXTRA_UIDS</span></span>  <br/> |
|<span data-ttu-id="1defe-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1defe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1defe-109">0x3D0D</span><span class="sxs-lookup"><span data-stu-id="1defe-109">0x3D0D</span></span>  <br/> |
|<span data-ttu-id="1defe-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1defe-110">Data type:</span></span>  <br/> |<span data-ttu-id="1defe-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1defe-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1defe-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1defe-112">Area:</span></span>  <br/> |<span data-ttu-id="1defe-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="1defe-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1defe-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1defe-114">Remarks</span></span>

<span data-ttu-id="1defe-115">Neue Profilabschnitte können für jeden Nachrichtenfilter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1defe-115">New profile sections can be created for each message filter.</span></span> <span data-ttu-id="1defe-116">Wenn die Informationen zum Nachrichtendienst in ein anderes Profil kopiert werden sollen, ist es wichtig, auch die zusätzlichen Profilabschnitte für die Filter zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="1defe-116">When the information about the message service is to be copied to another profile, it is important to copy the additional profile sections for the filters as well.</span></span> <span data-ttu-id="1defe-117">Ein Dienstanbieter, der zusätzliche Profilabschnitte verwendet, kann die **MAPIUID-Strukturen** dieser Profilabschnitte in **PR_SERVICE_EXTRA_UIDS** speichern, wodurch MAPI die zusätzlichen Nachrichtendienstinformationen kopieren kann.</span><span class="sxs-lookup"><span data-stu-id="1defe-117">A service provider that uses additional profile sections can store the **MAPIUID** structures of those profile sections in **PR_SERVICE_EXTRA_UIDS**, which allows MAPI to copy the additional message service information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1defe-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1defe-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1defe-119">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="1defe-119">Header files</span></span>

<span data-ttu-id="1defe-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1defe-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="1defe-121">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1defe-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="1defe-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1defe-122">Mapitags.h</span></span>
  
> <span data-ttu-id="1defe-123">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1defe-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1defe-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1defe-124">See also</span></span>



[<span data-ttu-id="1defe-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1defe-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1defe-126">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="1defe-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1defe-127">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1defe-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1defe-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1defe-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

