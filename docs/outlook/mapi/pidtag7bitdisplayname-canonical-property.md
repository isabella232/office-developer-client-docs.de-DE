---
title: PidTag7BitDisplayName (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e5177d47749c2f60a883bd12fbba27045114c601
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401069"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a><span data-ttu-id="13c26-103">PidTag7BitDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="13c26-103">PidTag7BitDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="13c26-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13c26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13c26-105">Enthält eine 7-Bit-ASCII-Darstellung der messaging dem Namen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="13c26-105">Contains a 7-bit ASCII representation of a messaging user's name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13c26-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="13c26-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13c26-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="13c26-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="13c26-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="13c26-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13c26-109">0x39FF</span><span class="sxs-lookup"><span data-stu-id="13c26-109">0x39FF</span></span>  <br/> |
|<span data-ttu-id="13c26-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="13c26-110">Data type:</span></span>  <br/> |<span data-ttu-id="13c26-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="13c26-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="13c26-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="13c26-112">Area:</span></span>  <br/> |<span data-ttu-id="13c26-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="13c26-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13c26-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13c26-114">Remarks</span></span>

<span data-ttu-id="13c26-115">Diese Eigenschaften ordnen Sie die Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) in eine 7-Bit-Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="13c26-115">These properties map the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property into a 7-bit character set.</span></span> <span data-ttu-id="13c26-116">Einige Messagingsysteme wie Internet und bestimmte x. 400-Links sind auf die 128-7-Bit-ASCII-Code Zeichensatz beschränkt.</span><span class="sxs-lookup"><span data-stu-id="13c26-116">Some messaging systems, such as Internet and certain X.400 links, are limited to the 128-character 7-bit ASCII code set.</span></span> <span data-ttu-id="13c26-117">Gateways für die messaging-Systemen können die Leistung verbessern, indem Aufrufen der [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) -Methode zum Abrufen dieser direkt-Eigenschaft, wodurch zusätzliche Verarbeitung für die Konvertierung von Code zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="13c26-117">Gateways to such messaging systems can improve their performance by calling the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method directly to retrieve the this property, thereby avoiding extra processing for code conversion.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="13c26-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="13c26-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13c26-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="13c26-119">Protocol specifications</span></span>

<span data-ttu-id="13c26-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13c26-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13c26-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="13c26-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13c26-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13c26-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13c26-123">Gibt die Eigenschaften und Vorgänge zu Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="13c26-123">Specifies the properties and operations on lists of users, contacts, groups and resources.</span></span>
    
<span data-ttu-id="13c26-124">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13c26-124">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13c26-125">Ein Client-Kommunikation mit einem NSPI-Server verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="13c26-125">Handles a client's communications with an NSPI server.</span></span>
    
<span data-ttu-id="13c26-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13c26-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13c26-127">Verarbeitet den Reihenfolge und Datenfluss, die zum Übertragen von Daten zwischen Client und Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13c26-127">Handles the order and data flow that is used to transfers data between client and server.</span></span>
    
<span data-ttu-id="13c26-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13c26-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13c26-129">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="13c26-129">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="13c26-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13c26-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13c26-131">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="13c26-131">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13c26-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="13c26-132">Header files</span></span>

<span data-ttu-id="13c26-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="13c26-133">Mapitags.h</span></span>
  
> <span data-ttu-id="13c26-134">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="13c26-134">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="13c26-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13c26-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="13c26-136">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="13c26-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13c26-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13c26-137">See also</span></span>



[<span data-ttu-id="13c26-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13c26-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13c26-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13c26-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13c26-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="13c26-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13c26-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="13c26-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

