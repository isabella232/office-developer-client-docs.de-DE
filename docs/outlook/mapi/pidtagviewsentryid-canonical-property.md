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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1980e3bd815b370f125f4449dd7b7f340a7dcb9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795280"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="c71d4-103">PidTagViewsEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c71d4-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c71d4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c71d4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c71d4-105">Die Eintrags-ID des Ordners benutzerdefinierte Ansichten enthält.</span><span class="sxs-lookup"><span data-stu-id="c71d4-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c71d4-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c71d4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c71d4-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c71d4-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c71d4-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="c71d4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c71d4-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="c71d4-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="c71d4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c71d4-110">Data type:</span></span>  <br/> |<span data-ttu-id="c71d4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c71d4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c71d4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c71d4-112">Area:</span></span>  <br/> |<span data-ttu-id="c71d4-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="c71d4-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c71d4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c71d4-114">Remarks</span></span>

<span data-ttu-id="c71d4-115">Der gemeinsamen Ordner anzeigen enthält ein vordefiniertes Satzes von Standardansicht Bezeichner, während der Ansichtordner Bezeichner definiert durch ein messaging-Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="c71d4-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="c71d4-116">Diese Ordner, die nicht in der Hierarchie zwischen Personen Nachricht (IPM) sichtbar sind, können enthalten viele Ansicht Bezeichner, die jeweils als eine Nachricht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c71d4-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="c71d4-117">Die Client-Anwendung kann wahlweise Zusammenführen von zwei Sätze der Bezeichner und diese beiden zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="c71d4-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c71d4-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c71d4-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c71d4-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c71d4-119">Header files</span></span>

<span data-ttu-id="c71d4-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c71d4-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="c71d4-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c71d4-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="c71d4-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c71d4-122">Mapitags.h</span></span>
  
> <span data-ttu-id="c71d4-123">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c71d4-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c71d4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c71d4-124">See also</span></span>



[<span data-ttu-id="c71d4-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c71d4-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c71d4-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c71d4-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c71d4-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c71d4-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c71d4-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c71d4-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

