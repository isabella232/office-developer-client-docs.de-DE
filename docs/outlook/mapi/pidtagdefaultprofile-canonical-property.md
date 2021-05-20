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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8295ae6904f503ca831a00c1f35ac08596b5358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428774"
---
# <a name="pidtagdefaultprofile-canonical-property"></a><span data-ttu-id="dfb7f-103">PidTagDefaultProfile (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dfb7f-103">PidTagDefaultProfile Canonical Property</span></span>

  
  
<span data-ttu-id="dfb7f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfb7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfb7f-105">Enthält TRUE, wenn ein Messagingbenutzerprofil das MAPI-Standardprofil ist.</span><span class="sxs-lookup"><span data-stu-id="dfb7f-105">Contains TRUE if a messaging user profile is the MAPI default profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dfb7f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dfb7f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dfb7f-107">PR_DEFAULT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="dfb7f-107">PR_DEFAULT_PROFILE</span></span>  <br/> |
|<span data-ttu-id="dfb7f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="dfb7f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dfb7f-109">0x3D04</span><span class="sxs-lookup"><span data-stu-id="dfb7f-109">0x3D04</span></span>  <br/> |
|<span data-ttu-id="dfb7f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dfb7f-110">Data type:</span></span>  <br/> |<span data-ttu-id="dfb7f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="dfb7f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="dfb7f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dfb7f-112">Area:</span></span>  <br/> |<span data-ttu-id="dfb7f-113">MAPI-Profil</span><span class="sxs-lookup"><span data-stu-id="dfb7f-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dfb7f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dfb7f-114">Remarks</span></span>

<span data-ttu-id="dfb7f-115">Diese Eigenschaft wird nicht als Eigenschaft eines Objekts, sondern nur als Spalte in einer Profiltabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dfb7f-115">This property does not appear as a property of any object but only as a column in a profile table.</span></span> <span data-ttu-id="dfb7f-116">Eine Clientanwendung kann die [IProfAdmin::SetDefaultProfile-Methode](iprofadmin-setdefaultprofile.md) verwenden, um das Standardprofil zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="dfb7f-116">A client application can use the [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) method to designate the default profile.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dfb7f-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dfb7f-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="dfb7f-118">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="dfb7f-118">Header files</span></span>

<span data-ttu-id="dfb7f-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dfb7f-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="dfb7f-120">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="dfb7f-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="dfb7f-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dfb7f-121">Mapitags.h</span></span>
  
> <span data-ttu-id="dfb7f-122">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="dfb7f-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dfb7f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfb7f-123">See also</span></span>



[<span data-ttu-id="dfb7f-124">PidTagDefaultStore (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dfb7f-124">PidTagDefaultStore Canonical Property</span></span>](pidtagdefaultstore-canonical-property.md)


[<span data-ttu-id="dfb7f-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dfb7f-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dfb7f-126">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="dfb7f-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dfb7f-127">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dfb7f-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dfb7f-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dfb7f-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

