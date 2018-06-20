---
title: Kanonische PidTagRecipientReassignmentProhibited-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0176485ca9b84260176e3be8ec9c8f42cf755cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794914"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="bede0-103">Kanonische PidTagRecipientReassignmentProhibited-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bede0-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="bede0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bede0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bede0-105">Gibt an, ob weitere Empfänger hinzufügen, wenn die Nachricht weitergeleitet für die e-Mail-Nachricht nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="bede0-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bede0-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bede0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bede0-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="bede0-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="bede0-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="bede0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bede0-109">0x002B</span><span class="sxs-lookup"><span data-stu-id="bede0-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="bede0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bede0-110">Data type:</span></span>  <br/> |<span data-ttu-id="bede0-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bede0-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bede0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bede0-112">Area:</span></span>  <br/> |<span data-ttu-id="bede0-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="bede0-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bede0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bede0-114">Remarks</span></span>

<span data-ttu-id="bede0-115">Diese Eigenschaft wird basierend auf der e-Mail-Nachricht **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bede0-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="bede0-116">**PR_SENSITIVITY** festgelegt ist "0 x 00000000" (normal) oder "0 x 00000003" (vertraulich), diese Eigenschaft auf "0 x 00" oder nicht vorhanden ist, was bedeutet, dass das Hinzufügen festgelegt werden muss zusätzliche oder andere Empfänger der e-Mail-Nachricht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="bede0-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="bede0-117">Wenn die e-Mail-Objekts **PR_SENSITIVITY** auf "0 x 00000001" (personal) oder "0 x 00000002" (privat) festgelegt ist, diese Eigenschaft muss festgelegt werden "0 x 01" zum Hinzufügen von zusätzlicher oder anderen Empfängern dieser e-Mail über Weiterleitung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="bede0-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bede0-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bede0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bede0-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bede0-119">Protocol specifications</span></span>

<span data-ttu-id="bede0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bede0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bede0-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bede0-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bede0-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bede0-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bede0-123">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bede0-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bede0-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bede0-124">Header files</span></span>

<span data-ttu-id="bede0-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bede0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bede0-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bede0-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="bede0-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bede0-127">Mapitags.h</span></span>
  
> <span data-ttu-id="bede0-128">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bede0-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bede0-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bede0-129">See also</span></span>



[<span data-ttu-id="bede0-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bede0-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bede0-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bede0-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bede0-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bede0-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bede0-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bede0-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

