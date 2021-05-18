---
title: PidTagRuleProvider (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280605"
---
# <a name="pidtagruleprovider-canonical-property"></a><span data-ttu-id="61aac-103">PidTagRuleProvider (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="61aac-103">PidTagRuleProvider Canonical Property</span></span>

  
  
<span data-ttu-id="61aac-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61aac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61aac-105">Enthält den Namen der Anwendung, die eine Regel legt.</span><span class="sxs-lookup"><span data-stu-id="61aac-105">Contains the name of the application that sets a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="61aac-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="61aac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="61aac-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span><span class="sxs-lookup"><span data-stu-id="61aac-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span></span>  <br/> |
|<span data-ttu-id="61aac-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="61aac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="61aac-109">0x6681</span><span class="sxs-lookup"><span data-stu-id="61aac-109">0x6681</span></span>  <br/> |
|<span data-ttu-id="61aac-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="61aac-110">Data type:</span></span>  <br/> |<span data-ttu-id="61aac-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="61aac-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="61aac-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="61aac-112">Area:</span></span>  <br/> |<span data-ttu-id="61aac-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="61aac-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61aac-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="61aac-114">Remarks</span></span>

<span data-ttu-id="61aac-115">Verzögerte Aktionen benötigen diese Eigenschaften, um den Code zu identifizieren, der die Regelaktion interpretieren und ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="61aac-115">Deferred actions need these properties to identify the code that must interpret and execute the rule action.</span></span>
  
<span data-ttu-id="61aac-116">Regeln, die in Postfächern und Ordnern gespeichert sind, werden der Anwendung zugeordnet, der sie durch eine Regelanbieterzeichenfolge gehören.</span><span class="sxs-lookup"><span data-stu-id="61aac-116">Rules stored on mailboxes and folders are associated with the application that owns them by a rule provider string.</span></span> <span data-ttu-id="61aac-117">Ein Regelanbieter legt Regeln in einer Regeltabelle fest und verarbeitet diese.</span><span class="sxs-lookup"><span data-stu-id="61aac-117">A rule provider sets and handles rules in a rule table.</span></span> <span data-ttu-id="61aac-118">Es bietet auch eine Möglichkeit, alle zurückgestellten Aktionen zu behandeln, wenn solche Regeln festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="61aac-118">It also provides a means of handling any deferred actions if such rules are set.</span></span> <span data-ttu-id="61aac-119">Verzögerte Aktionen werden implizit vom Informationsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="61aac-119">Deferred actions are created implicitly by the information store.</span></span> <span data-ttu-id="61aac-120">Wenn ein Anbieter eine verzögerte Aktionsregel für Vorgänge in einen anderen Speicher verschiebt oder kopiert, muss er einen Handler zum Ausführen der Aktion bereitstellen, wenn die Regel ausgelöst wird und eine verzögerte Aktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="61aac-120">For move or copy operations to a different store, if a provider sets a deferred action rule, it must provide a handler to perform the action when the rule is fired and a deferred action is created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="61aac-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="61aac-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="61aac-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="61aac-122">Protocol specifications</span></span>

<span data-ttu-id="61aac-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61aac-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61aac-124">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="61aac-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="61aac-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61aac-125">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61aac-126">Bearbeitet eingehende E-Mail-Nachrichten auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="61aac-126">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="61aac-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="61aac-127">Header files</span></span>

<span data-ttu-id="61aac-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="61aac-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="61aac-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="61aac-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="61aac-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="61aac-130">Mapitags.h</span></span>
  
> <span data-ttu-id="61aac-131">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="61aac-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61aac-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61aac-132">See also</span></span>



[<span data-ttu-id="61aac-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="61aac-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="61aac-134">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="61aac-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="61aac-135">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="61aac-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="61aac-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="61aac-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

