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
ms.openlocfilehash: bf92e62dc572a81b6e0aab4cb1b0fc8afe97800d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573096"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="03a1d-103">PidTagAttachFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="03a1d-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="03a1d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03a1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03a1d-105">Eine Bitmaske aus Flags für eine Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="03a1d-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03a1d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="03a1d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03a1d-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="03a1d-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="03a1d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="03a1d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03a1d-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="03a1d-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="03a1d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="03a1d-110">Data type:</span></span>  <br/> |<span data-ttu-id="03a1d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="03a1d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="03a1d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="03a1d-112">Area:</span></span>  <br/> |<span data-ttu-id="03a1d-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="03a1d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03a1d-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="03a1d-114">Remarks</span></span>

<span data-ttu-id="03a1d-115">Diese Eigenschaft wird verwendet, für die MHTML-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="03a1d-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="03a1d-116">Für die Bitmaske **PR_ATTACH_FLAGS** kann eine oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="03a1d-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="03a1d-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="03a1d-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="03a1d-118">Gibt an, dass diese Anlage nicht verfügbar für HTML-Rendering Clientanwendungen ist und sollte in Multipurpose Internet Mail Extensions (MIME) Verarbeitung ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="03a1d-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="03a1d-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="03a1d-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="03a1d-120">Gibt an, dass diese Anlage ist nicht verfügbar für Clientanwendungen Rendern in Rich Text Format (RTF) und MAPI ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="03a1d-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="03a1d-121">Wenn die **PR_ATTACH_FLAGS** -Eigenschaft gleich NULL ist oder nicht vorhanden ist, ist die Anlage von allen Anwendungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="03a1d-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="03a1d-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="03a1d-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03a1d-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="03a1d-123">Protocol specifications</span></span>

<span data-ttu-id="03a1d-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03a1d-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03a1d-125">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="03a1d-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03a1d-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="03a1d-126">Header files</span></span>

<span data-ttu-id="03a1d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03a1d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="03a1d-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="03a1d-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="03a1d-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="03a1d-129">Mapitags.h</span></span>
  
> <span data-ttu-id="03a1d-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="03a1d-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03a1d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03a1d-131">See also</span></span>



[<span data-ttu-id="03a1d-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03a1d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03a1d-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03a1d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03a1d-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="03a1d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03a1d-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="03a1d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

