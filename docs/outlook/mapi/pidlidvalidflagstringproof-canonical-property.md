---
title: Kanonische Pidlidvalidflagstringproof (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315386"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a><span data-ttu-id="9198e-103">Kanonische Pidlidvalidflagstringproof (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9198e-103">PidLidValidFlagStringProof Canonical Property</span></span>

  
  
<span data-ttu-id="9198e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9198e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9198e-105">Überprüft, ob der Wert der **dispidRequest** ([pidlidflagrequest (](pidlidflagrequest-canonical-property.md))-Eigenschaft von einem Agent festgelegt wurde, der den Wert der **PR_MESSAGE_DELIVERY_TIME** ([pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md))-Eigenschaft kannte.</span><span class="sxs-lookup"><span data-stu-id="9198e-105">Validates whether the **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) property's value was set by an agent who knew the value of the **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9198e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9198e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9198e-107">dispidValidFlagStringProof</span><span class="sxs-lookup"><span data-stu-id="9198e-107">dispidValidFlagStringProof</span></span>  <br/> |
|<span data-ttu-id="9198e-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="9198e-108">Property set:</span></span>  <br/> |<span data-ttu-id="9198e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="9198e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9198e-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="9198e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9198e-111">0x000085BF</span><span class="sxs-lookup"><span data-stu-id="9198e-111">0x000085BF</span></span>  <br/> |
|<span data-ttu-id="9198e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9198e-112">Data type:</span></span>  <br/> |<span data-ttu-id="9198e-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="9198e-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="9198e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9198e-114">Area:</span></span>  <br/> |<span data-ttu-id="9198e-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="9198e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9198e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9198e-116">Remarks</span></span>

<span data-ttu-id="9198e-117">Bei nicht-sendenden Objekten (empfangene e-Mails und nicht-e-Mail-Objekte) sollten Clients diesen Wert beim Ändern von **dispidRequest**auf den Wert von **PR_MESSAGE_DELIVERY_TIME** festlegen.</span><span class="sxs-lookup"><span data-stu-id="9198e-117">On non-sendable objects (received mail and non-mail objects), clients should set this value to the value of **PR_MESSAGE_DELIVERY_TIME** when modifying **dispidRequest**.</span></span>
  
<span data-ttu-id="9198e-118">Da der Wert von **PR_MESSAGE_DELIVERY_TIME** nicht vom Absender vorhergesagt werden kann, ist der Wert dieser Eigenschaft gleich dem Wert von **PR_MESSAGE_DELIVERY_TIME**, aber es ist ziemlich sicher, dass der Wert von **dispidRequest** nicht vom Absender der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9198e-118">Since the value of **PR_MESSAGE_DELIVERY_TIME** cannot be predicted by the sender, if the value of this property is equal to the value of **PR_MESSAGE_DELIVERY_TIME**, it is reasonably certain that the value of **dispidRequest** did not originate from the sender of the message.</span></span> <span data-ttu-id="9198e-119">Ein Client kann entscheiden, wie der Endbenutzer den Wert von **dispidRequest** basierend auf dem Ergebnis dieses Vergleichs gemäß der spezifischen Sicherheitsrichtlinie des Clients darstellen soll.</span><span class="sxs-lookup"><span data-stu-id="9198e-119">A client can decide how to present the value of **dispidRequest** to the end user based on the result of this comparison in accordance with the specific security policy of the client.</span></span> <span data-ttu-id="9198e-120">Wenn der Wert von **dispidRequest** aufgrund des Vorhandenseins eines Werts für **dispidFlagStringEnum** ([pidlidflagstring (](pidlidflagstring-canonical-property.md)) ignoriert wird, muss diese Eigenschaft ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="9198e-120">If the value of **dispidRequest** is ignored due to the presence of a value for **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), this property must be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9198e-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9198e-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9198e-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9198e-122">Protocol specifications</span></span>

<span data-ttu-id="9198e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9198e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9198e-124">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="9198e-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9198e-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9198e-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9198e-126">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.</span><span class="sxs-lookup"><span data-stu-id="9198e-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9198e-127">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="9198e-127">Header files</span></span>

<span data-ttu-id="9198e-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9198e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="9198e-129">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="9198e-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9198e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9198e-130">See also</span></span>



[<span data-ttu-id="9198e-131">Kanonische Pidtagmessagedeliverytime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9198e-131">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)


[<span data-ttu-id="9198e-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9198e-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9198e-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9198e-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9198e-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9198e-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9198e-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9198e-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

