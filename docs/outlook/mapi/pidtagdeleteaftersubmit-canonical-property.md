---
title: Kanonische PidTagDeleteAfterSubmit-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeleteAfterSubmit
api_type:
- HeaderDef
ms.assetid: ba69a557-120c-4b1e-bbb7-0e901e7d1ebf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7a63b3ad3c45790e043e1ea8e7d996c4847ef8d4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794287"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a><span data-ttu-id="7cd79-103">Kanonische PidTagDeleteAfterSubmit-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7cd79-103">PidTagDeleteAfterSubmit Canonical Property</span></span>

  
  
<span data-ttu-id="7cd79-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7cd79-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7cd79-105">Enthält True, wenn eine Clientanwendung MAPI, um die zugehörige Meldung nach der Übermittlung löschen möchte.</span><span class="sxs-lookup"><span data-stu-id="7cd79-105">Contains TRUE if a client application wants MAPI to delete the associated message after submission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7cd79-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7cd79-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7cd79-107">PR_DELETE_AFTER_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="7cd79-107">PR_DELETE_AFTER_SUBMIT</span></span>  <br/> |
|<span data-ttu-id="7cd79-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="7cd79-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7cd79-109">0x0E01</span><span class="sxs-lookup"><span data-stu-id="7cd79-109">0x0E01</span></span>  <br/> |
|<span data-ttu-id="7cd79-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7cd79-110">Data type:</span></span>  <br/> |<span data-ttu-id="7cd79-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7cd79-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7cd79-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7cd79-112">Area:</span></span>  <br/> |<span data-ttu-id="7cd79-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="7cd79-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7cd79-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7cd79-114">Remarks</span></span>

<span data-ttu-id="7cd79-115">Eine Clientanwendung verwendet diese Eigenschaft mit der **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))-Eigenschaft steuern, was geschieht mit einer Meldung, nachdem es gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="7cd79-115">A client application uses this property with the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="7cd79-116">Eine oder die andere sollte Set, jedoch nicht beide.</span><span class="sxs-lookup"><span data-stu-id="7cd79-116">Either one or the other should be set, but not both.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7cd79-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7cd79-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7cd79-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7cd79-118">Protocol specifications</span></span>

<span data-ttu-id="7cd79-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cd79-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cd79-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7cd79-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7cd79-121">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cd79-121">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cd79-122">Gibt die zulässige Vorgänge für die Hauptobjekte der Nachricht Store.</span><span class="sxs-lookup"><span data-stu-id="7cd79-122">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="7cd79-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cd79-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cd79-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7cd79-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7cd79-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7cd79-125">Header files</span></span>

<span data-ttu-id="7cd79-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7cd79-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7cd79-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7cd79-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7cd79-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7cd79-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7cd79-129">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7cd79-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7cd79-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cd79-130">See also</span></span>



[<span data-ttu-id="7cd79-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7cd79-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7cd79-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7cd79-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7cd79-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7cd79-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7cd79-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7cd79-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

