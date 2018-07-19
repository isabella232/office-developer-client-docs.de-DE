---
title: PidTagResponseRequested (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponseRequested
api_type:
- COM
ms.assetid: e52bb48c-7107-4ac4-b030-885409759ee7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b099bf5df657b5516fbf0948e742d1d1b36af2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794978"
---
# <a name="pidtagresponserequested-canonical-property"></a><span data-ttu-id="c4ca5-103">PidTagResponseRequested (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c4ca5-103">PidTagResponseRequested Canonical Property</span></span>

  
  
<span data-ttu-id="c4ca5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4ca5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4ca5-105">Enthält True, wenn der Absender der Nachricht eine Antwort auf eine Besprechungsanfrage möchte.</span><span class="sxs-lookup"><span data-stu-id="c4ca5-105">Contains TRUE if the message sender wants a response to a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4ca5-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c4ca5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4ca5-107">PR_RESPONSE_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="c4ca5-107">PR_RESPONSE_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="c4ca5-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="c4ca5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c4ca5-109">0x0063</span><span class="sxs-lookup"><span data-stu-id="c4ca5-109">0x0063</span></span>  <br/> |
|<span data-ttu-id="c4ca5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c4ca5-110">Data type:</span></span>  <br/> |<span data-ttu-id="c4ca5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c4ca5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c4ca5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c4ca5-112">Area:</span></span>  <br/> |<span data-ttu-id="c4ca5-113">MAPI-Umschlag</span><span class="sxs-lookup"><span data-stu-id="c4ca5-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4ca5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4ca5-114">Remarks</span></span>

<span data-ttu-id="c4ca5-115">Diese Eigenschaft wird für Besprechungsanfragen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4ca5-115">This property is used for meeting requests.</span></span> <span data-ttu-id="c4ca5-116">Die empfangenden Clientanwendung sollte der Benutzer aufgefordert, akzeptieren oder Ablehnen der Anforderung und senden Sie diese Antwort an den Absender zurückgesendet.</span><span class="sxs-lookup"><span data-stu-id="c4ca5-116">The receiving client application should prompt the user to accept or decline the request and then send this response back to the sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c4ca5-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c4ca5-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4ca5-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c4ca5-118">Protocol specifications</span></span>

<span data-ttu-id="c4ca5-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4ca5-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4ca5-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c4ca5-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c4ca5-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4ca5-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4ca5-122">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c4ca5-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="c4ca5-123">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4ca5-123">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4ca5-124">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="c4ca5-124">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="c4ca5-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4ca5-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4ca5-126">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="c4ca5-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4ca5-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c4ca5-127">Header files</span></span>

<span data-ttu-id="c4ca5-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4ca5-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4ca5-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c4ca5-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="c4ca5-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c4ca5-130">Mapitags.h</span></span>
  
> <span data-ttu-id="c4ca5-131">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c4ca5-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4ca5-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4ca5-132">See also</span></span>



[<span data-ttu-id="c4ca5-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4ca5-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4ca5-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4ca5-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4ca5-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c4ca5-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4ca5-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c4ca5-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

