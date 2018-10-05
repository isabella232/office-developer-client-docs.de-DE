---
title: PidTagInReplyToId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInReplyToId
api_type:
- HeaderDef
ms.assetid: d435a65a-de01-4fb0-bc54-a87a2c4462ac
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 036f38c1228e08cfc9a2093c027195a802904f19
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392172"
---
# <a name="pidtaginreplytoid-canonical-property"></a><span data-ttu-id="26337-103">PidTagInReplyToId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="26337-103">PidTagInReplyToId Canonical Property</span></span>

  
  
<span data-ttu-id="26337-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26337-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26337-105">Enthält die ursprüngliche Nachricht **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md))-Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="26337-105">Contains the original message's **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) property value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="26337-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="26337-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="26337-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span><span class="sxs-lookup"><span data-stu-id="26337-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span></span>  <br/> |
|<span data-ttu-id="26337-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="26337-108">Identifier:</span></span>  <br/> |<span data-ttu-id="26337-109">0x1042</span><span class="sxs-lookup"><span data-stu-id="26337-109">0x1042</span></span>  <br/> |
|<span data-ttu-id="26337-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="26337-110">Data type:</span></span>  <br/> |<span data-ttu-id="26337-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="26337-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="26337-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="26337-112">Area:</span></span>  <br/> |<span data-ttu-id="26337-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="26337-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26337-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="26337-114">Remarks</span></span>

<span data-ttu-id="26337-115">Diese Eigenschaften müssen auf allen Antworten auf Nachrichten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="26337-115">These properties must be set on all message replies.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="26337-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="26337-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="26337-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="26337-117">Protocol specifications</span></span>

<span data-ttu-id="26337-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26337-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26337-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="26337-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="26337-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26337-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26337-121">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="26337-121">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="26337-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26337-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26337-123">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="26337-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="26337-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="26337-124">Header files</span></span>

<span data-ttu-id="26337-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26337-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="26337-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="26337-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="26337-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="26337-127">Mapitags.h</span></span>
  
> <span data-ttu-id="26337-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="26337-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26337-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26337-129">See also</span></span>



[<span data-ttu-id="26337-130">PidTagInternetMessageId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="26337-130">PidTagInternetMessageId Canonical Property</span></span>](pidtaginternetmessageid-canonical-property.md)


[<span data-ttu-id="26337-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26337-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="26337-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26337-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="26337-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="26337-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="26337-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="26337-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

