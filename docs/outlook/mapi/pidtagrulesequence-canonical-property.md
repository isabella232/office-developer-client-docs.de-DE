---
title: PidTagRuleSequence (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleSequence
api_type:
- COM
ms.assetid: c42f2539-f7d6-464a-a82c-f0ac51823168
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 29579f91a85e74b568610c749d9408f813f157f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795065"
---
# <a name="pidtagrulesequence-canonical-property"></a><span data-ttu-id="479b0-103">PidTagRuleSequence (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="479b0-103">PidTagRuleSequence Canonical Property</span></span>

  
  
<span data-ttu-id="479b0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="479b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="479b0-105">Ein Wert verwendet, um die Reihenfolge zu bestimmen, in der Regeln ausgewertet und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="479b0-105">A value used to determine the order in which rules are evaluated and executed.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="479b0-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="479b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="479b0-107">PR_RULE_SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="479b0-107">PR_RULE_SEQUENCE</span></span>  <br/> |
|<span data-ttu-id="479b0-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="479b0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="479b0-109">0x6676</span><span class="sxs-lookup"><span data-stu-id="479b0-109">0x6676</span></span>  <br/> |
|<span data-ttu-id="479b0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="479b0-110">Data type:</span></span>  <br/> |<span data-ttu-id="479b0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="479b0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="479b0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="479b0-112">Area:</span></span>  <br/> |<span data-ttu-id="479b0-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="479b0-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="479b0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="479b0-114">Remarks</span></span>

<span data-ttu-id="479b0-115">Regeln werden in der Reihenfolge ihrer aufsteigender Reihenfolge der dieser Wert ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="479b0-115">Rules are evaluated in sequence according to the increasing order of this value.</span></span> <span data-ttu-id="479b0-116">Die Auswertungsreihenfolge für Regeln mit den gleichen Wert in dieser Eigenschaft ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="479b0-116">The evaluation order for rules that have the same value in this property is undefined.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="479b0-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="479b0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="479b0-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="479b0-118">Protocol specifications</span></span>

<span data-ttu-id="479b0-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="479b0-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="479b0-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="479b0-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="479b0-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="479b0-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="479b0-122">Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="479b0-122">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="479b0-123">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="479b0-123">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="479b0-124">Gibt die Methoden zum Verbinden mit und Postfächer als Stellvertreter und Interaktionen mit Nachrichten und Kalenderelemente konfigurieren, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="479b0-124">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="479b0-125">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="479b0-125">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="479b0-126">Zulässige Vorgänge für die Hauptobjekte-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="479b0-126">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="479b0-127">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="479b0-127">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="479b0-128">Gibt die zulässige Vorgänge für die Hauptobjekte der Nachricht Store.</span><span class="sxs-lookup"><span data-stu-id="479b0-128">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="479b0-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="479b0-129">Header files</span></span>

<span data-ttu-id="479b0-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="479b0-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="479b0-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="479b0-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="479b0-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="479b0-132">Mapitags.h</span></span>
  
> <span data-ttu-id="479b0-133">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="479b0-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="479b0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="479b0-134">See also</span></span>



[<span data-ttu-id="479b0-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="479b0-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="479b0-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="479b0-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="479b0-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="479b0-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="479b0-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="479b0-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

