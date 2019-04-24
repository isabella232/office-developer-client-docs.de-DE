---
title: Kanonische Pidtagruleuserflags (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleUserFlags
api_type:
- COM
ms.assetid: c5dfb21f-b35e-4521-bf2b-e3d03d98d75d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 235efce341e1870f0c33917f1c6d42b021727308
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321343"
---
# <a name="pidtagruleuserflags-canonical-property"></a><span data-ttu-id="ffdf1-103">Kanonische Pidtagruleuserflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ffdf1-103">PidTagRuleUserFlags Canonical Property</span></span>

  
  
<span data-ttu-id="ffdf1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffdf1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffdf1-105">Diese Eigenschaft wird vom Client für die ausschließliche Verwendung des Clients festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ffdf1-105">This property is set by the client for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ffdf1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ffdf1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ffdf1-107">PR_RULE_USER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ffdf1-107">PR_RULE_USER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="ffdf1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ffdf1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ffdf1-109">0x6678</span><span class="sxs-lookup"><span data-stu-id="ffdf1-109">0x6678</span></span>  <br/> |
|<span data-ttu-id="ffdf1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ffdf1-110">Data type:</span></span>  <br/> |<span data-ttu-id="ffdf1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ffdf1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ffdf1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ffdf1-112">Area:</span></span>  <br/> |<span data-ttu-id="ffdf1-113">Server seitige Regeln</span><span class="sxs-lookup"><span data-stu-id="ffdf1-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffdf1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffdf1-114">Remarks</span></span>

<span data-ttu-id="ffdf1-115">Der Server muss den Wert dieser Eigenschaft beibehalten, wenn er vom Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ffdf1-115">The server must preserve the value of this property if it was set by the client.</span></span> <span data-ttu-id="ffdf1-116">Der Server muss es während der Regelauswertung und-Verarbeitung ignorieren.</span><span class="sxs-lookup"><span data-stu-id="ffdf1-116">The server must ignore it during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ffdf1-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ffdf1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ffdf1-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ffdf1-118">Protocol specifications</span></span>

<span data-ttu-id="ffdf1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffdf1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffdf1-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ffdf1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ffdf1-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffdf1-121">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffdf1-122">Bearbeitet eingehende e-Mail-Nachrichten auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="ffdf1-122">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ffdf1-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="ffdf1-123">Header files</span></span>

<span data-ttu-id="ffdf1-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ffdf1-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="ffdf1-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="ffdf1-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="ffdf1-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ffdf1-126">Mapitags.h</span></span>
  
> <span data-ttu-id="ffdf1-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ffdf1-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ffdf1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffdf1-128">See also</span></span>



[<span data-ttu-id="ffdf1-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ffdf1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ffdf1-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ffdf1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ffdf1-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ffdf1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ffdf1-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ffdf1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

