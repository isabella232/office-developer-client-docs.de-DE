---
title: Kanonische Pidtagreadreceiptsearchkey (-Eigenschaft
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
ms.openlocfilehash: aa92e224f10fd652078b965c8e3a0b5ab59cc388
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320041"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a><span data-ttu-id="e4bcb-103">Kanonische Pidtagreadreceiptsearchkey (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e4bcb-103">PidTagReadReceiptSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="e4bcb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4bcb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4bcb-105">Enthält einen Suchschlüssel für den Messagingbenutzer, an den das Messagingsystem einen Lesebericht für eine Nachricht weiterleiten soll.</span><span class="sxs-lookup"><span data-stu-id="e4bcb-105">Contains a search key for the messaging user to which the messaging system should direct a read report for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e4bcb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e4bcb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e4bcb-107">PR_READ_RECEIPT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="e4bcb-107">PR_READ_RECEIPT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="e4bcb-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e4bcb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e4bcb-109">0x0053</span><span class="sxs-lookup"><span data-stu-id="e4bcb-109">0x0053</span></span>  <br/> |
|<span data-ttu-id="e4bcb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e4bcb-110">Data type:</span></span>  <br/> |<span data-ttu-id="e4bcb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e4bcb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e4bcb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e4bcb-112">Area:</span></span>  <br/> |<span data-ttu-id="e4bcb-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="e4bcb-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4bcb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4bcb-114">Remarks</span></span>

<span data-ttu-id="e4bcb-115">Diese Eigenschaft wird ignoriert, wenn die **PR_READ_RECEIPT_REQUESTED** ([pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e4bcb-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="e4bcb-116">Wenn eine Clientanwendung Lese Berichte selbst empfangen möchte, kann diese Eigenschaft nicht festgelegt werden, oder Sie wird auf den in der **PR_SENDER_SEARCH_KEY** ([pidtagsendersearchkey (](pidtagsendersearchkey-canonical-property.md))-Eigenschaft enthaltenen Suchschlüssel bei der Übermittlungszeit von Nachrichten eingestellt.</span><span class="sxs-lookup"><span data-stu-id="e4bcb-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the search key contained in the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e4bcb-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e4bcb-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e4bcb-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e4bcb-118">Protocol specifications</span></span>

<span data-ttu-id="e4bcb-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e4bcb-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e4bcb-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e4bcb-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e4bcb-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e4bcb-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e4bcb-122">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e4bcb-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e4bcb-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e4bcb-123">Header files</span></span>

<span data-ttu-id="e4bcb-124">Mapidef. h</span><span class="sxs-lookup"><span data-stu-id="e4bcb-124">Mapidef.h</span></span>
  
> <span data-ttu-id="e4bcb-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e4bcb-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="e4bcb-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e4bcb-126">Mapitags.h</span></span>
  
> <span data-ttu-id="e4bcb-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e4bcb-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e4bcb-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4bcb-128">See also</span></span>



[<span data-ttu-id="e4bcb-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4bcb-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e4bcb-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4bcb-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e4bcb-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e4bcb-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e4bcb-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e4bcb-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

