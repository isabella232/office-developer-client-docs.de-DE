---
title: PidLidSpamOriginalFolder (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSpamOriginalFolder
api_type:
- COM
ms.assetid: 45846fe3-7ab3-4019-98bb-fe615889c31c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 561008782e7c1ffb8bc71cf4e3bc17befe69bbca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387846"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="5d692-103">PidLidSpamOriginalFolder (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5d692-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="5d692-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d692-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d692-105">Gibt an, welcher Ordner eine Nachricht in vorher in den junk-e-Mail-Ordner gefiltert wurde.</span><span class="sxs-lookup"><span data-stu-id="5d692-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d692-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5d692-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d692-107">dispidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="5d692-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="5d692-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="5d692-108">Property set:</span></span>  <br/> |<span data-ttu-id="5d692-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5d692-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5d692-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="5d692-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5d692-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="5d692-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="5d692-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5d692-112">Data type:</span></span>  <br/> |<span data-ttu-id="5d692-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5d692-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5d692-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5d692-114">Area:</span></span>  <br/> |<span data-ttu-id="5d692-115">Spam</span><span class="sxs-lookup"><span data-stu-id="5d692-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d692-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5d692-116">Remarks</span></span>

<span data-ttu-id="5d692-117">Der Wert dieser Eigenschaft ist die **EntryID** des Ordners, der die Nachricht enthalten, bevor sie verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="5d692-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="5d692-118">Diese Eigenschaft muss festgelegt werden, wenn eine Nachricht als Spam gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="5d692-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5d692-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5d692-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d692-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5d692-120">Protocol specifications</span></span>

<span data-ttu-id="5d692-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d692-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d692-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5d692-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5d692-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d692-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d692-124">Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="5d692-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d692-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5d692-125">Header files</span></span>

<span data-ttu-id="5d692-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d692-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d692-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5d692-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d692-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d692-128">See also</span></span>



[<span data-ttu-id="5d692-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d692-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d692-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d692-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d692-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5d692-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d692-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5d692-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

