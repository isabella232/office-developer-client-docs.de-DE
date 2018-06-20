---
title: Kanonische PidTagSpoolerStatus-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: df52f668e91b707c0436b394186b27fdbb3a5dbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795197"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="dc999-103">Kanonische PidTagSpoolerStatus-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dc999-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="dc999-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc999-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc999-105">Enthält den Status der Nachricht basierend auf Informationen, die für die MAPI-Warteschlange verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="dc999-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc999-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dc999-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc999-107">PR_SPOOLER_STATUS</span><span class="sxs-lookup"><span data-stu-id="dc999-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="dc999-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="dc999-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dc999-109">0x0E10</span><span class="sxs-lookup"><span data-stu-id="dc999-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="dc999-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dc999-110">Data type:</span></span>  <br/> |<span data-ttu-id="dc999-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dc999-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dc999-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dc999-112">Area:</span></span>  <br/> |<span data-ttu-id="dc999-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="dc999-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc999-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dc999-114">Remarks</span></span>

<span data-ttu-id="dc999-115">Diese Eigenschaft wird auf Message Objekte MAPI berechnet.</span><span class="sxs-lookup"><span data-stu-id="dc999-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="dc999-116">Diese Eigenschaft wird auf eingehende Nachrichten nur angezeigt und ist in allen anderen Fällen reserviert.</span><span class="sxs-lookup"><span data-stu-id="dc999-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="dc999-117">Es gibt an, unabhängig davon, ob eine Nachricht an seinem endgültigen Speicherort übermittelt wurde, oder gibt an, ob ein messaging Hook Anbieter potenziell die Nachricht beim gelöscht erneutes es.</span><span class="sxs-lookup"><span data-stu-id="dc999-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="dc999-118">Clientanwendungen sollten diese Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="dc999-118">Client applications should never set this property.</span></span> <span data-ttu-id="dc999-119">Für eine eingehende Nachricht kann ein Client oder Dienstanbieter [IMAPIProp::GetProps](imapiprop-getprops.md) für diese Eigenschaft zum Bestimmen des Nachrichtenstatus aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dc999-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="dc999-120">Der Wert S_OK gibt an, dass die Nachricht erfolgreich an den Nachrichtenspeicher übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="dc999-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="dc999-121">Der Wert MAPI_E_OBJECT_DELETED gibt an, dass die Nachricht gelöscht wurde und an den Store nie zugesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="dc999-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="dc999-122">Nachricht Anbieter sollte diese Eigenschaft auf Nachrichten, Empfänger Tabellen und der ausgehende Warteschlangentabelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dc999-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="dc999-123">Clients und Anbieter sollte können Spalten in der ausgehenden Warteschlangentabelle festgelegt und einschränken können basierend auf dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc999-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dc999-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dc999-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="dc999-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="dc999-125">Header files</span></span>

<span data-ttu-id="dc999-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc999-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc999-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="dc999-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="dc999-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dc999-128">Mapitags.h</span></span>
  
> <span data-ttu-id="dc999-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dc999-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc999-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc999-130">See also</span></span>



[<span data-ttu-id="dc999-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc999-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc999-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc999-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc999-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dc999-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc999-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dc999-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

