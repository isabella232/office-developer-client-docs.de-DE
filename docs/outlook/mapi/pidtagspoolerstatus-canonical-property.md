---
title: Kanonische Pidtagspoolerstatus (-Eigenschaft
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
ms.openlocfilehash: 426d26cae147faf3f843ac547de9d205d766ac44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348209"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="eb1fa-103">Kanonische Pidtagspoolerstatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eb1fa-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="eb1fa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb1fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb1fa-105">Enthält den Status der Nachricht basierend auf Informationen, die dem MAPI-Spooler zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb1fa-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="eb1fa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb1fa-107">PR_SPOOLER_STATUS</span><span class="sxs-lookup"><span data-stu-id="eb1fa-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="eb1fa-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="eb1fa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eb1fa-109">0x0E10</span><span class="sxs-lookup"><span data-stu-id="eb1fa-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="eb1fa-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="eb1fa-110">Data type:</span></span>  <br/> |<span data-ttu-id="eb1fa-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="eb1fa-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="eb1fa-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="eb1fa-112">Area:</span></span>  <br/> |<span data-ttu-id="eb1fa-113">Nicht transmitable MAPI</span><span class="sxs-lookup"><span data-stu-id="eb1fa-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb1fa-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb1fa-114">Remarks</span></span>

<span data-ttu-id="eb1fa-115">Diese Eigenschaft wird von MAPI für Nachrichtenobjekte berechnet.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="eb1fa-116">Diese Eigenschaft wird nur für eingehende Nachrichten angezeigt und ist in allen anderen Fällen reserviert.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="eb1fa-117">Er gibt an, ob eine Nachricht an ihren endgültigen Standort übermittelt wurde oder ob ein nachrichtenverbindungs Anbieter die Nachricht möglicherweise beim erneuten Routing gelöscht hat.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="eb1fa-118">Client Anwendungen sollten diese Eigenschaft nie festlegen.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-118">Client applications should never set this property.</span></span> <span data-ttu-id="eb1fa-119">Für eine eingehende Nachricht kann ein Client oder Dienstanbieter [IMAPIProp::](imapiprop-getprops.md) GetProps für diese Eigenschaft aufrufen, um den Nachrichtenstatus zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="eb1fa-120">Der Wert S_OK gibt an, dass die Nachricht erfolgreich an den Nachrichtenspeicher übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="eb1fa-121">Der Wert MAPI_E_OBJECT_DELETED gibt an, dass die Nachricht gelöscht wurde und nie an den Speicher übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="eb1fa-122">Nachrichtenspeicher Anbieter sollten diese Eigenschaft für Nachrichten, Empfänger Tabellen und die Tabelle für ausgehende Warteschlangen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="eb1fa-123">Clients und Anbieter sollten in der Lage sein, Spalten der ausgehenden Warteschlangentabelle festzulegen und basierend auf dieser Eigenschaft einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eb1fa-124">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="eb1fa-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="eb1fa-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="eb1fa-125">Header files</span></span>

<span data-ttu-id="eb1fa-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="eb1fa-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb1fa-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="eb1fa-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="eb1fa-128">Mapitags.h</span></span>
  
> <span data-ttu-id="eb1fa-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb1fa-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb1fa-130">See also</span></span>



[<span data-ttu-id="eb1fa-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb1fa-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb1fa-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb1fa-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb1fa-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="eb1fa-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb1fa-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="eb1fa-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

