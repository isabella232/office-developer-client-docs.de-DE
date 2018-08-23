---
title: PidLidValidFlagStringProof (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: efbbffe184e965caae84db54383e1431dfb1a569
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585822"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="04e6a-103">PidLidValidFlagStringProof (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="04e6a-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="04e6a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04e6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04e6a-105">Überprüft, ob **DispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) den Wert der Eigenschaft von einem Agent festgelegt wurde, die den Wert der Eigenschaft **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) bekannt.</span><span class="sxs-lookup"><span data-stu-id="04e6a-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04e6a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="04e6a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04e6a-107">dispidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="04e6a-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="04e6a-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="04e6a-108">Property set:</span></span>  <br/> |<span data-ttu-id="04e6a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="04e6a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="04e6a-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="04e6a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="04e6a-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="04e6a-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="04e6a-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="04e6a-112">Data type:</span></span>  <br/> |<span data-ttu-id="04e6a-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="04e6a-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="04e6a-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="04e6a-114">Area:</span></span>  <br/> |<span data-ttu-id="04e6a-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="04e6a-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04e6a-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="04e6a-116">Remarks</span></span>

<span data-ttu-id="04e6a-117">Für nicht-sendable-Objekte (empfangene Nachrichten und nicht-Mail-Objekte) sollten Clients dieser Wert auf den Wert der **PR_MESSAGE_DELIVERY_TIME** festgelegt, wenn **DispidRequest**ändern.</span><span class="sxs-lookup"><span data-stu-id="04e6a-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="04e6a-118">Da der Wert der **PR_MESSAGE_DELIVERY_TIME** ist der Wert dieser Eigenschaft gleich dem Wert der **PR_MESSAGE_DELIVERY_TIME**vom Absender, vorhergesagt werden nicht möglich, ist es nach vernünftigem Ermessen sicher, dass der Wert der **DispidRequest** nicht der Absender der Nachricht stammen.</span><span class="sxs-lookup"><span data-stu-id="04e6a-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="04e6a-119">Ein Client kann entscheiden, wie den Wert der **DispidRequest** für den Endbenutzer basierend auf dem Ergebnis des Vergleichs gemäß den spezifischen Codezugriffssicherheits-Richtlinie des Clients zu präsentieren.</span><span class="sxs-lookup"><span data-stu-id="04e6a-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="04e6a-120">Wenn der Wert der **DispidRequest** aufgrund von das Vorhandensein eines Werts für **DispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) ignoriert wird, muss diese Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="04e6a-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="04e6a-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="04e6a-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="04e6a-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="04e6a-122">Protocol specifications</span></span>

<span data-ttu-id="04e6a-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04e6a-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04e6a-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="04e6a-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="04e6a-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04e6a-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04e6a-126">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="04e6a-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="04e6a-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="04e6a-127">Header files</span></span>

<span data-ttu-id="04e6a-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04e6a-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="04e6a-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="04e6a-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04e6a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04e6a-130">See also</span></span>



[<span data-ttu-id="04e6a-131">PidTagMessageDeliveryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="04e6a-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="04e6a-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="04e6a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04e6a-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="04e6a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04e6a-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="04e6a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04e6a-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="04e6a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

