---
title: Kanonische PidTagDefCreateDl-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3fb86fba3b0ff8a79858fad59dca61069aff6db9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794297"
---
# <a name="pidtagdefcreatedl-canonical-property"></a><span data-ttu-id="57208-103">Kanonische PidTagDefCreateDl-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="57208-103">PidTagDefCreateDl Canonical Property</span></span>

  
  
<span data-ttu-id="57208-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="57208-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="57208-105">Enthält die Vorlage Eintrags-ID für eine Verteilerliste Standard.</span><span class="sxs-lookup"><span data-stu-id="57208-105">Contains the template entry identifier for a default distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57208-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="57208-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="57208-107">PR_DEF_CREATE_DL</span><span class="sxs-lookup"><span data-stu-id="57208-107">PR_DEF_CREATE_DL</span></span>  <br/> |
|<span data-ttu-id="57208-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="57208-108">Identifier:</span></span>  <br/> |<span data-ttu-id="57208-109">0x3611</span><span class="sxs-lookup"><span data-stu-id="57208-109">0x3611</span></span>  <br/> |
|<span data-ttu-id="57208-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="57208-110">Data type:</span></span>  <br/> |<span data-ttu-id="57208-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="57208-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="57208-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="57208-112">Area:</span></span>  <br/> |<span data-ttu-id="57208-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="57208-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57208-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="57208-114">Remarks</span></span>

<span data-ttu-id="57208-115">Clientanwendungen mit dieser Eigenschaft können Sie um eine Verteilerliste in einem Container zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="57208-115">Client applications use this property to create a distribution list within a container.</span></span> <span data-ttu-id="57208-116">Unterstützung von Eintrag Creation ist optional für Address Book Container. die, die nicht unterstützen sind nicht erforderlich, diese Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="57208-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="57208-117">Diese Eigenschaft gibt einen Eintrag, der angezeigt werden, kann in der Eigenschaft **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) für Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="57208-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for distribution lists.</span></span> <span data-ttu-id="57208-118">Wenn den Bezeichner erhalten haben, verwendet der Client es in einem Aufruf der [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="57208-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="57208-119">Der Eintrag stellt die Vorlage für die Standard-Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="57208-119">The entry represents the template for the default distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="57208-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="57208-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="57208-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="57208-121">Header files</span></span>

<span data-ttu-id="57208-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="57208-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="57208-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="57208-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="57208-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="57208-124">Mapitags.h</span></span>
  
> <span data-ttu-id="57208-125">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="57208-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57208-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57208-126">See also</span></span>



[<span data-ttu-id="57208-127">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="57208-127">IABLogon::CompareEntryIDs</span></span>](iablogon-compareentryids.md)


[<span data-ttu-id="57208-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="57208-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="57208-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="57208-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="57208-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="57208-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="57208-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="57208-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
