---
title: PidTagInternetMessageId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetMessageId
api_type:
- HeaderDef
ms.assetid: 5c93d00c-a199-4d45-9bf6-87bd2ffe4784
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7b0af907fd5346de5b818c9c75a3d115e598b5e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794506"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="bade9-103">PidTagInternetMessageId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bade9-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="bade9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bade9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bade9-105">Im Feld Meldung ID gemäß [RFC2822] entspricht.</span><span class="sxs-lookup"><span data-stu-id="bade9-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bade9-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bade9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bade9-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="bade9-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="bade9-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="bade9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bade9-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="bade9-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="bade9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bade9-110">Data type:</span></span>  <br/> |<span data-ttu-id="bade9-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bade9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bade9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bade9-112">Area:</span></span>  <br/> |<span data-ttu-id="bade9-113">MIME</span><span class="sxs-lookup"><span data-stu-id="bade9-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bade9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bade9-114">Remarks</span></span>

<span data-ttu-id="bade9-115">Diese Eigenschaften sollten für alle e-Mail-Nachrichten vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="bade9-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bade9-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bade9-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bade9-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bade9-117">Protocol specifications</span></span>

<span data-ttu-id="bade9-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bade9-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bade9-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bade9-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bade9-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bade9-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bade9-121">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bade9-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bade9-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bade9-122">Header files</span></span>

<span data-ttu-id="bade9-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bade9-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="bade9-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bade9-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="bade9-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bade9-125">Mapitags.h</span></span>
  
> <span data-ttu-id="bade9-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bade9-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bade9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bade9-127">See also</span></span>



[<span data-ttu-id="bade9-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bade9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bade9-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bade9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bade9-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bade9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bade9-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bade9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

