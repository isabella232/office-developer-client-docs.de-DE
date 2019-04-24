---
title: Kanonische Pidtagaccess (-Eigenschaft
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
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316513"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="6c833-103">Kanonische Pidtagaccess (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6c833-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="6c833-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c833-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c833-105">Enthält eine Bitmaske von Flags, die die Vorgänge angibt, die für den Client für das Objekt zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="6c833-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c833-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6c833-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c833-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6c833-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="6c833-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6c833-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c833-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="6c833-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="6c833-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6c833-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c833-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6c833-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6c833-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6c833-112">Area:</span></span>  <br/> |<span data-ttu-id="6c833-113">Zugriffssteuerungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c833-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c833-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c833-114">Remarks</span></span>

<span data-ttu-id="6c833-115">Diese Eigenschaft ist für den Client schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6c833-115">This property is read-only for the client.</span></span> <span data-ttu-id="6c833-116">Es muss eine bitweise **or** -Wert von NULL oder mehr aus der folgenden Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="6c833-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="6c833-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="6c833-117">**Name**</span></span>|<span data-ttu-id="6c833-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6c833-118">**Value**</span></span>|<span data-ttu-id="6c833-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c833-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6c833-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="6c833-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="6c833-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6c833-121">0x00000001</span></span>  <br/> |<span data-ttu-id="6c833-122">Schreiben</span><span class="sxs-lookup"><span data-stu-id="6c833-122">Write</span></span>  <br/> |
|<span data-ttu-id="6c833-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="6c833-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="6c833-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6c833-124">0x00000002</span></span>  <br/> |<span data-ttu-id="6c833-125">Lesen</span><span class="sxs-lookup"><span data-stu-id="6c833-125">Read</span></span>  <br/> |
|<span data-ttu-id="6c833-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="6c833-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="6c833-127">0x00000004</span><span class="sxs-lookup"><span data-stu-id="6c833-127">0x00000004</span></span>  <br/> |<span data-ttu-id="6c833-128">Löschen</span><span class="sxs-lookup"><span data-stu-id="6c833-128">Delete</span></span>  <br/> |
|<span data-ttu-id="6c833-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="6c833-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="6c833-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6c833-130">0x00000008</span></span>  <br/> |<span data-ttu-id="6c833-131">Erstellen von Unterordnern in der Ordnerhierarchie</span><span class="sxs-lookup"><span data-stu-id="6c833-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="6c833-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="6c833-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="6c833-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c833-133">0x00000010</span></span>  <br/> |<span data-ttu-id="6c833-134">Erstellen von Inhaltsnachrichten</span><span class="sxs-lookup"><span data-stu-id="6c833-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="6c833-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="6c833-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="6c833-136">0x00000020</span><span class="sxs-lookup"><span data-stu-id="6c833-136">0x00000020</span></span>  <br/> |<span data-ttu-id="6c833-137">Erstellen von zugeordneten Inhaltsnachrichten</span><span class="sxs-lookup"><span data-stu-id="6c833-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="6c833-138">Die MAPI_ACCESS_DELETE-, MAPI_ACCESS_MODIFY-und MAPI_ACCESS_READ-Flags befinden sich in Folder-und Message-Objekten sowie in der Spalte **PR_ACCESS** unter Inhaltstabellen und zugeordneten Inhaltstabellen.</span><span class="sxs-lookup"><span data-stu-id="6c833-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="6c833-139">Die MAPI_ACCESS_CREATE_ASSOCIATED-, MAPI_ACCESS_CREATE_CONTENTS-und MAPI_ACCESS_CREATE_HIERARCHY-Flags werden nur auf Folder-Objekten gefunden.</span><span class="sxs-lookup"><span data-stu-id="6c833-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6c833-140">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6c833-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c833-141">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6c833-141">Protocol specifications</span></span>

<span data-ttu-id="6c833-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c833-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c833-143">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6c833-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c833-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c833-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c833-145">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="6c833-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c833-146">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="6c833-146">Header files</span></span>

<span data-ttu-id="6c833-147">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6c833-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c833-148">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="6c833-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c833-149">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6c833-149">Mapitags.h</span></span>
  
> <span data-ttu-id="6c833-150">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="6c833-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c833-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c833-151">See also</span></span>



[<span data-ttu-id="6c833-152">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c833-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c833-153">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c833-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c833-154">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6c833-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c833-155">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6c833-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

