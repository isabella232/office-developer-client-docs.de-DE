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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331556"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="af9ff-103">PidLidSpamOriginalFolder (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="af9ff-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="af9ff-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af9ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af9ff-105">Gibt an, in welchem Ordner sich eine Nachricht befindet, bevor sie in den Junk-E-Mail-Ordner gefiltert wurde.</span><span class="sxs-lookup"><span data-stu-id="af9ff-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af9ff-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="af9ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af9ff-107">dispidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="af9ff-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="af9ff-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="af9ff-108">Property set:</span></span>  <br/> |<span data-ttu-id="af9ff-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="af9ff-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="af9ff-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="af9ff-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="af9ff-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="af9ff-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="af9ff-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="af9ff-112">Data type:</span></span>  <br/> |<span data-ttu-id="af9ff-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="af9ff-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="af9ff-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="af9ff-114">Area:</span></span>  <br/> |<span data-ttu-id="af9ff-115">Spam</span><span class="sxs-lookup"><span data-stu-id="af9ff-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af9ff-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="af9ff-116">Remarks</span></span>

<span data-ttu-id="af9ff-117">Der Wert dieser Eigenschaft ist die **EntryID** des Ordners, der die Nachricht enthielt, bevor sie verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="af9ff-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="af9ff-118">Diese Eigenschaft sollte festgelegt werden, wenn eine Nachricht als Spam gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="af9ff-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="af9ff-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="af9ff-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af9ff-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="af9ff-120">Protocol specifications</span></span>

<span data-ttu-id="af9ff-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af9ff-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af9ff-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="af9ff-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af9ff-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af9ff-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af9ff-124">Ermöglicht die Behandlung von Zulässig-/Sperrlisten und die Ermittlung von Junk-E-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="af9ff-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af9ff-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="af9ff-125">Header files</span></span>

<span data-ttu-id="af9ff-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af9ff-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="af9ff-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="af9ff-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af9ff-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af9ff-128">See also</span></span>



[<span data-ttu-id="af9ff-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="af9ff-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af9ff-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="af9ff-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af9ff-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="af9ff-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af9ff-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="af9ff-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

