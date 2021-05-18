---
title: PidTagExpiryNumber (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryNumber
api_type:
- HeaderDef
ms.assetid: 644e8d3d-1792-4417-95a1-e978d0e6cd8e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: da90347f5aacdb2fcac8547eddd5b89a0a44820d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316366"
---
# <a name="pidtagexpirynumber-canonical-property"></a><span data-ttu-id="ed117-103">PidTagExpiryNumber (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ed117-103">PidTagExpiryNumber Canonical Property</span></span>

  
  
<span data-ttu-id="ed117-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed117-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed117-105">Definiert die Ablauf sendezeit in Verbindung mit der **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ed117-105">Defines the expiry send time in conjunction with the **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed117-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ed117-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed117-107">PR_EXPIRY_NUMBER</span><span class="sxs-lookup"><span data-stu-id="ed117-107">PR_EXPIRY_NUMBER</span></span>  <br/> |
|<span data-ttu-id="ed117-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ed117-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed117-109">0x3FED</span><span class="sxs-lookup"><span data-stu-id="ed117-109">0x3FED</span></span>  <br/> |
|<span data-ttu-id="ed117-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ed117-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed117-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ed117-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ed117-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ed117-112">Area:</span></span>  <br/> |<span data-ttu-id="ed117-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="ed117-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed117-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed117-114">Remarks</span></span>

<span data-ttu-id="ed117-115">Der Wert dieser Eigenschaft muss zwischen 0 und einschließlich 999 festgelegt werden, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ed117-115">This property's value must be set between 0 and 999 inclusive, if it is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ed117-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ed117-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed117-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ed117-117">Protocol specifications</span></span>

<span data-ttu-id="ed117-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed117-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed117-119">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ed117-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed117-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ed117-120">Header files</span></span>

<span data-ttu-id="ed117-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed117-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed117-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ed117-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed117-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ed117-123">Mapitags.h</span></span>
  
> <span data-ttu-id="ed117-124">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ed117-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed117-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed117-125">See also</span></span>



[<span data-ttu-id="ed117-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed117-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed117-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ed117-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed117-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ed117-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed117-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ed117-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

