---
title: PidTagConversionWithLossProhibited (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: eee70d97c35c7f115e424905b9e36f3dfa392c02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794277"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a><span data-ttu-id="e3bd4-103">PidTagConversionWithLossProhibited (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e3bd4-103">PidTagConversionWithLossProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="e3bd4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e3bd4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e3bd4-105">Enthält True, wenn ein Message Transfer Agent (MTA) verboten wird tätigen Nachricht Text Konvertierungen, die Informationen verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="e3bd4-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making message text conversions that lose information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3bd4-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e3bd4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3bd4-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="e3bd4-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="e3bd4-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="e3bd4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e3bd4-109">0x000d</span><span class="sxs-lookup"><span data-stu-id="e3bd4-109">0x000D</span></span>  <br/> |
|<span data-ttu-id="e3bd4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e3bd4-110">Data type:</span></span>  <br/> |<span data-ttu-id="e3bd4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e3bd4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e3bd4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e3bd4-112">Area:</span></span>  <br/> |<span data-ttu-id="e3bd4-113">Allgemeine Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e3bd4-113">General configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3bd4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3bd4-114">Remarks</span></span>

<span data-ttu-id="e3bd4-115">Ein Beispiel für die Art der Konvertierung wird nicht zulässig ist die "Verlust" Zuordnung von Unicode (zwei Bytes pro Zeichen) in einer Einzel-Byte-Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="e3bd4-115">An example of the type of conversion being prohibited is the "lossy" mapping from Unicode (two bytes per character) to a single-byte character set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e3bd4-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e3bd4-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e3bd4-117">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e3bd4-117">Header files</span></span>

<span data-ttu-id="e3bd4-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3bd4-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3bd4-119">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e3bd4-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="e3bd4-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e3bd4-120">Mapitags.h</span></span>
  
> <span data-ttu-id="e3bd4-121">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e3bd4-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3bd4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3bd4-122">See also</span></span>



[<span data-ttu-id="e3bd4-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3bd4-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3bd4-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3bd4-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3bd4-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e3bd4-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3bd4-126">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e3bd4-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

