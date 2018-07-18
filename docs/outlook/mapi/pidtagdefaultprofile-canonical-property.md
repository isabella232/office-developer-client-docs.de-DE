---
title: PidTagDefaultProfile (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6cd255c60987ec7a279e509aa2925a8029cce62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794272"
---
# <a name="pidtagdefaultprofile-canonical-property"></a><span data-ttu-id="90087-103">PidTagDefaultProfile (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="90087-103">PidTagDefaultProfile Canonical Property</span></span>

  
  
<span data-ttu-id="90087-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90087-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90087-105">Enthält True, wenn ein Benutzerprofil messaging das MAPI-Standardprofil ist.</span><span class="sxs-lookup"><span data-stu-id="90087-105">Contains TRUE if a messaging user profile is the MAPI default profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90087-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="90087-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90087-107">PR_DEFAULT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="90087-107">PR_DEFAULT_PROFILE</span></span>  <br/> |
|<span data-ttu-id="90087-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="90087-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90087-109">0x3D04</span><span class="sxs-lookup"><span data-stu-id="90087-109">0x3D04</span></span>  <br/> |
|<span data-ttu-id="90087-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="90087-110">Data type:</span></span>  <br/> |<span data-ttu-id="90087-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="90087-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="90087-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="90087-112">Area:</span></span>  <br/> |<span data-ttu-id="90087-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="90087-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90087-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90087-114">Remarks</span></span>

<span data-ttu-id="90087-115">Diese Eigenschaft wird nicht als eine Eigenschaft eines Objekts, sondern nur als eine Spalte in einer Profiltabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="90087-115">This property does not appear as a property of any object but only as a column in a profile table.</span></span> <span data-ttu-id="90087-116">Die [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) -Methode können eine Clientanwendung aus das Standardprofil auswählen.</span><span class="sxs-lookup"><span data-stu-id="90087-116">A client application can use the [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) method to designate the default profile.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="90087-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="90087-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="90087-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="90087-118">Header files</span></span>

<span data-ttu-id="90087-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90087-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="90087-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="90087-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="90087-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="90087-121">Mapitags.h</span></span>
  
> <span data-ttu-id="90087-122">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="90087-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90087-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90087-123">See also</span></span>



[<span data-ttu-id="90087-124">PidTagDefaultStore (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="90087-124">PidTagDefaultStore Canonical Property</span></span>](pidtagdefaultstore-canonical-property.md)


[<span data-ttu-id="90087-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90087-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90087-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90087-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90087-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="90087-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90087-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="90087-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

