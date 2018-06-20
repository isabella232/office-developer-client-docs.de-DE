---
title: Kanonische PidTagResponsibility-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9dba26ab6948d7190521ff31a8732c4b058ab7c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794985"
---
# <a name="pidtagresponsibility-canonical-property"></a><span data-ttu-id="46147-103">Kanonische PidTagResponsibility-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="46147-103">PidTagResponsibility Canonical Property</span></span>

  
  
<span data-ttu-id="46147-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46147-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46147-105">Enthält TRUE, wenn einige Adressbuchhierarchie bereits Verantwortung zur Übermittlung der Nachricht mit dieser Empfänger, und FALSE, wenn die Warteschlange MAPI berücksichtigt, dass dieser Transportdienst Verantwortung akzeptieren sollte angenommen hat.</span><span class="sxs-lookup"><span data-stu-id="46147-105">Contains TRUE if some transport provider has already accepted responsibility for delivering the message to this recipient, and FALSE if the MAPI spooler considers that this transport provider should accept responsibility.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46147-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="46147-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46147-107">PR_RESPONSIBILITY</span><span class="sxs-lookup"><span data-stu-id="46147-107">PR_RESPONSIBILITY</span></span>  <br/> |
|<span data-ttu-id="46147-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="46147-108">Identifier:</span></span>  <br/> |<span data-ttu-id="46147-109">0x0E0F</span><span class="sxs-lookup"><span data-stu-id="46147-109">0x0E0F</span></span>  <br/> |
|<span data-ttu-id="46147-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="46147-110">Data type:</span></span>  <br/> |<span data-ttu-id="46147-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="46147-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="46147-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="46147-112">Area:</span></span>  <br/> |<span data-ttu-id="46147-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="46147-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46147-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="46147-114">Remarks</span></span>

<span data-ttu-id="46147-115">Wenn die MAPI-Warteschlange eine ausgehende Nachricht zu einem Transportanbieter über [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), stellt wird diese Eigenschaft auf FALSE für alle Empfänger für die die MAPI-Warteschlange, Adressbuchhierarchie verantwortlich und TRUE für alle berücksichtigt andere Empfänger.</span><span class="sxs-lookup"><span data-stu-id="46147-115">When the MAPI spooler presents an outbound message to a transport provider, through [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), it sets this property to FALSE for all recipients for which the MAPI spooler considers that transport provider responsible, and TRUE for all other recipients.</span></span> <span data-ttu-id="46147-116">Der Adressbuchhierarchie sollten alle Empfänger **PR_RESPONSIBILITY** auf FALSE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="46147-116">The transport provider should attempt to handle all recipients with **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="46147-117">Nach dem erfolgreichen Senden oder nicht eindeutig an einen Empfänger senden sollte der Adressbuchhierarchie legen Sie diese Eigenschaft auf true fest, in der Quellnachricht, um anzugeben, dass er die Verantwortung für diesen Empfänger angenommen hat.</span><span class="sxs-lookup"><span data-stu-id="46147-117">After successfully sending, or conclusively failing to send, to a recipient, the transport provider should set this property to TRUE in the source message to indicate that it has accepted responsibility for that recipient.</span></span> 
  
<span data-ttu-id="46147-118">Wenn nach der Prüfung eines Empfängers, ein Transportdienstes entscheidet, dass es keine sollte nicht behandelt, sollte der Adressbuchhierarchie **PR_RESPONSIBILITY** Set auf false festgelegt lassen.</span><span class="sxs-lookup"><span data-stu-id="46147-118">If, after examining a recipient, a transport provider decides that it cannot or should not handle it, the transport provider should leave **PR_RESPONSIBILITY** set to FALSE.</span></span> <span data-ttu-id="46147-119">Die MAPI-Warteschlange sieht dann für einen anderen Transportanbieter, die diesen Empfänger verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="46147-119">The MAPI spooler will then look for another transport provider that can handle that recipient.</span></span> <span data-ttu-id="46147-120">Die MAPI-Warteschlange erstellt einen Unzustellbarkeitsbericht letztlich für alle Empfänger für die keine Adressbuchhierarchie Verantwortung annimmt.</span><span class="sxs-lookup"><span data-stu-id="46147-120">The MAPI spooler ultimately creates a nondelivery report for any recipients for which no transport provider accepts responsibility.</span></span> 
  
<span data-ttu-id="46147-121">Wenn der Adressbuchhierarchie versucht und die Nachricht nicht zustellen fehlschlägt, sollten sie die [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode, um die Gründe für den Fehler MAPI mit, aufrufen, damit MAPI einen Unzustellbarkeitsbericht generieren kann.</span><span class="sxs-lookup"><span data-stu-id="46147-121">If the transport provider attempts and fails to deliver the message, it should call the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate to MAPI the reasons for the failure, so that MAPI can generate a nondelivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="46147-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="46147-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46147-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="46147-123">Protocol specifications</span></span>

<span data-ttu-id="46147-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46147-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46147-125">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="46147-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="46147-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46147-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46147-127">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="46147-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46147-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="46147-128">Header files</span></span>

<span data-ttu-id="46147-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46147-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="46147-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="46147-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="46147-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="46147-131">Mapitags.h</span></span>
  
> <span data-ttu-id="46147-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="46147-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46147-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46147-133">See also</span></span>



[<span data-ttu-id="46147-134">Kanonische PidTagDeleteAfterSubmit-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="46147-134">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)


[<span data-ttu-id="46147-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46147-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46147-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46147-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46147-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="46147-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46147-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="46147-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

