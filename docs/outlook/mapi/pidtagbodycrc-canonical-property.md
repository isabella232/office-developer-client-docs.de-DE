---
title: PidTagBodyCrc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 66a150cf3f83465840aa0e79a9ef921b1534f814
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794152"
---
# <a name="pidtagbodycrc-canonical-property"></a><span data-ttu-id="64462-103">PidTagBodyCrc (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="64462-103">PidTagBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="64462-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="64462-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="64462-105">Enthält einen CRC CRC-Prüfung Wert auf den Nachrichtentext an.</span><span class="sxs-lookup"><span data-stu-id="64462-105">Contains a cyclic redundancy check (CRC) value on the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64462-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="64462-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64462-107">PR_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="64462-107">PR_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="64462-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="64462-108">Identifier:</span></span>  <br/> |<span data-ttu-id="64462-109">0x0E1C</span><span class="sxs-lookup"><span data-stu-id="64462-109">0x0E1C</span></span>  <br/> |
|<span data-ttu-id="64462-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="64462-110">Data type:</span></span>  <br/> |<span data-ttu-id="64462-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="64462-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="64462-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="64462-112">Area:</span></span>  <br/> |<span data-ttu-id="64462-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="64462-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64462-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64462-114">Remarks</span></span>

<span data-ttu-id="64462-115">Der Nachrichtenspeicher können jeder CRC-Algorithmus, der einen PT_LONG Wert generiert.</span><span class="sxs-lookup"><span data-stu-id="64462-115">The message store can use any CRC algorithm that generates a PT_LONG value.</span></span> <span data-ttu-id="64462-116">Es muss diese Eigenschaft als Teil der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode berechnen, wenn die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft festgelegt wurde, zum ersten Mal und wenn es später geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="64462-116">It must compute this property as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property has been set for the first time and whenever it has been subsequently modified.</span></span>
  
<span data-ttu-id="64462-117">Eine Clientanwendung verwendet **PR_BODY_CRC** zur Unterstützung bei der vergleichen Nachricht Textzeichenfolgen in **PR_BODY** Eigenschaften oder deren Varianten enthalten.</span><span class="sxs-lookup"><span data-stu-id="64462-117">A client application uses **PR_BODY_CRC** to aid in comparing message text strings contained in **PR_BODY** properties or their variants.</span></span> <span data-ttu-id="64462-118">Mithilfe dieser Eigenschaft, kann der Client schnell und einfach erkennen, wann der Nachrichtentext geändert hat.</span><span class="sxs-lookup"><span data-stu-id="64462-118">Using this property, the client can quickly and easily detect when the message text has changed.</span></span> <span data-ttu-id="64462-119">Es kann erhebliche Leistungssteigerungen Realisierung von über **PR_BODY_CRC** anstatt **PR_BODY** aus dem Nachrichtenspeicher abrufen und diese mit einer lokalen Version zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="64462-119">It can realize significant performance gains by using **PR_BODY_CRC** instead of obtaining **PR_BODY** from the message store and comparing it with a local version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="64462-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="64462-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="64462-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="64462-121">Header files</span></span>

<span data-ttu-id="64462-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64462-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="64462-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="64462-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="64462-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="64462-124">Mapitags.h</span></span>
  
> <span data-ttu-id="64462-125">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="64462-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64462-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64462-126">See also</span></span>



[<span data-ttu-id="64462-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="64462-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64462-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="64462-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64462-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="64462-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64462-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="64462-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

