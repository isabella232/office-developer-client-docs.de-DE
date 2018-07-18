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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 01d25614780f10f30d9e1314ea7f60ad3fbb4af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794365"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a><span data-ttu-id="cc4d2-103">PidTagExtendedRuleSizeLimit (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cc4d2-103">PidTagExtendedRuleSizeLimit Canonical Property</span></span>

  
  
<span data-ttu-id="cc4d2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cc4d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cc4d2-105">Enthält die maximale Größe in Bytes, die Benutzer für eine einzelne Regel "Erweiterte" aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-105">Contains the maximum size, in bytes, the user is allowed to accumulate for a single "extended" rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc4d2-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cc4d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc4d2-107">PR_EXTENDED_RULE_SIZE_LIMIT</span><span class="sxs-lookup"><span data-stu-id="cc4d2-107">PR_EXTENDED_RULE_SIZE_LIMIT</span></span>  <br/> |
|<span data-ttu-id="cc4d2-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="cc4d2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc4d2-109">0x0E9B</span><span class="sxs-lookup"><span data-stu-id="cc4d2-109">0x0E9B</span></span>  <br/> |
|<span data-ttu-id="cc4d2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cc4d2-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc4d2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cc4d2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cc4d2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cc4d2-112">Area:</span></span>  <br/> |<span data-ttu-id="cc4d2-113">Regeln</span><span class="sxs-lookup"><span data-stu-id="cc4d2-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc4d2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc4d2-114">Remarks</span></span>

<span data-ttu-id="cc4d2-115">Wenn diese Eigenschaft auf das Anmeldeobjekt festgelegt ist, sollte der Client die Größe der Eigenschaft **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) unter der von dieser Eigenschaft angegebene Wert beibehalten.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-115">If this property is set on the logon object, the client should keep the size of the **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) property under the value specified by this property.</span></span> <span data-ttu-id="cc4d2-116">Dagegen sollte der Server einen Fehler zurück, wenn der Client versucht, eine binäre Eigenschaft festlegen, die zu groß ist.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-116">Conversely, the server should return an error if the client does attempt to set a binary property that is too large.</span></span>
  
<span data-ttu-id="cc4d2-117">Informationen zu erweiterten Regeln finden Sie unter [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cc4d2-117">For information about extended rules, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cc4d2-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cc4d2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cc4d2-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cc4d2-119">Protocol specifications</span></span>

<span data-ttu-id="cc4d2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc4d2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc4d2-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cc4d2-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cc4d2-122">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cc4d2-123">Gibt die zulässige Vorgänge für die Hauptobjekte der Nachricht Store.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-123">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cc4d2-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="cc4d2-124">Header files</span></span>

<span data-ttu-id="cc4d2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc4d2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc4d2-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc4d2-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cc4d2-127">Mapitags.h</span></span>
  
> <span data-ttu-id="cc4d2-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cc4d2-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc4d2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc4d2-129">See also</span></span>



[<span data-ttu-id="cc4d2-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc4d2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc4d2-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc4d2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc4d2-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cc4d2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc4d2-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cc4d2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

