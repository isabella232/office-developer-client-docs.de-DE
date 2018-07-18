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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b934f9694061e17118be35e3fabeeff3bbc61a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794090"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="23af9-103">PidTagAttachFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="23af9-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="23af9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23af9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23af9-105">Eine Bitmaske aus Flags für eine Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="23af9-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23af9-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="23af9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23af9-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="23af9-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="23af9-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="23af9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="23af9-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="23af9-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="23af9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="23af9-110">Data type:</span></span>  <br/> |<span data-ttu-id="23af9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="23af9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="23af9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="23af9-112">Area:</span></span>  <br/> |<span data-ttu-id="23af9-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="23af9-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23af9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23af9-114">Remarks</span></span>

<span data-ttu-id="23af9-115">Diese Eigenschaft wird verwendet, für die MHTML-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="23af9-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="23af9-116">Für die Bitmaske **PR_ATTACH_FLAGS** kann eine oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="23af9-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="23af9-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="23af9-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="23af9-118">Gibt an, dass diese Anlage nicht verfügbar für HTML-Rendering Clientanwendungen ist und sollte in Multipurpose Internet Mail Extensions (MIME) Verarbeitung ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="23af9-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="23af9-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="23af9-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="23af9-120">Gibt an, dass diese Anlage ist nicht verfügbar für Clientanwendungen Rendern in Rich Text Format (RTF) und MAPI ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="23af9-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="23af9-121">Wenn die **PR_ATTACH_FLAGS** -Eigenschaft gleich NULL ist oder nicht vorhanden ist, ist die Anlage von allen Anwendungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="23af9-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="23af9-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="23af9-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23af9-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="23af9-123">Protocol specifications</span></span>

<span data-ttu-id="23af9-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23af9-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23af9-125">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="23af9-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23af9-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="23af9-126">Header files</span></span>

<span data-ttu-id="23af9-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23af9-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="23af9-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="23af9-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="23af9-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="23af9-129">Mapitags.h</span></span>
  
> <span data-ttu-id="23af9-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="23af9-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23af9-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23af9-131">See also</span></span>



[<span data-ttu-id="23af9-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23af9-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23af9-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23af9-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23af9-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="23af9-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23af9-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="23af9-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

