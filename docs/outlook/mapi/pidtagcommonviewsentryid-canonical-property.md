---
title: PidTagCommonViewsEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7449e59227b147d34c2329175d0251dbb9c427b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581342"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a><span data-ttu-id="fe551-103">PidTagCommonViewsEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fe551-103">PidTagCommonViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="fe551-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe551-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe551-105">Enthält die Eintrags-ID der vordefinierten gemeinsame Ansicht Ordner.</span><span class="sxs-lookup"><span data-stu-id="fe551-105">Contains the entry identifier of the predefined common view folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe551-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fe551-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe551-107">PR_COMMON_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fe551-107">PR_COMMON_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="fe551-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="fe551-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fe551-109">0x35E6</span><span class="sxs-lookup"><span data-stu-id="fe551-109">0x35E6</span></span>  <br/> |
|<span data-ttu-id="fe551-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fe551-110">Data type:</span></span>  <br/> |<span data-ttu-id="fe551-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fe551-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fe551-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fe551-112">Area:</span></span>  <br/> |<span data-ttu-id="fe551-113">Outlook-Anwendung</span><span class="sxs-lookup"><span data-stu-id="fe551-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe551-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="fe551-114">Remarks</span></span>

<span data-ttu-id="fe551-115">Der gemeinsamen Ordner anzeigen enthält ein vordefiniertes Satzes von Standardansicht Bezeichner, während der Ansichtordner Bezeichner definiert durch ein messaging-Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="fe551-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="fe551-116">Diese Ordner, die nicht in der Hierarchie zwischen Personen Nachricht (IPM) sichtbar sind, können enthalten viele Ansicht Bezeichner, die jeweils als eine Nachricht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fe551-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="fe551-117">Eine Clientanwendung kann wahlweise Zusammenführen von zwei Sätze der Bezeichner und diese beiden zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="fe551-117">A client application can choose to merge the two sets of specifiers and make them both available.</span></span> 
  
<span data-ttu-id="fe551-118">Weitere Informationen zu Sichten finden Sie unter [Anzeigen von Ordnern](mapi-view-folders.md).</span><span class="sxs-lookup"><span data-stu-id="fe551-118">For more information on views, see [View Folders](mapi-view-folders.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fe551-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fe551-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fe551-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="fe551-120">Header files</span></span>

<span data-ttu-id="fe551-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe551-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe551-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fe551-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="fe551-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fe551-123">Mapitags.h</span></span>
  
> <span data-ttu-id="fe551-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fe551-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe551-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe551-125">See also</span></span>



[<span data-ttu-id="fe551-126">PidTagDefaultViewEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fe551-126">PidTagDefaultViewEntryId Canonical Property</span></span>](pidtagdefaultviewentryid-canonical-property.md)
  
[<span data-ttu-id="fe551-127">PidTagViewsEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fe551-127">PidTagViewsEntryId Canonical Property</span></span>](pidtagviewsentryid-canonical-property.md)


[<span data-ttu-id="fe551-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe551-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe551-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe551-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe551-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fe551-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe551-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fe551-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

