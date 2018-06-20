---
title: Kanonische PidTagReadReceiptSearchKey-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptSearchKey
api_type:
- COM
ms.assetid: a0ea5628-1393-4ab8-bc34-a58cf130db51
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3210a8ab29127120ff139de51761bd84722ca52d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794862"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a><span data-ttu-id="5912d-103">Kanonische PidTagReadReceiptSearchKey-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5912d-103">PidTagReadReceiptSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="5912d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5912d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5912d-105">Enthält einen Schlüssel Suche für die messaging-Benutzer an den messaging-System einen lesen-Bericht für eine Nachricht senden sollen.</span><span class="sxs-lookup"><span data-stu-id="5912d-105">Contains a search key for the messaging user to which the messaging system should direct a read report for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5912d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5912d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5912d-107">PR_READ_RECEIPT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="5912d-107">PR_READ_RECEIPT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="5912d-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5912d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5912d-109">0x0053</span><span class="sxs-lookup"><span data-stu-id="5912d-109">0x0053</span></span>  <br/> |
|<span data-ttu-id="5912d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5912d-110">Data type:</span></span>  <br/> |<span data-ttu-id="5912d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5912d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5912d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5912d-112">Area:</span></span>  <br/> |<span data-ttu-id="5912d-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="5912d-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5912d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5912d-114">Remarks</span></span>

<span data-ttu-id="5912d-115">Diese Eigenschaft wird ignoriert, es sei denn, die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft auf TRUE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5912d-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="5912d-116">Wenn eine Clientanwendung empfangen möchte, kann lesen Sie Berichte selbst, es lassen Sie diese Eigenschaft nicht festgelegt oder legen Sie ihn auf die suchen-Taste, die in der Eigenschaft **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) Zeitpunkt der Übermittlung von Nachricht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5912d-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the search key contained in the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5912d-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5912d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5912d-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5912d-118">Protocol specifications</span></span>

<span data-ttu-id="5912d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5912d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5912d-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5912d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5912d-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5912d-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5912d-122">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5912d-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5912d-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5912d-123">Header files</span></span>

<span data-ttu-id="5912d-124">Mapidef.h</span><span class="sxs-lookup"><span data-stu-id="5912d-124">Mapidef.h</span></span>
  
> <span data-ttu-id="5912d-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5912d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="5912d-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5912d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="5912d-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5912d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5912d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5912d-128">See also</span></span>



[<span data-ttu-id="5912d-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5912d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5912d-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5912d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5912d-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5912d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5912d-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5912d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

