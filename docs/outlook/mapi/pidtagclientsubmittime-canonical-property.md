---
title: Kanonische PidTagClientSubmitTime-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ccf4a6054ecc89e280f2f5cbc4c72b2a8a829055
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794164"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="59a9d-103">Kanonische PidTagClientSubmitTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="59a9d-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="59a9d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="59a9d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="59a9d-105">Enthält Datum und Zeit für der Absender eine Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="59a9d-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59a9d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="59a9d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59a9d-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="59a9d-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="59a9d-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="59a9d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="59a9d-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="59a9d-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="59a9d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="59a9d-110">Data type:</span></span>  <br/> |<span data-ttu-id="59a9d-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="59a9d-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="59a9d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="59a9d-112">Area:</span></span>  <br/> |<span data-ttu-id="59a9d-113">Nachrichtzeit</span><span class="sxs-lookup"><span data-stu-id="59a9d-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59a9d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="59a9d-114">Remarks</span></span>

<span data-ttu-id="59a9d-115">Der Anbieter wird **PR_CLIENT_SUBMIT_TIME** auf die Zeit, die die Clientanwendung [IMessage::SubmitMessage](imessage-submitmessage.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="59a9d-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="59a9d-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="59a9d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="59a9d-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="59a9d-117">Protocol specifications</span></span>

<span data-ttu-id="59a9d-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59a9d-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59a9d-119">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="59a9d-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="59a9d-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="59a9d-120">Header files</span></span>

<span data-ttu-id="59a9d-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59a9d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="59a9d-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="59a9d-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="59a9d-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="59a9d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="59a9d-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="59a9d-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59a9d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59a9d-125">See also</span></span>



[<span data-ttu-id="59a9d-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59a9d-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59a9d-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59a9d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59a9d-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="59a9d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59a9d-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="59a9d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

