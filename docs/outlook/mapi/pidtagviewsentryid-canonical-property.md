---
title: PidTagViewsEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7d261ac0e9aaf36f2333b04b45edfaf8e24fa30d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427311"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="6ce67-103">PidTagViewsEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6ce67-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="6ce67-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ce67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ce67-105">Enthält die Eintrags-ID des benutzerdefinierten Ordners Ansichten.</span><span class="sxs-lookup"><span data-stu-id="6ce67-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ce67-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6ce67-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ce67-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6ce67-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="6ce67-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6ce67-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6ce67-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="6ce67-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="6ce67-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6ce67-110">Data type:</span></span>  <br/> |<span data-ttu-id="6ce67-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6ce67-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6ce67-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6ce67-112">Area:</span></span>  <br/> |<span data-ttu-id="6ce67-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="6ce67-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ce67-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ce67-114">Remarks</span></span>

<span data-ttu-id="6ce67-115">Der Allgemeine Ansichtsordner enthält einen vordefinierten Satz von Standardansichtsbezeichnern, während der Ansichtsordner von einem Messagingbenutzer definierte Specifier enthält.</span><span class="sxs-lookup"><span data-stu-id="6ce67-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="6ce67-116">Diese Ordner, die in der IpM-Hierarchie (Interpersonal Message) nicht sichtbar sind, können viele Ansichtsbezeichner enthalten, die jeweils als Nachricht gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="6ce67-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="6ce67-117">Die Clientanwendung kann die beiden Sätze von Specifiern zusammenführen und beide verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="6ce67-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6ce67-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6ce67-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6ce67-119">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="6ce67-119">Header files</span></span>

<span data-ttu-id="6ce67-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ce67-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ce67-121">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6ce67-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="6ce67-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6ce67-122">Mapitags.h</span></span>
  
> <span data-ttu-id="6ce67-123">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6ce67-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ce67-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ce67-124">See also</span></span>



[<span data-ttu-id="6ce67-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ce67-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ce67-126">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="6ce67-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ce67-127">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6ce67-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ce67-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6ce67-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

