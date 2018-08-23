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
ms.openlocfilehash: e8bed42ee44e48540df52e806c7113e02b60cd07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593634"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a><span data-ttu-id="d7e43-103">PidTagItemTemporaryflags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d7e43-103">PidTagItemTemporaryflags Canonical Property</span></span>

  
  
<span data-ttu-id="d7e43-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7e43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7e43-105">Enthält ein Flag, das angibt, dass eine Nachricht lesen, aber nicht als gelesen markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d7e43-105">Contains a flag that indicates that a message has been read, but not marked as read.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7e43-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d7e43-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7e43-107">PR_ITEM_TMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="d7e43-107">PR_ITEM_TMPFLAGS</span></span>  <br/> |
|<span data-ttu-id="d7e43-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d7e43-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7e43-109">0x1097</span><span class="sxs-lookup"><span data-stu-id="d7e43-109">0x1097</span></span>  <br/> |
|<span data-ttu-id="d7e43-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d7e43-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7e43-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d7e43-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d7e43-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d7e43-112">Area:</span></span>  <br/> |<span data-ttu-id="d7e43-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="d7e43-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7e43-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="d7e43-114">Remarks</span></span>

<span data-ttu-id="d7e43-115">Diese Eigenschaft wird in Outlook ungelesene Nachrichten Suchordner verwendet, um verfolgen an welche Nachrichten gelesen wurden, ohne tatsächlich markieren als gelesen, die sie aus dem Ordner entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="d7e43-115">This property is used in Outlook's Unread Messages search folder to keep track of which messages have been read without actually marking them as read, which would remove them from the folder.</span></span> <span data-ttu-id="d7e43-116">Wenn die Ansicht geändert wird, den diese Eigenschaft entfernt ist und das Element wird als gekennzeichnet lesen.</span><span class="sxs-lookup"><span data-stu-id="d7e43-116">When the view changes this property is removed and the item is marked as read.</span></span> <span data-ttu-id="d7e43-117">Diese Eigenschaft wird nicht mit dem Exchange Server synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="d7e43-117">This property will not synchronize to the Exchange Server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d7e43-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d7e43-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d7e43-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d7e43-119">Protocol specifications</span></span>

<span data-ttu-id="d7e43-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7e43-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7e43-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d7e43-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d7e43-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7e43-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7e43-123">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="d7e43-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d7e43-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d7e43-124">Header files</span></span>

<span data-ttu-id="d7e43-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7e43-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7e43-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d7e43-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7e43-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7e43-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d7e43-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d7e43-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7e43-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7e43-129">See also</span></span>



[<span data-ttu-id="d7e43-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7e43-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7e43-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7e43-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7e43-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d7e43-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7e43-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d7e43-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

