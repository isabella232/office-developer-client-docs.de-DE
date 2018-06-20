---
title: Kanonische PidTag7BitDisplayName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTag7BitDisplayName
api_type:
- HeaderDef
ms.assetid: 803d7c4e-ed80-4d5b-988f-27068a8ccd63
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4ae7645e45efb461ac53b6718569d909cec76504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794027"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a><span data-ttu-id="cbcce-103">Kanonische PidTag7BitDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cbcce-103">PidTag7BitDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="cbcce-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cbcce-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cbcce-105">Enthält eine 7-Bit-ASCII-Darstellung der messaging dem Namen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="cbcce-105">Contains a 7-bit ASCII representation of a messaging user's name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cbcce-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cbcce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cbcce-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="cbcce-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="cbcce-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="cbcce-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cbcce-109">0x39FF</span><span class="sxs-lookup"><span data-stu-id="cbcce-109">0x39FF</span></span>  <br/> |
|<span data-ttu-id="cbcce-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cbcce-110">Data type:</span></span>  <br/> |<span data-ttu-id="cbcce-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cbcce-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cbcce-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cbcce-112">Area:</span></span>  <br/> |<span data-ttu-id="cbcce-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="cbcce-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbcce-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cbcce-114">Remarks</span></span>

<span data-ttu-id="cbcce-115">Diese Eigenschaften ordnen Sie die Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) in eine 7-Bit-Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="cbcce-115">These properties map the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property into a 7-bit character set.</span></span> <span data-ttu-id="cbcce-116">Einige Messagingsysteme wie Internet und bestimmte x. 400-Links sind auf die 128-7-Bit-ASCII-Code Zeichensatz beschränkt.</span><span class="sxs-lookup"><span data-stu-id="cbcce-116">Some messaging systems, such as Internet and certain X.400 links, are limited to the 128-character 7-bit ASCII code set.</span></span> <span data-ttu-id="cbcce-117">Gateways für die messaging-Systemen können die Leistung verbessern, indem Aufrufen der [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) -Methode zum Abrufen dieser direkt-Eigenschaft, wodurch zusätzliche Verarbeitung für die Konvertierung von Code zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="cbcce-117">Gateways to such messaging systems can improve their performance by calling the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method directly to retrieve the this property, thereby avoiding extra processing for code conversion.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cbcce-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cbcce-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cbcce-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cbcce-119">Protocol specifications</span></span>

<span data-ttu-id="cbcce-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcce-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcce-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="cbcce-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cbcce-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcce-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcce-123">Gibt die Eigenschaften und Vorgänge zu Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="cbcce-123">Specifies the properties and operations on lists of users, contacts, groups and resources.</span></span>
    
<span data-ttu-id="cbcce-124">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcce-124">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcce-125">Ein Client-Kommunikation mit einem NSPI-Server verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cbcce-125">Handles a client's communications with an NSPI server.</span></span>
    
<span data-ttu-id="cbcce-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcce-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcce-127">Verarbeitet den Reihenfolge und Datenfluss, die zum Übertragen von Daten zwischen Client und Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cbcce-127">Handles the order and data flow that is used to transfers data between client and server.</span></span>
    
<span data-ttu-id="cbcce-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcce-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcce-129">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="cbcce-129">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="cbcce-130">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbcce-130">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbcce-131">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="cbcce-131">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cbcce-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="cbcce-132">Header files</span></span>

<span data-ttu-id="cbcce-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cbcce-133">Mapitags.h</span></span>
  
> <span data-ttu-id="cbcce-134">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cbcce-134">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="cbcce-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cbcce-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="cbcce-136">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="cbcce-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cbcce-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbcce-137">See also</span></span>



[<span data-ttu-id="cbcce-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cbcce-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cbcce-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cbcce-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cbcce-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cbcce-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cbcce-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cbcce-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

