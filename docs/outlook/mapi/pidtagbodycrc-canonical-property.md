---
title: Kanonische Pidtagbodycrc (-Eigenschaft
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
ms.openlocfilehash: 416486c3b06c485a1fa6525b54c37a6e0d23f56c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415180"
---
# <a name="pidtagbodycrc-canonical-property"></a><span data-ttu-id="7f63d-103">Kanonische Pidtagbodycrc (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7f63d-103">PidTagBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="7f63d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f63d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f63d-105">Enthält einen CRC-Wert (zyklische Redundanzprüfung) für den Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="7f63d-105">Contains a cyclic redundancy check (CRC) value on the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f63d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7f63d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f63d-107">PR_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="7f63d-107">PR_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="7f63d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7f63d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f63d-109">0x0E1C</span><span class="sxs-lookup"><span data-stu-id="7f63d-109">0x0E1C</span></span>  <br/> |
|<span data-ttu-id="7f63d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7f63d-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f63d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7f63d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7f63d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7f63d-112">Area:</span></span>  <br/> |<span data-ttu-id="7f63d-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="7f63d-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f63d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f63d-114">Remarks</span></span>

<span data-ttu-id="7f63d-115">Der Nachrichtenspeicher kann einen beliebigen CRC-Algorithmus verwenden, der einen PT_LONG-Wert generiert.</span><span class="sxs-lookup"><span data-stu-id="7f63d-115">The message store can use any CRC algorithm that generates a PT_LONG value.</span></span> <span data-ttu-id="7f63d-116">Diese Eigenschaft muss als Teil der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode berechnet werden, wenn die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft zum ersten Mal festgelegt wurde und wenn Sie anschließend geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7f63d-116">It must compute this property as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property has been set for the first time and whenever it has been subsequently modified.</span></span>
  
<span data-ttu-id="7f63d-117">Eine Clientanwendung verwendet **PR_BODY_CRC** , um die in **PR_BODY** -Eigenschaften oder deren Varianten enthaltenen Nachrichtentext Zeichenfolgen zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="7f63d-117">A client application uses **PR_BODY_CRC** to aid in comparing message text strings contained in **PR_BODY** properties or their variants.</span></span> <span data-ttu-id="7f63d-118">Mit dieser Eigenschaft kann der Client schnell und einfach erkennen, wann der Nachrichtentext geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7f63d-118">Using this property, the client can quickly and easily detect when the message text has changed.</span></span> <span data-ttu-id="7f63d-119">Mithilfe von **PR_BODY_CRC** können Sie beträchtliche Leistungssteigerungen erzielen, statt **PR_BODY** aus dem Nachrichtenspeicher abzurufen und mit einer lokalen Version zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="7f63d-119">It can realize significant performance gains by using **PR_BODY_CRC** instead of obtaining **PR_BODY** from the message store and comparing it with a local version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7f63d-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7f63d-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7f63d-121">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="7f63d-121">Header files</span></span>

<span data-ttu-id="7f63d-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7f63d-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f63d-123">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="7f63d-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f63d-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7f63d-124">Mapitags.h</span></span>
  
> <span data-ttu-id="7f63d-125">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="7f63d-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f63d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f63d-126">See also</span></span>



[<span data-ttu-id="7f63d-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7f63d-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f63d-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7f63d-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f63d-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7f63d-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f63d-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7f63d-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

