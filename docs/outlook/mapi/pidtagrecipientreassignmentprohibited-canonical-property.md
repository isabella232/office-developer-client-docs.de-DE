---
title: PidTagRecipientReassignmentProhibited (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341111"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="6fc85-103">PidTagRecipientReassignmentProhibited (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6fc85-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="6fc85-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fc85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fc85-105">Gibt an, ob das Hinzufügen zusätzlicher Empfänger beim Weiterleiten der Nachricht für die E-Mail-Nachricht nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6fc85-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6fc85-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6fc85-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6fc85-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="6fc85-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="6fc85-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6fc85-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6fc85-109">0x002B</span><span class="sxs-lookup"><span data-stu-id="6fc85-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="6fc85-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6fc85-110">Data type:</span></span>  <br/> |<span data-ttu-id="6fc85-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6fc85-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6fc85-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6fc85-112">Area:</span></span>  <br/> |<span data-ttu-id="6fc85-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="6fc85-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6fc85-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6fc85-114">Remarks</span></span>

<span data-ttu-id="6fc85-115">Diese Eigenschaft wird basierend auf dem Wert PR_SENSITIVITY **(** [PidTagSensitivity](pidtagsensitivity-canonical-property.md)) der E-Mail-Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6fc85-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="6fc85-116">Wenn **PR_SENSITIVITY** auf "0x00000000" (normal) oder "0x00000003" (vertraulich) festgelegt ist, muss diese Eigenschaft auf "0x00" oder nicht festgelegt sein, was bedeutet, dass das Hinzufügen zusätzlicher oder anderer Empfänger zur E-Mail-Nachricht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6fc85-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="6fc85-117">Wenn die PR_SENSITIVITY  des E-Mail-Objekts auf "0x00000001" (persönlich) oder "0x00000002" (privat) festgelegt ist, muss diese Eigenschaft "0x01" festgelegt werden, um zu verhindern, dass zusätzliche oder andere Empfänger dieser E-Mail durch Weiterleitung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6fc85-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6fc85-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6fc85-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6fc85-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6fc85-119">Protocol specifications</span></span>

<span data-ttu-id="6fc85-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6fc85-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6fc85-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6fc85-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6fc85-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6fc85-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6fc85-123">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6fc85-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6fc85-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="6fc85-124">Header files</span></span>

<span data-ttu-id="6fc85-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6fc85-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6fc85-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6fc85-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="6fc85-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6fc85-127">Mapitags.h</span></span>
  
> <span data-ttu-id="6fc85-128">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6fc85-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6fc85-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fc85-129">See also</span></span>



[<span data-ttu-id="6fc85-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6fc85-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6fc85-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="6fc85-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6fc85-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6fc85-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6fc85-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6fc85-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

