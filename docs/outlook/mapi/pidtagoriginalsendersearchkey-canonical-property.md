---
title: Kanonische PidTagOriginalSenderSearchKey-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderSearchKey
api_type:
- COM
ms.assetid: 164eb9dd-e553-459e-99c1-3da0284bb01f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2aa0a8601a72b6d4c40167ac55d3d643bf946708
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794704"
---
# <a name="pidtagoriginalsendersearchkey-canonical-property"></a><span data-ttu-id="0e0bd-103">Kanonische PidTagOriginalSenderSearchKey-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0e0bd-103">PidTagOriginalSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="0e0bd-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e0bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e0bd-105">Enthält den Search-Schlüssel für den Absender der ersten Version einer Nachricht, d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-105">Contains the search key for the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e0bd-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0e0bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e0bd-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="0e0bd-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="0e0bd-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="0e0bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e0bd-109">0x005C</span><span class="sxs-lookup"><span data-stu-id="0e0bd-109">0x005C</span></span>  <br/> |
|<span data-ttu-id="0e0bd-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0e0bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e0bd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0e0bd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0e0bd-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0e0bd-112">Area:</span></span>  <br/> |<span data-ttu-id="0e0bd-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="0e0bd-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e0bd-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0e0bd-114">Remarks</span></span>

<span data-ttu-id="0e0bd-115">Diese Eigenschaft ist eine der Adresseigenschaften für den ursprünglichen Absender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="0e0bd-116">Am ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaft auf den Wert der Eigenschaft **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property.</span></span> <span data-ttu-id="0e0bd-117">Es wird nie geändert, wenn die Nachricht weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0e0bd-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0e0bd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e0bd-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0e0bd-119">Protocol specifications</span></span>

<span data-ttu-id="0e0bd-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e0bd-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e0bd-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e0bd-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e0bd-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e0bd-123">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e0bd-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0e0bd-124">Header files</span></span>

<span data-ttu-id="0e0bd-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e0bd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e0bd-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e0bd-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0e0bd-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0e0bd-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0e0bd-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e0bd-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e0bd-129">See also</span></span>



[<span data-ttu-id="0e0bd-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0e0bd-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e0bd-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0e0bd-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e0bd-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0e0bd-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e0bd-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0e0bd-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
