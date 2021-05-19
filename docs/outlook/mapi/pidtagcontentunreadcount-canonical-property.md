---
title: PidTagContentUnreadCount (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9572a053182aaa59020a6816736b8a4b92e778b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331871"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a><span data-ttu-id="73c2e-103">PidTagContentUnreadCount (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="73c2e-103">PidTagContentUnreadCount Canonical Property</span></span>

  
  
<span data-ttu-id="73c2e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73c2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73c2e-105">Enthält die Anzahl ungelesener Nachrichten in einem Ordner, wie vom Nachrichtenspeicher berechnet.</span><span class="sxs-lookup"><span data-stu-id="73c2e-105">Contains the number of unread messages in a folder, as computed by the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73c2e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="73c2e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73c2e-107">PR_CONTENT_UNREAD</span><span class="sxs-lookup"><span data-stu-id="73c2e-107">PR_CONTENT_UNREAD</span></span>  <br/> |
|<span data-ttu-id="73c2e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="73c2e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="73c2e-109">0x3603</span><span class="sxs-lookup"><span data-stu-id="73c2e-109">0x3603</span></span>  <br/> |
|<span data-ttu-id="73c2e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="73c2e-110">Data type:</span></span>  <br/> |<span data-ttu-id="73c2e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="73c2e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="73c2e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="73c2e-112">Area:</span></span>  <br/> |<span data-ttu-id="73c2e-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="73c2e-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73c2e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="73c2e-114">Remarks</span></span>

<span data-ttu-id="73c2e-115">Diese vom Nachrichtenspeicher berechnete Eigenschaft wird für zwei unterschiedliche, wenngleich verwandte Zwecke verwendet.</span><span class="sxs-lookup"><span data-stu-id="73c2e-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="73c2e-116">In einem MAPI-Ordnerobjekt enthält es die Anzahl der Nachrichten in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="73c2e-116">On a MAPI folder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="73c2e-117">In einer Überschriftenzeile in kategorisierten MAPI-Tabellen enthält sie die Anzahl nicht gelesener nicht zugeordneter Nachrichten in der Kategorie, die dieser Überschriftenzeile entspricht.</span><span class="sxs-lookup"><span data-stu-id="73c2e-117">In a heading row in categorized MAPI tables, it contains the number of unread non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="73c2e-118">Diese Eigenschaft enthält die Anzahl der Nachrichten in der Ordnerinhaltstabelle, für die das flag MSGFLAG_READ in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73c2e-118">This property contains the number of messages in the folder contents table for which the MSGFLAG_READ flag is not set in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="73c2e-119">Die **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) -Eigenschaft enthält die Gesamtanzahl der Nachrichten für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="73c2e-119">The **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) property contains the total message count for the folder.</span></span> <span data-ttu-id="73c2e-120">Die **PR_CONTENT_COUNT** und diese Eigenschaft sind schreibgeschützt für Clients.</span><span class="sxs-lookup"><span data-stu-id="73c2e-120">The **PR_CONTENT_COUNT** and this property are read-only to clients.</span></span> 
  
<span data-ttu-id="73c2e-121">Einige Clientanwendungen zeigen die Überschriftenzeile einer Kategorie abhängig vom Wert dieser Eigenschaft unterschiedlich an.</span><span class="sxs-lookup"><span data-stu-id="73c2e-121">Some client applications display the heading row of a category differently depending on the value of this property.</span></span> <span data-ttu-id="73c2e-122">Ein Client kann beispielsweise eine Kategorie anzeigen, die ungelesene Nachrichten fett formatiert enthält.</span><span class="sxs-lookup"><span data-stu-id="73c2e-122">For example, a client can display a category that includes unread messages in bold.</span></span> <span data-ttu-id="73c2e-123">Diese Eigenschaft kann nicht als Kategorie verwendet werden, und ein Versuch dazu führt dazu, dass der MAPI_E_INVALID_PARAMETER von der [IMAPITable::SortTable-Methode zurückgegeben](imapitable-sorttable.md) wird.</span><span class="sxs-lookup"><span data-stu-id="73c2e-123">This property cannot be used as a category and an attempt to do so results in the MAPI_E_INVALID_PARAMETER value being returned from the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="73c2e-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="73c2e-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="73c2e-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="73c2e-125">Protocol specifications</span></span>

<span data-ttu-id="73c2e-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73c2e-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73c2e-127">Enthält Verweise auf Microsoft Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="73c2e-127">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="73c2e-128">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73c2e-128">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73c2e-129">Verarbeitet Ordnervorgänge.</span><span class="sxs-lookup"><span data-stu-id="73c2e-129">Handles folder operations.</span></span>
    
<span data-ttu-id="73c2e-130">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73c2e-130">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73c2e-131">Enthält zulässige Vorgänge für die Zentralen Tabellenobjekte.</span><span class="sxs-lookup"><span data-stu-id="73c2e-131">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="73c2e-132">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="73c2e-132">Header files</span></span>

<span data-ttu-id="73c2e-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73c2e-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="73c2e-134">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="73c2e-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="73c2e-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="73c2e-135">Mapitags.h</span></span>
  
> <span data-ttu-id="73c2e-136">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="73c2e-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73c2e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73c2e-137">See also</span></span>



[<span data-ttu-id="73c2e-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73c2e-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73c2e-139">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="73c2e-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73c2e-140">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="73c2e-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73c2e-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="73c2e-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

