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
ms.openlocfilehash: 639d5e96eb56fb543d6a6026b1c9400631cee819
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593340"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="54f1b-103">PidLidSpamOriginalFolder (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="54f1b-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="54f1b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54f1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54f1b-105">Gibt an, welcher Ordner eine Nachricht in vorher in den junk-e-Mail-Ordner gefiltert wurde.</span><span class="sxs-lookup"><span data-stu-id="54f1b-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54f1b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="54f1b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54f1b-107">dispidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="54f1b-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="54f1b-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="54f1b-108">Property set:</span></span>  <br/> |<span data-ttu-id="54f1b-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="54f1b-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="54f1b-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="54f1b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="54f1b-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="54f1b-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="54f1b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="54f1b-112">Data type:</span></span>  <br/> |<span data-ttu-id="54f1b-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="54f1b-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="54f1b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="54f1b-114">Area:</span></span>  <br/> |<span data-ttu-id="54f1b-115">Spam</span><span class="sxs-lookup"><span data-stu-id="54f1b-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54f1b-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="54f1b-116">Remarks</span></span>

<span data-ttu-id="54f1b-117">Der Wert dieser Eigenschaft ist die **EntryID** des Ordners, der die Nachricht enthalten, bevor sie verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="54f1b-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="54f1b-118">Diese Eigenschaft muss festgelegt werden, wenn eine Nachricht als Spam gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="54f1b-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="54f1b-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="54f1b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="54f1b-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="54f1b-120">Protocol specifications</span></span>

<span data-ttu-id="54f1b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54f1b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54f1b-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="54f1b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="54f1b-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54f1b-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54f1b-124">Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="54f1b-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="54f1b-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="54f1b-125">Header files</span></span>

<span data-ttu-id="54f1b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54f1b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="54f1b-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="54f1b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54f1b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54f1b-128">See also</span></span>



[<span data-ttu-id="54f1b-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54f1b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54f1b-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54f1b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54f1b-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="54f1b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54f1b-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="54f1b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

