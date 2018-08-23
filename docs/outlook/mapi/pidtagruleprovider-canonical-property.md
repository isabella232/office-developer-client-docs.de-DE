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
ms.openlocfilehash: 3a80669f3d8f3d262cc8787f60efb3bc4b24d4b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589441"
---
# <a name="pidtagruleprovider-canonical-property"></a><span data-ttu-id="e2620-103">PidTagRuleProvider (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e2620-103">PidTagRuleProvider Canonical Property</span></span>

  
  
<span data-ttu-id="e2620-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2620-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2620-105">Enthält den Namen der Anwendung, die eine Regel festlegt.</span><span class="sxs-lookup"><span data-stu-id="e2620-105">Contains the name of the application that sets a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2620-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e2620-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2620-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A, PR_RULE_PROVIDER_W</span><span class="sxs-lookup"><span data-stu-id="e2620-107">PR_RULE_PROVIDER, PR_RULE_PROVIDER_A , PR_RULE_PROVIDER_W</span></span>  <br/> |
|<span data-ttu-id="e2620-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e2620-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2620-109">0x6681</span><span class="sxs-lookup"><span data-stu-id="e2620-109">0x6681</span></span>  <br/> |
|<span data-ttu-id="e2620-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e2620-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2620-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2620-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e2620-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e2620-112">Area:</span></span>  <br/> |<span data-ttu-id="e2620-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="e2620-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2620-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="e2620-114">Remarks</span></span>

<span data-ttu-id="e2620-115">Zurückgestellt Aktionen müssen diese Eigenschaften zum Identifizieren des Codes, die interpretiert werden und die Regelaktion ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="e2620-115">Deferred actions need these properties to identify the code that must interpret and execute the rule action.</span></span>
  
<span data-ttu-id="e2620-116">Regeln für Postfächer und Ordner gespeichert sind zugeordnet, mit der Anwendung, die sie von einer Regel Anbieterzeichenfolge besitzt.</span><span class="sxs-lookup"><span data-stu-id="e2620-116">Rules stored on mailboxes and folders are associated with the application that owns them by a rule provider string.</span></span> <span data-ttu-id="e2620-117">Ein Anbieter Regel festgelegt und Regeln in einer Regeltabelle behandelt.</span><span class="sxs-lookup"><span data-stu-id="e2620-117">A rule provider sets and handles rules in a rule table.</span></span> <span data-ttu-id="e2620-118">Es bietet auch eine Möglichkeit, alle zurückgestellten Aktionen verarbeiten, wenn solche Regeln festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e2620-118">It also provides a means of handling any deferred actions if such rules are set.</span></span> <span data-ttu-id="e2620-119">Zurückgestellte Aktionen werden von den Informationsspeicher implizit erstellt.</span><span class="sxs-lookup"><span data-stu-id="e2620-119">Deferred actions are created implicitly by the information store.</span></span> <span data-ttu-id="e2620-120">Für Vorgänge verschieben oder Kopieren auf einen anderen Wenn ein Anbieter in der Regel verzögerter Aktion Legt fest, muss es einen Ereignishandler bereitstellen, um die Aktion ausführen, wenn die Regel ausgelöst wird, und eine verzögerte Aktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e2620-120">For move or copy operations to a different store, if a provider sets a deferred action rule, it must provide a handler to perform the action when the rule is fired and a deferred action is created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2620-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e2620-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2620-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e2620-122">Protocol specifications</span></span>

<span data-ttu-id="e2620-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2620-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2620-124">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e2620-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2620-125">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2620-125">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2620-126">Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="e2620-126">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2620-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e2620-127">Header files</span></span>

<span data-ttu-id="e2620-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2620-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2620-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e2620-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2620-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e2620-130">Mapitags.h</span></span>
  
> <span data-ttu-id="e2620-131">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e2620-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2620-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2620-132">See also</span></span>



[<span data-ttu-id="e2620-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2620-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2620-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2620-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2620-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e2620-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2620-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e2620-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

