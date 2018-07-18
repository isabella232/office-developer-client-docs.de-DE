---
title: PidLidSmartNoAttach (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSmartNoAttach
api_type:
- COM
ms.assetid: 60299c1b-1b46-4c3a-8fb9-a2b4d3383aac
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 43e10652a7dccdf0da6592df0f9fc2daf5ea9bee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793789"
---
# <a name="pidlidsmartnoattach-canonical-property"></a><span data-ttu-id="86331-103">PidLidSmartNoAttach (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="86331-103">PidLidSmartNoAttach Canonical Property</span></span>

  
  
<span data-ttu-id="86331-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="86331-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="86331-105">Stellt dar, ob die Anlagen auf eine Nachricht gelten als ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="86331-105">Represents whether the attachments on a message are considered as hidden.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86331-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="86331-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86331-107">dispidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="86331-107">dispidSmartNoAttach</span></span>  <br/> |
|<span data-ttu-id="86331-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="86331-108">Property set:</span></span>  <br/> |<span data-ttu-id="86331-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="86331-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="86331-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="86331-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="86331-111">0x00008514</span><span class="sxs-lookup"><span data-stu-id="86331-111">0x00008514</span></span>  <br/> |
|<span data-ttu-id="86331-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="86331-112">Data type:</span></span>  <br/> |<span data-ttu-id="86331-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="86331-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="86331-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="86331-114">Area:</span></span>  <br/> |<span data-ttu-id="86331-115">Laufzeit-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="86331-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86331-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86331-116">Remarks</span></span>

<span data-ttu-id="86331-117">Diese Eigenschaft ist TRUE, wenn die Anlagen der Nachricht gelten als ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="86331-117">This property is TRUE if the attachments of the message are considered as hidden.</span></span>
  
<span data-ttu-id="86331-118">Es gibt an, ob das Message-Objekt keine sichtbaren Anlagen Endbenutzer hat.</span><span class="sxs-lookup"><span data-stu-id="86331-118">It indicates whether the message object has no end-user visible attachments.</span></span> <span data-ttu-id="86331-119">Diese Eigenschaft kann nicht festgelegt werden; ist dies der Fall ist, wird davon ausgegangen, dass ein Standardwert FALSE.</span><span class="sxs-lookup"><span data-stu-id="86331-119">This property may be unset; if so, a default value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="86331-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="86331-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="86331-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="86331-121">Protocol specifications</span></span>

<span data-ttu-id="86331-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86331-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86331-123">Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="86331-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="86331-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86331-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86331-125">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="86331-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="86331-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="86331-126">Header files</span></span>

<span data-ttu-id="86331-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86331-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="86331-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="86331-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86331-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86331-129">See also</span></span>



[<span data-ttu-id="86331-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="86331-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86331-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="86331-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86331-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="86331-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86331-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="86331-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

