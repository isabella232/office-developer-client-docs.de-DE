---
title: Kanonische PidTagOriginalSenderEmailAddress-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEmailAddress
api_type:
- COM
ms.assetid: cc86505c-e264-435f-ae21-4a10f0bbf082
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 02a057d6382394c947fa1f23c4408ff0ad2339de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794713"
---
# <a name="pidtagoriginalsenderemailaddress-canonical-property"></a><span data-ttu-id="c92a2-103">Kanonische PidTagOriginalSenderEmailAddress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c92a2-103">PidTagOriginalSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="c92a2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c92a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c92a2-105">Enthält die e-Mail-Adresse des Absenders einer Nachricht, d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird die erste Version.</span><span class="sxs-lookup"><span data-stu-id="c92a2-105">Contains the email address of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c92a2-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c92a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c92a2-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="c92a2-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="c92a2-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="c92a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c92a2-109">0x0067</span><span class="sxs-lookup"><span data-stu-id="c92a2-109">0x0067</span></span>  <br/> |
|<span data-ttu-id="c92a2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c92a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="c92a2-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c92a2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c92a2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c92a2-112">Area:</span></span>  <br/> |<span data-ttu-id="c92a2-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="c92a2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c92a2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c92a2-114">Remarks</span></span>

<span data-ttu-id="c92a2-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den ursprünglichen Absender einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c92a2-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="c92a2-116">Am ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaft auf den Wert der **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c92a2-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="c92a2-117">Es wird nie geändert, wenn die Nachricht weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="c92a2-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c92a2-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c92a2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c92a2-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c92a2-119">Protocol specifications</span></span>

<span data-ttu-id="c92a2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c92a2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c92a2-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c92a2-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c92a2-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c92a2-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c92a2-123">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c92a2-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c92a2-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c92a2-124">Header files</span></span>

<span data-ttu-id="c92a2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c92a2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c92a2-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c92a2-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c92a2-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c92a2-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c92a2-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c92a2-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c92a2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c92a2-129">See also</span></span>



[<span data-ttu-id="c92a2-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c92a2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c92a2-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c92a2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c92a2-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c92a2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c92a2-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c92a2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

