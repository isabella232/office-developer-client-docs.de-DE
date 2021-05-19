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
ms.openlocfilehash: ec092e6cc6174e156dbfe7784143c9d74715eef7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357701"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a><span data-ttu-id="0e2a7-103">PidTagItemTemporaryflags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0e2a7-103">PidTagItemTemporaryflags Canonical Property</span></span>

  
  
<span data-ttu-id="0e2a7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e2a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e2a7-105">Enthält ein Flag, das angibt, dass eine Nachricht gelesen, aber nicht als gelesen markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0e2a7-105">Contains a flag that indicates that a message has been read, but not marked as read.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e2a7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0e2a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e2a7-107">PR_ITEM_TMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="0e2a7-107">PR_ITEM_TMPFLAGS</span></span>  <br/> |
|<span data-ttu-id="0e2a7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0e2a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e2a7-109">0x1097</span><span class="sxs-lookup"><span data-stu-id="0e2a7-109">0x1097</span></span>  <br/> |
|<span data-ttu-id="0e2a7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0e2a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e2a7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0e2a7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0e2a7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0e2a7-112">Area:</span></span>  <br/> |<span data-ttu-id="0e2a7-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="0e2a7-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e2a7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0e2a7-114">Remarks</span></span>

<span data-ttu-id="0e2a7-115">Diese Eigenschaft wird im Outlook Ordner Ungelesene Nachrichten verwendet, um nachverfolgt zu werden, welche Nachrichten gelesen wurden, ohne sie tatsächlich als gelesen zu kennzeichnen, wodurch sie aus dem Ordner entfernt würden.</span><span class="sxs-lookup"><span data-stu-id="0e2a7-115">This property is used in Outlook's Unread Messages search folder to keep track of which messages have been read without actually marking them as read, which would remove them from the folder.</span></span> <span data-ttu-id="0e2a7-116">Wenn sich die Ansicht ändert, wird diese Eigenschaft entfernt und das Element als gelesen markiert.</span><span class="sxs-lookup"><span data-stu-id="0e2a7-116">When the view changes this property is removed and the item is marked as read.</span></span> <span data-ttu-id="0e2a7-117">Diese Eigenschaft wird nicht mit dem Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0e2a7-117">This property will not synchronize to the Exchange Server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0e2a7-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0e2a7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e2a7-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0e2a7-119">Protocol specifications</span></span>

<span data-ttu-id="0e2a7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e2a7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e2a7-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0e2a7-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e2a7-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e2a7-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e2a7-123">Verarbeitet Ordnervorgänge.</span><span class="sxs-lookup"><span data-stu-id="0e2a7-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e2a7-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="0e2a7-124">Header files</span></span>

<span data-ttu-id="0e2a7-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e2a7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e2a7-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0e2a7-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e2a7-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0e2a7-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0e2a7-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0e2a7-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e2a7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e2a7-129">See also</span></span>



[<span data-ttu-id="0e2a7-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0e2a7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e2a7-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="0e2a7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e2a7-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0e2a7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e2a7-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0e2a7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

