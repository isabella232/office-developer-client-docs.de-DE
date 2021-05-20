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
ms.openlocfilehash: e22b8905901f16606614ac918896f3afe0093752
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437343"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a><span data-ttu-id="8f1ec-103">PidTagCommonViewsEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8f1ec-103">PidTagCommonViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="8f1ec-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f1ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f1ec-105">Enthält die Eintrags-ID des vordefinierten Ordners für allgemeine Ansicht.</span><span class="sxs-lookup"><span data-stu-id="8f1ec-105">Contains the entry identifier of the predefined common view folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f1ec-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8f1ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f1ec-107">PR_COMMON_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8f1ec-107">PR_COMMON_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="8f1ec-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8f1ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8f1ec-109">0x35E6</span><span class="sxs-lookup"><span data-stu-id="8f1ec-109">0x35E6</span></span>  <br/> |
|<span data-ttu-id="8f1ec-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8f1ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="8f1ec-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8f1ec-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8f1ec-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8f1ec-112">Area:</span></span>  <br/> |<span data-ttu-id="8f1ec-113">Outlook-Anwendung</span><span class="sxs-lookup"><span data-stu-id="8f1ec-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f1ec-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8f1ec-114">Remarks</span></span>

<span data-ttu-id="8f1ec-115">Der Allgemeine Ansichtsordner enthält einen vordefinierten Satz von Standardansichtsbezeichnern, während der Ansichtsordner von einem Messagingbenutzer definierte Specifier enthält.</span><span class="sxs-lookup"><span data-stu-id="8f1ec-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="8f1ec-116">Diese Ordner, die in der IpM-Hierarchie (Interpersonal Message) nicht sichtbar sind, können viele Ansichtsbezeichner enthalten, die jeweils als Nachricht gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="8f1ec-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="8f1ec-117">Eine Clientanwendung kann die beiden Sätze von Specifiern zusammenführen und beide verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="8f1ec-117">A client application can choose to merge the two sets of specifiers and make them both available.</span></span> 
  
<span data-ttu-id="8f1ec-118">Weitere Informationen zu Ansichten finden Sie unter [View Folders](mapi-view-folders.md).</span><span class="sxs-lookup"><span data-stu-id="8f1ec-118">For more information on views, see [View Folders](mapi-view-folders.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8f1ec-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8f1ec-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8f1ec-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="8f1ec-120">Header files</span></span>

<span data-ttu-id="8f1ec-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8f1ec-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f1ec-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8f1ec-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="8f1ec-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8f1ec-123">Mapitags.h</span></span>
  
> <span data-ttu-id="8f1ec-124">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8f1ec-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f1ec-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f1ec-125">See also</span></span>



[<span data-ttu-id="8f1ec-126">PidTagDefaultViewEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8f1ec-126">PidTagDefaultViewEntryId Canonical Property</span></span>](pidtagdefaultviewentryid-canonical-property.md)
  
[<span data-ttu-id="8f1ec-127">PidTagViewsEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8f1ec-127">PidTagViewsEntryId Canonical Property</span></span>](pidtagviewsentryid-canonical-property.md)


[<span data-ttu-id="8f1ec-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f1ec-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f1ec-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="8f1ec-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f1ec-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8f1ec-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f1ec-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8f1ec-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

