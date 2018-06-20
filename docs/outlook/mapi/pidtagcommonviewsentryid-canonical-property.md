---
title: Kanonische PidTagCommonViewsEntryId-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7d91ed369b3a6e8b4f62534d49b202b46c327baa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794177"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a><span data-ttu-id="0399c-103">Kanonische PidTagCommonViewsEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0399c-103">PidTagCommonViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="0399c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0399c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0399c-105">Enthält die Eintrags-ID der vordefinierten gemeinsame Ansicht Ordner.</span><span class="sxs-lookup"><span data-stu-id="0399c-105">Contains the entry identifier of the predefined common view folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0399c-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0399c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0399c-107">PR_COMMON_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0399c-107">PR_COMMON_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="0399c-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="0399c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0399c-109">0x35E6</span><span class="sxs-lookup"><span data-stu-id="0399c-109">0x35E6</span></span>  <br/> |
|<span data-ttu-id="0399c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0399c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0399c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0399c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0399c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0399c-112">Area:</span></span>  <br/> |<span data-ttu-id="0399c-113">Outlook-Anwendung</span><span class="sxs-lookup"><span data-stu-id="0399c-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0399c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0399c-114">Remarks</span></span>

<span data-ttu-id="0399c-115">Der gemeinsamen Ordner anzeigen enthält ein vordefiniertes Satzes von Standardansicht Bezeichner, während der Ansichtordner Bezeichner definiert durch ein messaging-Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="0399c-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="0399c-116">Diese Ordner, die nicht in der Hierarchie zwischen Personen Nachricht (IPM) sichtbar sind, können enthalten viele Ansicht Bezeichner, die jeweils als eine Nachricht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0399c-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="0399c-117">Eine Clientanwendung kann wahlweise Zusammenführen von zwei Sätze der Bezeichner und diese beiden zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="0399c-117">A client application can choose to merge the two sets of specifiers and make them both available.</span></span> 
  
<span data-ttu-id="0399c-118">Weitere Informationen zu Sichten finden Sie unter [Anzeigen von Ordnern](mapi-view-folders.md).</span><span class="sxs-lookup"><span data-stu-id="0399c-118">For more information on views, see [View Folders](mapi-view-folders.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0399c-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0399c-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0399c-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0399c-120">Header files</span></span>

<span data-ttu-id="0399c-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0399c-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="0399c-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0399c-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="0399c-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0399c-123">Mapitags.h</span></span>
  
> <span data-ttu-id="0399c-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0399c-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0399c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0399c-125">See also</span></span>



[<span data-ttu-id="0399c-126">Kanonische PidTagDefaultViewEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0399c-126">PidTagDefaultViewEntryId Canonical Property</span></span>](pidtagdefaultviewentryid-canonical-property.md)
  
[<span data-ttu-id="0399c-127">Kanonische PidTagViewsEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0399c-127">PidTagViewsEntryId Canonical Property</span></span>](pidtagviewsentryid-canonical-property.md)


[<span data-ttu-id="0399c-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0399c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0399c-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0399c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0399c-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0399c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0399c-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0399c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

