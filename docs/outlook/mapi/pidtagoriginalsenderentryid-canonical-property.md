---
title: PidTagOriginalSenderEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEntryId
api_type:
- COM
ms.assetid: bd182589-afea-4967-92f5-ba1914e4db3f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0b30a61d3bce6d1e6295edb1e93e27b9f7fc8363
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574444"
---
# <a name="pidtagoriginalsenderentryid-canonical-property"></a><span data-ttu-id="0047c-103">PidTagOriginalSenderEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0047c-103">PidTagOriginalSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="0047c-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0047c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0047c-105">Enthält die Eintrags-ID des Absenders einer Nachricht, d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird die erste Version.</span><span class="sxs-lookup"><span data-stu-id="0047c-105">Contains the entry identifier of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0047c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0047c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0047c-107">PR_ORIGINAL_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0047c-107">PR_ORIGINAL_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="0047c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0047c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0047c-109">0x005B</span><span class="sxs-lookup"><span data-stu-id="0047c-109">0x005B</span></span>  <br/> |
|<span data-ttu-id="0047c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0047c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0047c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0047c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0047c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0047c-112">Area:</span></span>  <br/> |<span data-ttu-id="0047c-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="0047c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0047c-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="0047c-114">Remarks</span></span>

<span data-ttu-id="0047c-115">Diese Eigenschaft ist eine der Adresseigenschaften für den ursprünglichen Absender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0047c-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="0047c-116">Am ersten-Übermittlung der Nachricht sollte eine Clientanwendung diese Eigenschaft auf den Wert der Eigenschaft **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0047c-116">At first submission of the message, a client application should set this property to the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="0047c-117">Es wird nie geändert, wenn die Nachricht weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="0047c-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0047c-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0047c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0047c-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0047c-119">Protocol specifications</span></span>

<span data-ttu-id="0047c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0047c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0047c-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0047c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0047c-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0047c-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0047c-123">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0047c-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0047c-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0047c-124">Header files</span></span>

<span data-ttu-id="0047c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0047c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0047c-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0047c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0047c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0047c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0047c-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0047c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0047c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0047c-129">See also</span></span>



[<span data-ttu-id="0047c-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0047c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0047c-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0047c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0047c-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0047c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0047c-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0047c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

