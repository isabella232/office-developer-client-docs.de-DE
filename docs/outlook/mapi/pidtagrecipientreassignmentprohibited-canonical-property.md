---
title: Kanonische Pidtagrecipientreassignmentprohibited (-Eigenschaft
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
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341111"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a><span data-ttu-id="406b6-103">Kanonische Pidtagrecipientreassignmentprohibited (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="406b6-103">PidTagRecipientReassignmentProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="406b6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="406b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="406b6-105">Gibt an, ob das Hinzufügen zusätzlicher Empfänger bei der Übermittlung der Nachricht für die e-Mail-Nachricht nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="406b6-105">Specifies whether adding additional recipients, when forwarding the message, is prohibited for the email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="406b6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="406b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="406b6-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="406b6-107">PR_RECIPIENT_REASSIGNMENT_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="406b6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="406b6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="406b6-109">0x002B</span><span class="sxs-lookup"><span data-stu-id="406b6-109">0x002B</span></span>  <br/> |
|<span data-ttu-id="406b6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="406b6-110">Data type:</span></span>  <br/> |<span data-ttu-id="406b6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="406b6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="406b6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="406b6-112">Area:</span></span>  <br/> |<span data-ttu-id="406b6-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="406b6-113">MAPI Envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="406b6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="406b6-114">Remarks</span></span>

<span data-ttu-id="406b6-115">Diese Eigenschaft wird basierend auf dem Wert der e-Mail-Nachricht **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="406b6-115">This property is set based on the email message's **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) value.</span></span> <span data-ttu-id="406b6-116">Wenn **PR_SENSITIVITY** auf "0x00000000" (normal) oder "0x00000003" (vertraulich) festgelegt ist, muss diese Eigenschaft auf "$ 00" festgelegt werden oder nicht, was bedeutet, dass das Hinzufügen von zusätzlichen oder unterschiedlichen Empfängern zur e-Mail-Nachricht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="406b6-116">If **PR_SENSITIVITY** is set to "0x00000000" (normal) or "0x00000003" (confidential), this property must be set to "0x00" or absent meaning that adding additional or different recipients to the email message is allowed.</span></span> <span data-ttu-id="406b6-117">Wenn das **PR_SENSITIVITY** des e-Mail-Objekts auf "0x00000001" (persönlich) oder "0x00000002" (privat) festgelegt ist, muss diese Eigenschaft auf "0x01" festgelegt werden, um das Hinzufügen zusätzlicher oder anderer Empfänger dieser e-Mail durch die Weiterleitung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="406b6-117">If the email object's **PR_SENSITIVITY** is set to "0x00000001" (personal) or "0x00000002" (private), this property must be set "0x01" to prevent adding additional or different recipients of this email through forwarding.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="406b6-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="406b6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="406b6-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="406b6-119">Protocol specifications</span></span>

<span data-ttu-id="406b6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="406b6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="406b6-121">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="406b6-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="406b6-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="406b6-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="406b6-123">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="406b6-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="406b6-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="406b6-124">Header files</span></span>

<span data-ttu-id="406b6-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="406b6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="406b6-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="406b6-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="406b6-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="406b6-127">Mapitags.h</span></span>
  
> <span data-ttu-id="406b6-128">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="406b6-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="406b6-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="406b6-129">See also</span></span>



[<span data-ttu-id="406b6-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="406b6-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="406b6-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="406b6-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="406b6-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="406b6-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="406b6-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="406b6-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

