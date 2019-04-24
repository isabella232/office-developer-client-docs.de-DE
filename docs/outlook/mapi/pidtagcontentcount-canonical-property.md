---
title: Kanonische Pidtagcontentcount (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCount
api_type:
- HeaderDef
ms.assetid: 27c75031-a968-4636-98a6-4a5b7422f57c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7e9994da72bbc38a546f220e5ecf8768b80c6f1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331955"
---
# <a name="pidtagcontentcount-canonical-property"></a><span data-ttu-id="02380-103">Kanonische Pidtagcontentcount (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="02380-103">PidTagContentCount Canonical Property</span></span>

  
  
<span data-ttu-id="02380-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02380-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02380-105">Enthält die Anzahl der Nachrichten in einem Ordner, die vom Nachrichtenspeicher berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="02380-105">Contains the number of messages in a folder, as computed by the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02380-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="02380-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02380-107">PR_CONTENT_COUNT</span><span class="sxs-lookup"><span data-stu-id="02380-107">PR_CONTENT_COUNT</span></span>  <br/> |
|<span data-ttu-id="02380-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="02380-108">Identifier:</span></span>  <br/> |<span data-ttu-id="02380-109">0x3602</span><span class="sxs-lookup"><span data-stu-id="02380-109">0x3602</span></span>  <br/> |
|<span data-ttu-id="02380-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="02380-110">Data type:</span></span>  <br/> |<span data-ttu-id="02380-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="02380-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="02380-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="02380-112">Area:</span></span>  <br/> |<span data-ttu-id="02380-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="02380-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02380-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02380-114">Remarks</span></span>

<span data-ttu-id="02380-115">Diese vom Nachrichtenspeicher berechnete Eigenschaft wird für zwei verschiedene, wenn auch verwandte Zwecke verwendet.</span><span class="sxs-lookup"><span data-stu-id="02380-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="02380-116">In einem MapiFolder-Objekt enthält es die Anzahl der Nachrichten in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="02380-116">On a MapiFolder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="02380-117">In einer Überschriftenzeile in kategorisierten MAPI-Tabellen enthält es die Anzahl der nicht zugeordneten Nachrichten in der Kategorie, die dieser Überschriftenzeile entspricht.</span><span class="sxs-lookup"><span data-stu-id="02380-117">In a heading row in categorized MAPI tables, it contains the number of non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="02380-118">Die in dieser Eigenschaft enthaltene Zahl enthält keine zugeordneten Einträge im Ordner.</span><span class="sxs-lookup"><span data-stu-id="02380-118">The number contained in this property does not include associated entries in the folder.</span></span> <span data-ttu-id="02380-119">**PR_CONTENT_UNREAD** ([Pidtagcontentunreadcount (](pidtagcontentunreadcount-canonical-property.md)) enthält die Anzahl der ungelesenen Nachrichten für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="02380-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contains the count of unread messages for the folder.</span></span> <span data-ttu-id="02380-120">Eine Clientanwendung kann diese Eigenschaft und **PR_CONTENT_UNREAD**lesen, aber nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="02380-120">A client application can read but not change this property and **PR_CONTENT_UNREAD**.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="02380-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="02380-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="02380-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="02380-122">Protocol specifications</span></span>

<span data-ttu-id="02380-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02380-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02380-124">Enthält Verweise auf zugehörige Microsoft Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="02380-124">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="02380-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02380-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02380-126">Behandelt Ordner Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="02380-126">Handles folder operations.</span></span>
    
<span data-ttu-id="02380-127">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02380-127">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02380-128">Enthält zulässige Vorgänge für die Haupttabellen Objekte.</span><span class="sxs-lookup"><span data-stu-id="02380-128">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="02380-129">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="02380-129">Header files</span></span>

<span data-ttu-id="02380-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="02380-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="02380-131">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="02380-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="02380-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="02380-132">Mapitags.h</span></span>
  
> <span data-ttu-id="02380-133">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="02380-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02380-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02380-134">See also</span></span>



[<span data-ttu-id="02380-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02380-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02380-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02380-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02380-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="02380-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02380-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="02380-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

