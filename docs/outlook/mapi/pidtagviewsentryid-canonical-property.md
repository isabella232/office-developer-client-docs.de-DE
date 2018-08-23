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
ms.openlocfilehash: 73ed7213ea2bd5079458ccc237b65590f06e8d53
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586263"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="8dedf-103">PidTagViewsEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8dedf-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="8dedf-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8dedf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8dedf-105">Die Eintrags-ID des Ordners benutzerdefinierte Ansichten enthält.</span><span class="sxs-lookup"><span data-stu-id="8dedf-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8dedf-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8dedf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8dedf-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8dedf-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="8dedf-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8dedf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8dedf-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="8dedf-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="8dedf-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8dedf-110">Data type:</span></span>  <br/> |<span data-ttu-id="8dedf-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8dedf-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8dedf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8dedf-112">Area:</span></span>  <br/> |<span data-ttu-id="8dedf-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="8dedf-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8dedf-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="8dedf-114">Remarks</span></span>

<span data-ttu-id="8dedf-115">Der gemeinsamen Ordner anzeigen enthält ein vordefiniertes Satzes von Standardansicht Bezeichner, während der Ansichtordner Bezeichner definiert durch ein messaging-Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="8dedf-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="8dedf-116">Diese Ordner, die nicht in der Hierarchie zwischen Personen Nachricht (IPM) sichtbar sind, können enthalten viele Ansicht Bezeichner, die jeweils als eine Nachricht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8dedf-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="8dedf-117">Die Client-Anwendung kann wahlweise Zusammenführen von zwei Sätze der Bezeichner und diese beiden zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="8dedf-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8dedf-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8dedf-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8dedf-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="8dedf-119">Header files</span></span>

<span data-ttu-id="8dedf-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8dedf-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="8dedf-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8dedf-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="8dedf-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8dedf-122">Mapitags.h</span></span>
  
> <span data-ttu-id="8dedf-123">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8dedf-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8dedf-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dedf-124">See also</span></span>



[<span data-ttu-id="8dedf-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8dedf-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8dedf-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8dedf-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8dedf-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8dedf-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8dedf-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8dedf-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

