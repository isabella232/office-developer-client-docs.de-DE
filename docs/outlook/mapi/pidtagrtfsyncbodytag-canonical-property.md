---
title: PidTagRtfSyncBodyTag (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyTag
api_type:
- COM
ms.assetid: 2dab5018-4214-4162-93bc-e5565f3ac24c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 24ef1d4e3e936426aea8216119e8ada9f6122e95
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387510"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a><span data-ttu-id="ab1b8-103">PidTagRtfSyncBodyTag (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ab1b8-103">PidTagRtfSyncBodyTag Canonical Property</span></span>

  
  
<span data-ttu-id="ab1b8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab1b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab1b8-105">Enthält wesentliche Zeichen, die am Anfang des den Nachrichtentext angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ab1b8-105">Contains significant characters that appear at the beginning of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ab1b8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ab1b8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab1b8-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span><span class="sxs-lookup"><span data-stu-id="ab1b8-107">PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W</span></span>  <br/> |
|<span data-ttu-id="ab1b8-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ab1b8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab1b8-109">0x1008</span><span class="sxs-lookup"><span data-stu-id="ab1b8-109">0x1008</span></span>  <br/> |
|<span data-ttu-id="ab1b8-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ab1b8-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab1b8-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ab1b8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ab1b8-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ab1b8-112">Area:</span></span>  <br/> |<span data-ttu-id="ab1b8-113">MAPI-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ab1b8-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab1b8-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ab1b8-114">Remarks</span></span>

<span data-ttu-id="ab1b8-115">Die [RTFSync](rtfsync.md) -Funktion verwendet die Tags für Text an den Anfang des Nachrichtentexts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ab1b8-115">The [RTFSync](rtfsync.md) function uses the text tag to indicate the beginning of the message text.</span></span> <span data-ttu-id="ab1b8-116">Wenn der Text geändert wird, wird das Tag verwendet, um den Anfang der vorherigen Text zu finden.</span><span class="sxs-lookup"><span data-stu-id="ab1b8-116">When the text is modified, the tag is used to find the beginning of the previous text.</span></span> 
  
<span data-ttu-id="ab1b8-117">Diese Eigenschaften sind zusätzliche Eigenschaften von Rich-Text-Format.</span><span class="sxs-lookup"><span data-stu-id="ab1b8-117">These properties are Rich Text Format auxiliary properties.</span></span> <span data-ttu-id="ab1b8-118">Sie werden von der Funktion **RTFSync** verwendet und nicht direkt von Clientanwendungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ab1b8-118">They are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ab1b8-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ab1b8-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab1b8-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ab1b8-120">Protocol specifications</span></span>

<span data-ttu-id="ab1b8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab1b8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab1b8-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ab1b8-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ab1b8-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab1b8-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab1b8-124">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="ab1b8-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab1b8-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ab1b8-125">Header files</span></span>

<span data-ttu-id="ab1b8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab1b8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab1b8-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ab1b8-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab1b8-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ab1b8-128">Mapitags.h</span></span>
  
> <span data-ttu-id="ab1b8-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ab1b8-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab1b8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab1b8-130">See also</span></span>



[<span data-ttu-id="ab1b8-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab1b8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab1b8-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab1b8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab1b8-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ab1b8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab1b8-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ab1b8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

