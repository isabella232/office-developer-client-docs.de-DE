---
title: Kanonische PidTagContentCount-Eigenschaft
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
ms.openlocfilehash: 3c542b07eac626da5fbbb6a96b4545ad3c8558b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794241"
---
# <a name="pidtagcontentcount-canonical-property"></a><span data-ttu-id="cebb3-103">Kanonische PidTagContentCount-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cebb3-103">PidTagContentCount Canonical Property</span></span>

  
  
<span data-ttu-id="cebb3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cebb3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cebb3-105">Die Anzahl der Nachrichten in einem Ordner enthält, wie Sie mithilfe des Nachrichtenspeichers berechnet.</span><span class="sxs-lookup"><span data-stu-id="cebb3-105">Contains the number of messages in a folder, as computed by the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cebb3-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cebb3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cebb3-107">PR_CONTENT_COUNT</span><span class="sxs-lookup"><span data-stu-id="cebb3-107">PR_CONTENT_COUNT</span></span>  <br/> |
|<span data-ttu-id="cebb3-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="cebb3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cebb3-109">0x3602</span><span class="sxs-lookup"><span data-stu-id="cebb3-109">0x3602</span></span>  <br/> |
|<span data-ttu-id="cebb3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cebb3-110">Data type:</span></span>  <br/> |<span data-ttu-id="cebb3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cebb3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cebb3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cebb3-112">Area:</span></span>  <br/> |<span data-ttu-id="cebb3-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="cebb3-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cebb3-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cebb3-114">Remarks</span></span>

<span data-ttu-id="cebb3-115">Diese Eigenschaft von der Nachrichtenspeicher berechnet wird für zwei unterschiedliche, obwohl verbunden, Zwecke.</span><span class="sxs-lookup"><span data-stu-id="cebb3-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="cebb3-116">Für ein MapiFolder-Objekt enthält sie die Anzahl der Nachrichten in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="cebb3-116">On a MapiFolder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="cebb3-117">In eine Überschriftenzeile in kategorisierten MAPI-Tabellen enthält sie die Anzahl der Nachrichten in der Kategorie dieser Überschriftenzeile entsprechendes-verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="cebb3-117">In a heading row in categorized MAPI tables, it contains the number of non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="cebb3-118">Die Zahl in dieser Eigenschaft enthaltenen umfasst nicht zugeordnete Einträge im Ordner.</span><span class="sxs-lookup"><span data-stu-id="cebb3-118">The number contained in this property does not include associated entries in the folder.</span></span> <span data-ttu-id="cebb3-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) enthält die Anzahl der ungelesenen Nachrichten für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="cebb3-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contains the count of unread messages for the folder.</span></span> <span data-ttu-id="cebb3-120">Eine Clientanwendung kann gelesen, aber nicht geändert werden, diese Eigenschaft und die **PR_CONTENT_UNREAD**.</span><span class="sxs-lookup"><span data-stu-id="cebb3-120">A client application can read but not change this property and **PR_CONTENT_UNREAD**.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cebb3-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cebb3-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cebb3-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cebb3-122">Protocol specifications</span></span>

<span data-ttu-id="cebb3-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cebb3-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cebb3-124">Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="cebb3-124">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cebb3-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cebb3-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cebb3-126">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="cebb3-126">Handles folder operations.</span></span>
    
<span data-ttu-id="cebb3-127">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cebb3-127">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cebb3-128">Zulässige Vorgänge für die Hauptobjekte-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="cebb3-128">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cebb3-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="cebb3-129">Header files</span></span>

<span data-ttu-id="cebb3-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cebb3-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="cebb3-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="cebb3-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="cebb3-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cebb3-132">Mapitags.h</span></span>
  
> <span data-ttu-id="cebb3-133">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cebb3-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cebb3-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cebb3-134">See also</span></span>



[<span data-ttu-id="cebb3-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cebb3-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cebb3-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cebb3-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cebb3-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cebb3-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cebb3-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cebb3-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
