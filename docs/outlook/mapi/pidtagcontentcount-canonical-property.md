---
title: PidTagContentCount (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b489e73f9453e5d2ae6657969c2bc18fc9a4620e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562939"
---
# <a name="pidtagcontentcount-canonical-property"></a><span data-ttu-id="4dea4-103">PidTagContentCount (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4dea4-103">PidTagContentCount Canonical Property</span></span>

  
  
<span data-ttu-id="4dea4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4dea4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4dea4-105">Die Anzahl der Nachrichten in einem Ordner enthält, wie Sie mithilfe des Nachrichtenspeichers berechnet.</span><span class="sxs-lookup"><span data-stu-id="4dea4-105">Contains the number of messages in a folder, as computed by the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4dea4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4dea4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4dea4-107">PR_CONTENT_COUNT</span><span class="sxs-lookup"><span data-stu-id="4dea4-107">PR_CONTENT_COUNT</span></span>  <br/> |
|<span data-ttu-id="4dea4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4dea4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4dea4-109">0x3602</span><span class="sxs-lookup"><span data-stu-id="4dea4-109">0x3602</span></span>  <br/> |
|<span data-ttu-id="4dea4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4dea4-110">Data type:</span></span>  <br/> |<span data-ttu-id="4dea4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4dea4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4dea4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4dea4-112">Area:</span></span>  <br/> |<span data-ttu-id="4dea4-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="4dea4-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4dea4-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4dea4-114">Remarks</span></span>

<span data-ttu-id="4dea4-115">Diese Eigenschaft von der Nachrichtenspeicher berechnet wird für zwei unterschiedliche, obwohl verbunden, Zwecke.</span><span class="sxs-lookup"><span data-stu-id="4dea4-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="4dea4-116">Für ein MapiFolder-Objekt enthält sie die Anzahl der Nachrichten in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="4dea4-116">On a MapiFolder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="4dea4-117">In eine Überschriftenzeile in kategorisierten MAPI-Tabellen enthält sie die Anzahl der Nachrichten in der Kategorie dieser Überschriftenzeile entsprechendes-verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="4dea4-117">In a heading row in categorized MAPI tables, it contains the number of non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="4dea4-118">Die Zahl in dieser Eigenschaft enthaltenen umfasst nicht zugeordnete Einträge im Ordner.</span><span class="sxs-lookup"><span data-stu-id="4dea4-118">The number contained in this property does not include associated entries in the folder.</span></span> <span data-ttu-id="4dea4-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) enthält die Anzahl der ungelesenen Nachrichten für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="4dea4-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contains the count of unread messages for the folder.</span></span> <span data-ttu-id="4dea4-120">Eine Clientanwendung kann gelesen, aber nicht geändert werden, diese Eigenschaft und die **PR_CONTENT_UNREAD**.</span><span class="sxs-lookup"><span data-stu-id="4dea4-120">A client application can read but not change this property and **PR_CONTENT_UNREAD**.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4dea4-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4dea4-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4dea4-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4dea4-122">Protocol specifications</span></span>

<span data-ttu-id="4dea4-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dea4-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dea4-124">Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="4dea4-124">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4dea4-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dea4-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dea4-126">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="4dea4-126">Handles folder operations.</span></span>
    
<span data-ttu-id="4dea4-127">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dea4-127">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dea4-128">Zulässige Vorgänge für die Hauptobjekte-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="4dea4-128">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4dea4-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4dea4-129">Header files</span></span>

<span data-ttu-id="4dea4-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4dea4-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="4dea4-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4dea4-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="4dea4-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4dea4-132">Mapitags.h</span></span>
  
> <span data-ttu-id="4dea4-133">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4dea4-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4dea4-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4dea4-134">See also</span></span>



[<span data-ttu-id="4dea4-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4dea4-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4dea4-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4dea4-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4dea4-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4dea4-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4dea4-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4dea4-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

