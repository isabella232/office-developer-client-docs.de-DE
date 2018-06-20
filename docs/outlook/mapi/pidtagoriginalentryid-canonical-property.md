---
title: Kanonische PidTagOriginalEntryId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalEntryId
api_type:
- COM
ms.assetid: 8197d2c7-8665-41b8-bd3a-e9c1c2e642e9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d60531b087d00ca63a060a4dbfac559ba3b01788
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794698"
---
# <a name="pidtagoriginalentryid-canonical-property"></a><span data-ttu-id="1770e-103">Kanonische PidTagOriginalEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1770e-103">PidTagOriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="1770e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1770e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1770e-105">Enthält die ursprünglichen Eintrags-ID für einen Eintrag aus einem Adressbuch an ein persönliches Adressbuch oder anderen beschreibbaren Adressbuch kopiert.</span><span class="sxs-lookup"><span data-stu-id="1770e-105">Contains the original entry identifier for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1770e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1770e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1770e-107">PR_ORIGINAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1770e-107">PR_ORIGINAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="1770e-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="1770e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1770e-109">0x3A12</span><span class="sxs-lookup"><span data-stu-id="1770e-109">0x3A12</span></span>  <br/> |
|<span data-ttu-id="1770e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1770e-110">Data type:</span></span>  <br/> |<span data-ttu-id="1770e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1770e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1770e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1770e-112">Area:</span></span>  <br/> |<span data-ttu-id="1770e-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="1770e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1770e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1770e-114">Remarks</span></span>

<span data-ttu-id="1770e-115">Diese Eigenschaft ist eine der Eigenschaften, die der ursprünglichen Quelle eines Eintrags kopierten Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="1770e-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="1770e-116">Bei einem Bericht nonread enthält diese Eigenschaft eine Kopie des Eintrags-ID von der ursprünglichen Empfänger der Nachricht für den der Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="1770e-116">For a nonread report, this property contains a copy of the entry identifier of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="1770e-117">Wenn Sie der ursprüngliche Empfänger einer Verteilerliste gehört, wird die Eintrags-ID der Verteilerliste für den Bericht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="1770e-117">When the original recipient is part of a distribution list, the entry identifier of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1770e-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1770e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1770e-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1770e-119">Protocol specifications</span></span>

<span data-ttu-id="1770e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1770e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1770e-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1770e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1770e-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1770e-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1770e-123">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="1770e-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="1770e-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1770e-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1770e-125">Synchronisieren von messaging Objektdaten zwischen einem Server und einem Client behandelt.</span><span class="sxs-lookup"><span data-stu-id="1770e-125">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1770e-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1770e-126">Header files</span></span>

<span data-ttu-id="1770e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1770e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="1770e-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1770e-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="1770e-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1770e-129">Mapitags.h</span></span>
  
> <span data-ttu-id="1770e-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1770e-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1770e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1770e-131">See also</span></span>



[<span data-ttu-id="1770e-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1770e-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1770e-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1770e-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1770e-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1770e-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1770e-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1770e-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

