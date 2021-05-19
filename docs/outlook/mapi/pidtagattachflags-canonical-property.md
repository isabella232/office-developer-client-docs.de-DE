---
title: PidTagAttachFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: efccd75cce04e4e392a7fbd9feecc7c8b49ab57e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339333"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="cdcdc-103">PidTagAttachFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cdcdc-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="cdcdc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdcdc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdcdc-105">Enthält eine Bitmaske mit Flags für eine Anlage.</span><span class="sxs-lookup"><span data-stu-id="cdcdc-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cdcdc-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cdcdc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cdcdc-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="cdcdc-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="cdcdc-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="cdcdc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cdcdc-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="cdcdc-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="cdcdc-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cdcdc-110">Data type:</span></span>  <br/> |<span data-ttu-id="cdcdc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cdcdc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cdcdc-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cdcdc-112">Area:</span></span>  <br/> |<span data-ttu-id="cdcdc-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="cdcdc-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cdcdc-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cdcdc-114">Remarks</span></span>

<span data-ttu-id="cdcdc-115">Diese Eigenschaft wird für die MHTML-Unterstützung verwendet.</span><span class="sxs-lookup"><span data-stu-id="cdcdc-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="cdcdc-116">Mindestens eines der folgenden Flags kann für die PR_ATTACH_FLAGS **festgelegt** werden:</span><span class="sxs-lookup"><span data-stu-id="cdcdc-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="cdcdc-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="cdcdc-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="cdcdc-118">Gibt an, dass diese Anlage für HTML-Renderinganwendungen nicht verfügbar ist und in der Verarbeitung von Mehrzweck-Internet-Mail-Erweiterungen (MIME) ignoriert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="cdcdc-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="cdcdc-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="cdcdc-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="cdcdc-120">Gibt an, dass diese Anlage nicht für Anwendungen verfügbar ist, die im Rich Text Format (RTF) gerendert werden und von MAPI ignoriert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="cdcdc-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="cdcdc-121">Wenn die **PR_ATTACH_FLAGS** null oder nicht vorhanden ist, muss die Anlage von allen Anwendungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="cdcdc-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cdcdc-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cdcdc-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cdcdc-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cdcdc-123">Protocol specifications</span></span>

<span data-ttu-id="cdcdc-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdcdc-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdcdc-125">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="cdcdc-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cdcdc-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="cdcdc-126">Header files</span></span>

<span data-ttu-id="cdcdc-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cdcdc-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="cdcdc-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="cdcdc-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="cdcdc-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cdcdc-129">Mapitags.h</span></span>
  
> <span data-ttu-id="cdcdc-130">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cdcdc-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cdcdc-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdcdc-131">See also</span></span>



[<span data-ttu-id="cdcdc-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cdcdc-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cdcdc-133">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="cdcdc-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cdcdc-134">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cdcdc-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cdcdc-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cdcdc-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

