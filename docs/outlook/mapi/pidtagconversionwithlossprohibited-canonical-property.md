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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 972df747e0ee459996b9b4da5732be1490fbd08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417126"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a><span data-ttu-id="e1a18-103">PidTagConversionWithLossProhibited (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e1a18-103">PidTagConversionWithLossProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="e1a18-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1a18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1a18-105">Enthält TRUE, wenn es einem Nachrichtenübertragungs-Agent (Message Transfer Agent, MTA) untersagt ist, Nachrichtentextkonvertierungen zu machen, die Informationen verlieren.</span><span class="sxs-lookup"><span data-stu-id="e1a18-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making message text conversions that lose information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1a18-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e1a18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1a18-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="e1a18-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="e1a18-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e1a18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1a18-109">0x000D</span><span class="sxs-lookup"><span data-stu-id="e1a18-109">0x000D</span></span>  <br/> |
|<span data-ttu-id="e1a18-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e1a18-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1a18-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e1a18-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e1a18-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e1a18-112">Area:</span></span>  <br/> |<span data-ttu-id="e1a18-113">Allgemeine Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e1a18-113">General configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1a18-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e1a18-114">Remarks</span></span>

<span data-ttu-id="e1a18-115">Ein Beispiel für die Art der unzulässigen Konvertierung ist die "verlustige" Zuordnung von Unicode (zwei Bytes pro Zeichen) zu einem Einzelnen-Byte-Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="e1a18-115">An example of the type of conversion being prohibited is the "lossy" mapping from Unicode (two bytes per character) to a single-byte character set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e1a18-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e1a18-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e1a18-117">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="e1a18-117">Header files</span></span>

<span data-ttu-id="e1a18-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1a18-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1a18-119">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e1a18-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1a18-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e1a18-120">Mapitags.h</span></span>
  
> <span data-ttu-id="e1a18-121">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e1a18-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1a18-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1a18-122">See also</span></span>



[<span data-ttu-id="e1a18-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1a18-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1a18-124">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="e1a18-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1a18-125">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e1a18-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1a18-126">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e1a18-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

