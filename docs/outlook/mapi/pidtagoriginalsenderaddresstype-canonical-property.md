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
ms.openlocfilehash: ba0d68482c06a1f6d9ccdae95f63e980a1fd23e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563744"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a><span data-ttu-id="66130-103">PidTagOriginalSenderAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="66130-103">PidTagOriginalSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="66130-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66130-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66130-105">Enthält den Adresstyp des Absenders einer Nachricht, d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird die erste Version.</span><span class="sxs-lookup"><span data-stu-id="66130-105">Contains the address type of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66130-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="66130-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66130-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="66130-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="66130-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="66130-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66130-109">0 x 0066</span><span class="sxs-lookup"><span data-stu-id="66130-109">0x0066</span></span>  <br/> |
|<span data-ttu-id="66130-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="66130-110">Data type:</span></span>  <br/> |<span data-ttu-id="66130-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="66130-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="66130-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="66130-112">Area:</span></span>  <br/> |<span data-ttu-id="66130-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="66130-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66130-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="66130-114">Remarks</span></span>

<span data-ttu-id="66130-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den ursprünglichen Absender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="66130-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="66130-116">Am ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaften auf den Wert der **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="66130-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span></span> <span data-ttu-id="66130-117">Es wird nie geändert, wenn die Nachricht weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="66130-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="66130-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="66130-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66130-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="66130-119">Protocol specifications</span></span>

<span data-ttu-id="66130-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66130-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66130-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="66130-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="66130-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66130-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66130-123">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="66130-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="66130-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="66130-124">Header files</span></span>

<span data-ttu-id="66130-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66130-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="66130-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="66130-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="66130-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="66130-127">Mapitags.h</span></span>
  
> <span data-ttu-id="66130-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="66130-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66130-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66130-129">See also</span></span>



[<span data-ttu-id="66130-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="66130-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66130-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="66130-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66130-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="66130-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66130-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="66130-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

