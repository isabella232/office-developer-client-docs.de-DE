---
title: PidTagContentCorrelator (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2290e6751778f17defc8d1007ff62c88f1b75465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794224"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="1cc23-103">PidTagContentCorrelator (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1cc23-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="1cc23-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1cc23-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1cc23-105">Enthält einen Wert, den Absender der Nachricht verwenden kann, um einen Bericht mit der ursprünglichen Nachricht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="1cc23-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1cc23-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1cc23-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1cc23-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="1cc23-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="1cc23-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="1cc23-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1cc23-109">0 x 0007</span><span class="sxs-lookup"><span data-stu-id="1cc23-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="1cc23-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1cc23-110">Data type:</span></span>  <br/> |<span data-ttu-id="1cc23-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1cc23-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1cc23-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1cc23-112">Area:</span></span>  <br/> |<span data-ttu-id="1cc23-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="1cc23-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cc23-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cc23-114">Remarks</span></span>

<span data-ttu-id="1cc23-115">Der Inhalt von binären Zeichenfolgen werden durch den Absender der Nachricht definiert.</span><span class="sxs-lookup"><span data-stu-id="1cc23-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="1cc23-116">Wenn Sie auf eine ausgehende Nachricht, diese Eigenschaft auf Berichte, die als Antwort auf die Nachricht generiert kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1cc23-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1cc23-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1cc23-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1cc23-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1cc23-118">Header files</span></span>

<span data-ttu-id="1cc23-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1cc23-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="1cc23-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1cc23-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="1cc23-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1cc23-121">Mapitags.h</span></span>
  
> <span data-ttu-id="1cc23-122">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1cc23-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1cc23-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cc23-123">See also</span></span>



[<span data-ttu-id="1cc23-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1cc23-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1cc23-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1cc23-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1cc23-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1cc23-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1cc23-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1cc23-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

