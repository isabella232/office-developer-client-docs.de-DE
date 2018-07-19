---
title: PidTagItemTemporaryflags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagItemTemporaryflags
api_type:
- HeaderDef
ms.assetid: 8066de8e-2b77-4bac-8df3-e64b03ee42b9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: df2fa19656aa1bff810a082cda94a091e2c7fc9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794544"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a><span data-ttu-id="03cbc-103">PidTagItemTemporaryflags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="03cbc-103">PidTagItemTemporaryflags Canonical Property</span></span>

  
  
<span data-ttu-id="03cbc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03cbc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03cbc-105">Enthält ein Flag, das angibt, dass eine Nachricht lesen, aber nicht als gelesen markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="03cbc-105">Contains a flag that indicates that a message has been read, but not marked as read.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03cbc-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="03cbc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03cbc-107">PR_ITEM_TMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="03cbc-107">PR_ITEM_TMPFLAGS</span></span>  <br/> |
|<span data-ttu-id="03cbc-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="03cbc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03cbc-109">0x1097</span><span class="sxs-lookup"><span data-stu-id="03cbc-109">0x1097</span></span>  <br/> |
|<span data-ttu-id="03cbc-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="03cbc-110">Data type:</span></span>  <br/> |<span data-ttu-id="03cbc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="03cbc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="03cbc-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="03cbc-112">Area:</span></span>  <br/> |<span data-ttu-id="03cbc-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="03cbc-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03cbc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03cbc-114">Remarks</span></span>

<span data-ttu-id="03cbc-115">Diese Eigenschaft wird in Outlook ungelesene Nachrichten Suchordner verwendet, um verfolgen an welche Nachrichten gelesen wurden, ohne tatsächlich markieren als gelesen, die sie aus dem Ordner entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="03cbc-115">This property is used in Outlook's Unread Messages search folder to keep track of which messages have been read without actually marking them as read, which would remove them from the folder.</span></span> <span data-ttu-id="03cbc-116">Wenn die Ansicht geändert wird, den diese Eigenschaft entfernt ist und das Element wird als gekennzeichnet lesen.</span><span class="sxs-lookup"><span data-stu-id="03cbc-116">When the view changes this property is removed and the item is marked as read.</span></span> <span data-ttu-id="03cbc-117">Diese Eigenschaft wird nicht mit dem Exchange Server synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="03cbc-117">This property will not synchronize to the Exchange Server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="03cbc-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="03cbc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03cbc-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="03cbc-119">Protocol specifications</span></span>

<span data-ttu-id="03cbc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03cbc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03cbc-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="03cbc-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03cbc-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03cbc-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03cbc-123">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="03cbc-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03cbc-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="03cbc-124">Header files</span></span>

<span data-ttu-id="03cbc-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03cbc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="03cbc-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="03cbc-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="03cbc-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="03cbc-127">Mapitags.h</span></span>
  
> <span data-ttu-id="03cbc-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="03cbc-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03cbc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03cbc-129">See also</span></span>



[<span data-ttu-id="03cbc-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03cbc-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03cbc-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03cbc-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03cbc-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="03cbc-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03cbc-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="03cbc-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

