---
title: PidTagSpoolerStatus (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 426d26cae147faf3f843ac547de9d205d766ac44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408677"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="25655-103">PidTagSpoolerStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="25655-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="25655-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25655-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25655-105">Enthält den Status der Nachricht basierend auf Informationen, die für den MAPI-Spooler verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="25655-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25655-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="25655-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25655-107">PR_SPOOLER_STATUS</span><span class="sxs-lookup"><span data-stu-id="25655-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="25655-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="25655-108">Identifier:</span></span>  <br/> |<span data-ttu-id="25655-109">0x0E10</span><span class="sxs-lookup"><span data-stu-id="25655-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="25655-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="25655-110">Data type:</span></span>  <br/> |<span data-ttu-id="25655-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="25655-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="25655-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="25655-112">Area:</span></span>  <br/> |<span data-ttu-id="25655-113">MAPI nicht durchlässig</span><span class="sxs-lookup"><span data-stu-id="25655-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25655-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="25655-114">Remarks</span></span>

<span data-ttu-id="25655-115">Diese Eigenschaft wird von MAPI für Nachrichtenobjekte berechnet.</span><span class="sxs-lookup"><span data-stu-id="25655-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="25655-116">Diese Eigenschaft wird nur für eingehende Nachrichten angezeigt und ist in allen anderen Fällen reserviert.</span><span class="sxs-lookup"><span data-stu-id="25655-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="25655-117">Es gibt an, ob eine Nachricht an den endgültigen Speicherort zugestellt wurde oder ob ein Messaging-Hook-Anbieter die Nachricht beim Umleitungsrouting möglicherweise gelöscht hat.</span><span class="sxs-lookup"><span data-stu-id="25655-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="25655-118">Clientanwendungen sollten diese Eigenschaft nie festlegen.</span><span class="sxs-lookup"><span data-stu-id="25655-118">Client applications should never set this property.</span></span> <span data-ttu-id="25655-119">Bei einer eingehenden Nachricht kann ein Client oder Dienstanbieter [IMAPIProp::GetProps](imapiprop-getprops.md) für diese Eigenschaft aufrufen, um den Nachrichtenstatus zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="25655-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="25655-120">Der Wert S_OK an, dass die Nachricht erfolgreich an den Nachrichtenspeicher übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="25655-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="25655-121">Der Wert MAPI_E_OBJECT_DELETED an, dass die Nachricht gelöscht wurde und niemals für den Speicher gebunden wurde.</span><span class="sxs-lookup"><span data-stu-id="25655-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="25655-122">Nachrichtenspeicheranbieter sollten diese Eigenschaft für Nachrichten, Empfängertabellen und die Tabelle für ausgehende Warteschlangen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="25655-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="25655-123">Clients und Anbieter sollten in der Lage sein, Spalten in der Tabelle für ausgehende Warteschlangen zu setzen und basierend auf dieser Eigenschaft einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="25655-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="25655-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="25655-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="25655-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="25655-125">Header files</span></span>

<span data-ttu-id="25655-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25655-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="25655-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="25655-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="25655-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="25655-128">Mapitags.h</span></span>
  
> <span data-ttu-id="25655-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="25655-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25655-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25655-130">See also</span></span>



[<span data-ttu-id="25655-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="25655-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25655-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="25655-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25655-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="25655-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25655-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="25655-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

