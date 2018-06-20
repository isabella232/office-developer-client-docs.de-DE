---
title: Kanonische PidTagContentUnreadCount-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ce7092840037345ae99b31c39cfbd4ac96b99ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794247"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a><span data-ttu-id="45d70-103">Kanonische PidTagContentUnreadCount-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="45d70-103">PidTagContentUnreadCount Canonical Property</span></span>

  
  
<span data-ttu-id="45d70-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45d70-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45d70-105">Die Anzahl der ungelesenen Nachrichten in einem Ordner enthält, wie Sie mithilfe des Nachrichtenspeichers berechnet.</span><span class="sxs-lookup"><span data-stu-id="45d70-105">Contains the number of unread messages in a folder, as computed by the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45d70-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="45d70-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45d70-107">PR_CONTENT_UNREAD</span><span class="sxs-lookup"><span data-stu-id="45d70-107">PR_CONTENT_UNREAD</span></span>  <br/> |
|<span data-ttu-id="45d70-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="45d70-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45d70-109">0x3603</span><span class="sxs-lookup"><span data-stu-id="45d70-109">0x3603</span></span>  <br/> |
|<span data-ttu-id="45d70-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="45d70-110">Data type:</span></span>  <br/> |<span data-ttu-id="45d70-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="45d70-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="45d70-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="45d70-112">Area:</span></span>  <br/> |<span data-ttu-id="45d70-113">Ordner</span><span class="sxs-lookup"><span data-stu-id="45d70-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45d70-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45d70-114">Remarks</span></span>

<span data-ttu-id="45d70-115">Diese Eigenschaft von der Nachrichtenspeicher berechnet wird für zwei unterschiedliche, obwohl verbunden, Zwecke.</span><span class="sxs-lookup"><span data-stu-id="45d70-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="45d70-116">Auf ein MAPI-Folder-Objekt enthält sie die Anzahl der Nachrichten in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="45d70-116">On a MAPI folder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="45d70-117">In eine Überschriftenzeile in kategorisierten MAPI-Tabellen enthält sie die Anzahl der ungelesenen nicht zugeordneten Nachrichten in der Kategorie, die diese Zeile mit der Spaltenüberschrift entspricht.</span><span class="sxs-lookup"><span data-stu-id="45d70-117">In a heading row in categorized MAPI tables, it contains the number of unread non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="45d70-118">Diese Eigenschaft enthält die Anzahl der Nachrichten in den Ordner Inhaltstabelle für den das Flag MSGFLAG_READ in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="45d70-118">This property contains the number of messages in the folder contents table for which the MSGFLAG_READ flag is not set in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="45d70-119">Die **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))-Eigenschaft enthält die Anzahl der insgesamt Nachrichten für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="45d70-119">The **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) property contains the total message count for the folder.</span></span> <span data-ttu-id="45d70-120">Die **PR_CONTENT_COUNT** und diese Eigenschaft sind für Clients schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="45d70-120">The **PR_CONTENT_COUNT** and this property are read-only to clients.</span></span> 
  
<span data-ttu-id="45d70-121">Einige Clientanwendungen werden die Kopfzeile einer Kategorie unterschiedlich, je nachdem der Wert dieser Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="45d70-121">Some client applications display the heading row of a category differently depending on the value of this property.</span></span> <span data-ttu-id="45d70-122">Ein Client kann beispielsweise eine Kategorie anzeigen, die ungelesene Nachrichten fett enthält.</span><span class="sxs-lookup"><span data-stu-id="45d70-122">For example, a client can display a category that includes unread messages in bold.</span></span> <span data-ttu-id="45d70-123">Diese Eigenschaft kann nicht als eine Kategorie und beim Versuch verwendet werden, hierzu Ergebnisse in der MAPI_E_INVALID_PARAMETER-Wert aus der [SortTable](imapitable-sorttable.md) -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="45d70-123">This property cannot be used as a category and an attempt to do so results in the MAPI_E_INVALID_PARAMETER value being returned from the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="45d70-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="45d70-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45d70-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="45d70-125">Protocol specifications</span></span>

<span data-ttu-id="45d70-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45d70-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45d70-127">Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="45d70-127">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45d70-128">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45d70-128">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45d70-129">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="45d70-129">Handles folder operations.</span></span>
    
<span data-ttu-id="45d70-130">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45d70-130">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45d70-131">Zulässige Vorgänge für die Hauptobjekte-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="45d70-131">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45d70-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="45d70-132">Header files</span></span>

<span data-ttu-id="45d70-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45d70-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="45d70-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="45d70-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="45d70-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45d70-135">Mapitags.h</span></span>
  
> <span data-ttu-id="45d70-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="45d70-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45d70-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45d70-137">See also</span></span>



[<span data-ttu-id="45d70-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45d70-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45d70-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45d70-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45d70-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="45d70-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45d70-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="45d70-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
