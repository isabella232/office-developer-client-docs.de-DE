---
title: PidTagAccess (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bb00d4e0e1437f9b3c13ac5e7d0a9dc4f3610d32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794039"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="e644b-103">PidTagAccess (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e644b-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="e644b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e644b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e644b-105">Enthält eine Bitmaske aus Flags, die angibt, die Vorgänge, die an den Client für das Objekt verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e644b-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e644b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e644b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e644b-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e644b-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="e644b-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="e644b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e644b-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="e644b-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="e644b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e644b-110">Data type:</span></span>  <br/> |<span data-ttu-id="e644b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e644b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e644b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e644b-112">Area:</span></span>  <br/> |<span data-ttu-id="e644b-113">Access-Steuerelementeigenschaften</span><span class="sxs-lookup"><span data-stu-id="e644b-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e644b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e644b-114">Remarks</span></span>

<span data-ttu-id="e644b-115">Diese Eigenschaft ist schreibgeschützt für den Client.</span><span class="sxs-lookup"><span data-stu-id="e644b-115">This property is read-only for the client.</span></span> <span data-ttu-id="e644b-116">Es muss ein bitweises **oder** von NULL oder mehrere Werte aus der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e644b-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="e644b-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="e644b-117">**Name**</span></span>|<span data-ttu-id="e644b-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e644b-118">**Value**</span></span>|<span data-ttu-id="e644b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e644b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e644b-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="e644b-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="e644b-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e644b-121">0x00000001</span></span>  <br/> |<span data-ttu-id="e644b-122">Schreiben</span><span class="sxs-lookup"><span data-stu-id="e644b-122">Write</span></span>  <br/> |
|<span data-ttu-id="e644b-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="e644b-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="e644b-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e644b-124">0x00000002</span></span>  <br/> |<span data-ttu-id="e644b-125">Lesen</span><span class="sxs-lookup"><span data-stu-id="e644b-125">Read</span></span>  <br/> |
|<span data-ttu-id="e644b-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="e644b-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="e644b-127">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="e644b-127">0x00000004</span></span>  <br/> |<span data-ttu-id="e644b-128">Löschen</span><span class="sxs-lookup"><span data-stu-id="e644b-128">Delete</span></span>  <br/> |
|<span data-ttu-id="e644b-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="e644b-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="e644b-130">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="e644b-130">0x00000008</span></span>  <br/> |<span data-ttu-id="e644b-131">Erstellen von Unterordnern im Ordner-Hierarchie</span><span class="sxs-lookup"><span data-stu-id="e644b-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="e644b-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="e644b-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="e644b-133">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="e644b-133">0x00000010</span></span>  <br/> |<span data-ttu-id="e644b-134">Erstellen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e644b-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="e644b-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="e644b-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="e644b-136">0 x 00000020</span><span class="sxs-lookup"><span data-stu-id="e644b-136">0x00000020</span></span>  <br/> |<span data-ttu-id="e644b-137">Erstellen der zugeordnete von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e644b-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="e644b-138">Die Flags MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY und MAPI_ACCESS_READ werden für Ordner und Message-Objekten und in der Spalte **PR_ACCESS** in Inhalt und Inhalt der zugeordneten Tabellen gefunden.</span><span class="sxs-lookup"><span data-stu-id="e644b-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="e644b-139">Die Flags MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS und MAPI_ACCESS_CREATE_HIERARCHY befinden sich auf nur Folder-Objekten.</span><span class="sxs-lookup"><span data-stu-id="e644b-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e644b-140">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e644b-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e644b-141">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e644b-141">Protocol specifications</span></span>

<span data-ttu-id="e644b-142">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e644b-142">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e644b-143">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e644b-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e644b-144">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e644b-144">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e644b-145">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="e644b-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e644b-146">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e644b-146">Header files</span></span>

<span data-ttu-id="e644b-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e644b-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="e644b-148">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e644b-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="e644b-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e644b-149">Mapitags.h</span></span>
  
> <span data-ttu-id="e644b-150">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e644b-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e644b-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e644b-151">See also</span></span>



[<span data-ttu-id="e644b-152">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e644b-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e644b-153">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e644b-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e644b-154">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e644b-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e644b-155">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e644b-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

