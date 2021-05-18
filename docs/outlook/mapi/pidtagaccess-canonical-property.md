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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316513"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="7a4cf-103">PidTagAccess (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7a4cf-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="7a4cf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a4cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a4cf-105">Enthält eine Bitmaske mit Flags, die die Vorgänge angibt, die dem Client für das Objekt zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="7a4cf-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a4cf-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7a4cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a4cf-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7a4cf-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="7a4cf-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7a4cf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7a4cf-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="7a4cf-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="7a4cf-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7a4cf-110">Data type:</span></span>  <br/> |<span data-ttu-id="7a4cf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7a4cf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7a4cf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7a4cf-112">Area:</span></span>  <br/> |<span data-ttu-id="7a4cf-113">Eigenschaften der Zugriffssteuerung</span><span class="sxs-lookup"><span data-stu-id="7a4cf-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a4cf-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7a4cf-114">Remarks</span></span>

<span data-ttu-id="7a4cf-115">Diese Eigenschaft ist schreibgeschützt für den Client.</span><span class="sxs-lookup"><span data-stu-id="7a4cf-115">This property is read-only for the client.</span></span> <span data-ttu-id="7a4cf-116">Es muss ein bitweises **OR** von null oder mehr Werten aus der folgenden Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="7a4cf-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="7a4cf-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="7a4cf-117">**Name**</span></span>|<span data-ttu-id="7a4cf-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7a4cf-118">**Value**</span></span>|<span data-ttu-id="7a4cf-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a4cf-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7a4cf-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7a4cf-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="7a4cf-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7a4cf-121">0x00000001</span></span>  <br/> |<span data-ttu-id="7a4cf-122">Schreiben</span><span class="sxs-lookup"><span data-stu-id="7a4cf-122">Write</span></span>  <br/> |
|<span data-ttu-id="7a4cf-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="7a4cf-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="7a4cf-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7a4cf-124">0x00000002</span></span>  <br/> |<span data-ttu-id="7a4cf-125">Lesen</span><span class="sxs-lookup"><span data-stu-id="7a4cf-125">Read</span></span>  <br/> |
|<span data-ttu-id="7a4cf-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="7a4cf-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="7a4cf-127">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7a4cf-127">0x00000004</span></span>  <br/> |<span data-ttu-id="7a4cf-128">Löschen</span><span class="sxs-lookup"><span data-stu-id="7a4cf-128">Delete</span></span>  <br/> |
|<span data-ttu-id="7a4cf-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="7a4cf-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="7a4cf-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7a4cf-130">0x00000008</span></span>  <br/> |<span data-ttu-id="7a4cf-131">Erstellen von Unterordnern in der Ordnerhierarchie</span><span class="sxs-lookup"><span data-stu-id="7a4cf-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="7a4cf-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="7a4cf-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="7a4cf-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7a4cf-133">0x00000010</span></span>  <br/> |<span data-ttu-id="7a4cf-134">Erstellen von Inhaltsnachrichten</span><span class="sxs-lookup"><span data-stu-id="7a4cf-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="7a4cf-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="7a4cf-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="7a4cf-136">0x00000020</span><span class="sxs-lookup"><span data-stu-id="7a4cf-136">0x00000020</span></span>  <br/> |<span data-ttu-id="7a4cf-137">Erstellen zugeordneter Inhaltsnachrichten</span><span class="sxs-lookup"><span data-stu-id="7a4cf-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="7a4cf-138">Die MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY und MAPI_ACCESS_READ werden in Ordner- und Nachrichtenobjekten und in der spalte **PR_ACCESS** in Inhaltstabellen und zugehörigen Inhaltstabellen gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a4cf-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="7a4cf-139">Die MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS und MAPI_ACCESS_CREATE_HIERARCHY werden nur für Ordnerobjekte gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a4cf-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7a4cf-140">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7a4cf-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7a4cf-141">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7a4cf-141">Protocol specifications</span></span>

<span data-ttu-id="7a4cf-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a4cf-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a4cf-143">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7a4cf-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7a4cf-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a4cf-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a4cf-145">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="7a4cf-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7a4cf-146">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="7a4cf-146">Header files</span></span>

<span data-ttu-id="7a4cf-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a4cf-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a4cf-148">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7a4cf-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="7a4cf-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7a4cf-149">Mapitags.h</span></span>
  
> <span data-ttu-id="7a4cf-150">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7a4cf-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a4cf-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a4cf-151">See also</span></span>



[<span data-ttu-id="7a4cf-152">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a4cf-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7a4cf-153">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="7a4cf-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a4cf-154">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7a4cf-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a4cf-155">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7a4cf-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

