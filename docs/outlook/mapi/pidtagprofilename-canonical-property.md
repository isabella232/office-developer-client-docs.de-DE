---
title: Kanonische PidTagProfileName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 992b3a6a30e15d267ffeda11ec98c7b4aeacb2c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435649"
---
# <a name="pidtagprofilename-canonical-property"></a><span data-ttu-id="c48f4-103">Kanonische PidTagProfileName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c48f4-103">PidTagProfileName Canonical Property</span></span>

  
  
<span data-ttu-id="c48f4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c48f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c48f4-105">Enthält den Namen des Profils.</span><span class="sxs-lookup"><span data-stu-id="c48f4-105">Contains the name of the profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c48f4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c48f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c48f4-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="c48f4-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="c48f4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c48f4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c48f4-109">0x3D12</span><span class="sxs-lookup"><span data-stu-id="c48f4-109">0x3D12</span></span>  <br/> |
|<span data-ttu-id="c48f4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c48f4-110">Data type:</span></span>  <br/> |<span data-ttu-id="c48f4-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c48f4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c48f4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c48f4-112">Area:</span></span>  <br/> |<span data-ttu-id="c48f4-113">MAPI-Profilkonfiguration</span><span class="sxs-lookup"><span data-stu-id="c48f4-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c48f4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c48f4-114">Remarks</span></span>

<span data-ttu-id="c48f4-115">Diese Eigenschaften werden von Dienstanbietern berechnet.</span><span class="sxs-lookup"><span data-stu-id="c48f4-115">These properties are computed by service providers.</span></span> <span data-ttu-id="c48f4-116">Die Implementierung der **ServiceEntry** -Funktion eines Anbieters kann diese Eigenschaften verwenden, um den Profilnamen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c48f4-116">A provider's implementation of the **ServiceEntry** function can use these properties to discover the profile name.</span></span> 
  
<span data-ttu-id="c48f4-117">Client Anwendungen können diese Eigenschaften als bequeme Alternative zum Abrufen des Profilnamens verwenden, indem Sie die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft in der Statustabellen Zeile des MAPI-Subsystems untersuchen.</span><span class="sxs-lookup"><span data-stu-id="c48f4-117">Client applications can use these properties as a convenient alternative to obtaining the profile name by examining the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MAPI subsystem's status table row.</span></span>
  
<span data-ttu-id="c48f4-118">Diese Eigenschaften sind möglicherweise nicht über die Zeit hinweg eindeutig, beispielsweise, wenn ein Profil gelöscht und später mit demselben Namen neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c48f4-118">These properties may not be unique across time, for example where a profile is deleted and later recreated with the same name.</span></span> <span data-ttu-id="c48f4-119">MAPI liefert eine vollständig eindeutige **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md))-Eigenschaft in einem hartcodierten Profil Abschnitt namens **MUID_PROFILE_INSTANCE.**</span><span class="sxs-lookup"><span data-stu-id="c48f4-119">MAPI furnishes a totally unique **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property in a hard-coded profile section called **MUID_PROFILE_INSTANCE.**</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c48f4-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c48f4-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c48f4-121">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="c48f4-121">Header files</span></span>

<span data-ttu-id="c48f4-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c48f4-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="c48f4-123">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="c48f4-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="c48f4-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c48f4-124">Mapitags.h</span></span>
  
> <span data-ttu-id="c48f4-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c48f4-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c48f4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c48f4-126">See also</span></span>



[<span data-ttu-id="c48f4-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c48f4-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c48f4-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c48f4-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c48f4-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c48f4-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c48f4-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c48f4-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

