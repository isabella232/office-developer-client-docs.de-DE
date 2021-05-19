---
title: PidTagOriginalSenderAddressType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderAddressType
api_type:
- COM
ms.assetid: bd777f19-cbb1-4497-8a0b-e05b491c6957
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d593b5ae1c2341ae0972ba68bcf42dde64e9a2f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342679"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a><span data-ttu-id="e7bcf-103">PidTagOriginalSenderAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e7bcf-103">PidTagOriginalSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="e7bcf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7bcf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7bcf-105">Enthält den Adresstyp des Absenders der ersten Version einer Nachricht, d. h. die Nachricht, bevor sie weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-105">Contains the address type of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7bcf-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e7bcf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7bcf-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="e7bcf-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="e7bcf-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e7bcf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e7bcf-109">0x0066</span><span class="sxs-lookup"><span data-stu-id="e7bcf-109">0x0066</span></span>  <br/> |
|<span data-ttu-id="e7bcf-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e7bcf-110">Data type:</span></span>  <br/> |<span data-ttu-id="e7bcf-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e7bcf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e7bcf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e7bcf-112">Area:</span></span>  <br/> |<span data-ttu-id="e7bcf-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="e7bcf-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7bcf-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e7bcf-114">Remarks</span></span>

<span data-ttu-id="e7bcf-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den ursprünglichen Absender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="e7bcf-116">Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaften auf den Wert PR_SENDER_ADDRTYPE **(** [PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) festlegen.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span></span> <span data-ttu-id="e7bcf-117">Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e7bcf-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e7bcf-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e7bcf-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e7bcf-119">Protocol specifications</span></span>

<span data-ttu-id="e7bcf-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7bcf-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7bcf-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e7bcf-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7bcf-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7bcf-123">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e7bcf-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="e7bcf-124">Header files</span></span>

<span data-ttu-id="e7bcf-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7bcf-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7bcf-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e7bcf-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e7bcf-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e7bcf-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e7bcf-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7bcf-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7bcf-129">See also</span></span>



[<span data-ttu-id="e7bcf-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7bcf-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7bcf-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="e7bcf-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7bcf-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e7bcf-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7bcf-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e7bcf-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

