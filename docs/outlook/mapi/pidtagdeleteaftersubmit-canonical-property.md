---
title: PidTagDeleteAfterSubmit (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2708d89e2572e8820de0b525b4f53ccd309ae2a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359913"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a><span data-ttu-id="dded8-103">PidTagDeleteAfterSubmit (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dded8-103">PidTagDeleteAfterSubmit Canonical Property</span></span>

  
  
<span data-ttu-id="dded8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dded8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dded8-105">Enthält TRUE, wenn eine Clientanwendung möchte, dass MAPI die zugeordnete Nachricht nach der Übermittlung löscht.</span><span class="sxs-lookup"><span data-stu-id="dded8-105">Contains TRUE if a client application wants MAPI to delete the associated message after submission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dded8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dded8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dded8-107">PR_DELETE_AFTER_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="dded8-107">PR_DELETE_AFTER_SUBMIT</span></span>  <br/> |
|<span data-ttu-id="dded8-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="dded8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dded8-109">0x0E01</span><span class="sxs-lookup"><span data-stu-id="dded8-109">0x0E01</span></span>  <br/> |
|<span data-ttu-id="dded8-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dded8-110">Data type:</span></span>  <br/> |<span data-ttu-id="dded8-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="dded8-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="dded8-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dded8-112">Area:</span></span>  <br/> |<span data-ttu-id="dded8-113">MAPI nicht durchlässig</span><span class="sxs-lookup"><span data-stu-id="dded8-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dded8-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dded8-114">Remarks</span></span>

<span data-ttu-id="dded8-115">Eine Clientanwendung verwendet diese Eigenschaft mit der **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) -Eigenschaft, um zu steuern, was mit einer Nachricht nach dem Senden geschieht.</span><span class="sxs-lookup"><span data-stu-id="dded8-115">A client application uses this property with the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="dded8-116">Entweder die eine oder die andere sollte festgelegt werden, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="dded8-116">Either one or the other should be set, but not both.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dded8-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dded8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dded8-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="dded8-118">Protocol specifications</span></span>

<span data-ttu-id="dded8-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dded8-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dded8-120">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="dded8-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dded8-121">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dded8-121">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dded8-122">Gibt zulässige Vorgänge für die Zentralen Nachrichtenspeicherobjekte an.</span><span class="sxs-lookup"><span data-stu-id="dded8-122">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="dded8-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dded8-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dded8-124">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="dded8-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dded8-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="dded8-125">Header files</span></span>

<span data-ttu-id="dded8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dded8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="dded8-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="dded8-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="dded8-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dded8-128">Mapitags.h</span></span>
  
> <span data-ttu-id="dded8-129">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="dded8-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dded8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dded8-130">See also</span></span>



[<span data-ttu-id="dded8-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dded8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dded8-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="dded8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dded8-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dded8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dded8-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dded8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

