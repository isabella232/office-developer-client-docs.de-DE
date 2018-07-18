---
title: PidTagReadReceiptEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptEntryId
api_type:
- COM
ms.assetid: 141d49c8-87cf-4d80-a33b-ccbf3eeae19e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 82bc5fd99df115527f703eff7261d02d1bf4d3ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794857"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="323ff-103">PidTagReadReceiptEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="323ff-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="323ff-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="323ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="323ff-105">Enthält einen Eintrag Bezeichner für die messaging-Benutzer, in dem das messaging-System Berichtselemente Lesen für diese Nachricht senden sollen.</span><span class="sxs-lookup"><span data-stu-id="323ff-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="323ff-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="323ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="323ff-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="323ff-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="323ff-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="323ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="323ff-109">0 x 0046</span><span class="sxs-lookup"><span data-stu-id="323ff-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="323ff-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="323ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="323ff-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="323ff-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="323ff-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="323ff-112">Area:</span></span>  <br/> |<span data-ttu-id="323ff-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="323ff-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="323ff-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="323ff-114">Remarks</span></span>

<span data-ttu-id="323ff-115">Diese Eigenschaft wird ignoriert, es sei denn, die **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft auf TRUE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="323ff-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="323ff-116">Wenn eine Clientanwendung empfangen möchte, kann lesen Sie Berichte selbst, es lassen Sie diese Eigenschaft nicht festgelegt oder legen Sie es an die Eintrags-ID, die in der Eigenschaft **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) Zeitpunkt der Übermittlung von Nachricht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="323ff-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="323ff-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="323ff-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="323ff-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="323ff-118">Protocol specifications</span></span>

<span data-ttu-id="323ff-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="323ff-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="323ff-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="323ff-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="323ff-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="323ff-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="323ff-122">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="323ff-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="323ff-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="323ff-123">Header files</span></span>

<span data-ttu-id="323ff-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="323ff-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="323ff-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="323ff-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="323ff-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="323ff-126">Mapitags.h</span></span>
  
> <span data-ttu-id="323ff-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="323ff-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="323ff-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="323ff-128">See also</span></span>



[<span data-ttu-id="323ff-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="323ff-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="323ff-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="323ff-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="323ff-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="323ff-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="323ff-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="323ff-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

