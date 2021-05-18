---
title: PidTagExtendedRuleSizeLimit (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 347d84021b7e9ece925acb99e8b539ba608337a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316345"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a><span data-ttu-id="32e2e-103">PidTagExtendedRuleSizeLimit (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="32e2e-103">PidTagExtendedRuleSizeLimit Canonical Property</span></span>

  
  
<span data-ttu-id="32e2e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32e2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32e2e-105">Enthält die maximale Größe in Byte, die der Benutzer für eine einzelne "erweiterte" Regel sammeln darf.</span><span class="sxs-lookup"><span data-stu-id="32e2e-105">Contains the maximum size, in bytes, the user is allowed to accumulate for a single "extended" rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="32e2e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="32e2e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="32e2e-107">PR_EXTENDED_RULE_SIZE_LIMIT</span><span class="sxs-lookup"><span data-stu-id="32e2e-107">PR_EXTENDED_RULE_SIZE_LIMIT</span></span>  <br/> |
|<span data-ttu-id="32e2e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="32e2e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="32e2e-109">0x0E9B</span><span class="sxs-lookup"><span data-stu-id="32e2e-109">0x0E9B</span></span>  <br/> |
|<span data-ttu-id="32e2e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="32e2e-110">Data type:</span></span>  <br/> |<span data-ttu-id="32e2e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="32e2e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="32e2e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="32e2e-112">Area:</span></span>  <br/> |<span data-ttu-id="32e2e-113">Regeln</span><span class="sxs-lookup"><span data-stu-id="32e2e-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32e2e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="32e2e-114">Remarks</span></span>

<span data-ttu-id="32e2e-115">Wenn diese Eigenschaft für das Anmeldeobjekt festgelegt ist, sollte der Client die Größe der **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) -Eigenschaft unter dem durch diese Eigenschaft angegebenen Wert halten.</span><span class="sxs-lookup"><span data-stu-id="32e2e-115">If this property is set on the logon object, the client should keep the size of the **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) property under the value specified by this property.</span></span> <span data-ttu-id="32e2e-116">Umgekehrt sollte der Server einen Fehler zurückgeben, wenn der Client versucht, eine zu große binäre Eigenschaft zu setzen.</span><span class="sxs-lookup"><span data-stu-id="32e2e-116">Conversely, the server should return an error if the client does attempt to set a binary property that is too large.</span></span>
  
<span data-ttu-id="32e2e-117">Weitere Informationen zu erweiterten Regeln finden Sie [unter [MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="32e2e-117">For information about extended rules, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="32e2e-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="32e2e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="32e2e-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="32e2e-119">Protocol specifications</span></span>

<span data-ttu-id="32e2e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32e2e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32e2e-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="32e2e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="32e2e-122">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32e2e-122">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32e2e-123">Gibt zulässige Vorgänge für die Zentralen Nachrichtenspeicherobjekte an.</span><span class="sxs-lookup"><span data-stu-id="32e2e-123">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="32e2e-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="32e2e-124">Header files</span></span>

<span data-ttu-id="32e2e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="32e2e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="32e2e-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="32e2e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="32e2e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="32e2e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="32e2e-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="32e2e-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="32e2e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32e2e-129">See also</span></span>



[<span data-ttu-id="32e2e-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="32e2e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="32e2e-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="32e2e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="32e2e-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="32e2e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="32e2e-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="32e2e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

