---
title: PidTagMessageToMe (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToMe
api_type:
- HeaderDef
ms.assetid: aeb0fa71-f471-46c5-ad9c-f8afb3fed533
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96a0b010a8ba26a0c1b0cb409f1aaabb308a1c01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356196"
---
# <a name="pidtagmessagetome-canonical-property"></a><span data-ttu-id="ab176-103">PidTagMessageToMe (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ab176-103">PidTagMessageToMe Canonical Property</span></span>

  
  
<span data-ttu-id="ab176-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab176-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab176-105">Enthält TRUE, wenn dieser Messagingbenutzer ausdrücklich als primärer (An)-Empfänger dieser Nachricht benannt wird und nicht Teil einer Verteilerliste ist.</span><span class="sxs-lookup"><span data-stu-id="ab176-105">Contains TRUE if this messaging user is specifically named as a primary (To) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab176-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ab176-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab176-107">PR_MESSAGE_TO_ME</span><span class="sxs-lookup"><span data-stu-id="ab176-107">PR_MESSAGE_TO_ME</span></span>  <br/> |
|<span data-ttu-id="ab176-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ab176-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab176-109">0x0057</span><span class="sxs-lookup"><span data-stu-id="ab176-109">0x0057</span></span>  <br/> |
|<span data-ttu-id="ab176-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ab176-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab176-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ab176-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ab176-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ab176-112">Area:</span></span>  <br/> |<span data-ttu-id="ab176-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="ab176-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab176-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ab176-114">Remarks</span></span>

<span data-ttu-id="ab176-115">Diese Eigenschaft bietet eine bequeme Möglichkeit, um zu bestimmen, ob der Benutzername explizit in der primären Empfängerliste angezeigt wird, ohne alle Einträge in der Liste zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="ab176-115">This property provides a convenient way to determine whether the user name appears explicitly in the primary recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="ab176-116">Diese Eigenschaft hilft auch bei der automatisierten Behandlung von empfangenen Nachrichten zum Zeitpunkt des Empfangs.</span><span class="sxs-lookup"><span data-stu-id="ab176-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="ab176-117">Bei der Option des Transportanbieters enthält diese Eigenschaft entweder FALSE oder ist nicht enthalten, wenn der Messagingbenutzer nicht direkt in der Empfängertabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="ab176-117">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="ab176-118">Die Nachrichtenzustellung, die sich aus der Erweiterung der Verteilerliste oder einer Blindkopienbezeichnung ergibt, führt nicht dazu, dass diese Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ab176-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="ab176-119">Der Empfänger muss explizit benannt werden.</span><span class="sxs-lookup"><span data-stu-id="ab176-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="ab176-120">Nicht gesendete Nachrichten legen im Allgemeinen nicht die **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) oder diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ab176-120">Unsent messages generally do not set the **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or this property.</span></span> <span data-ttu-id="ab176-121">Wenn sie in Nachrichten vorhanden sind, auf die der Benutzer in öffentlichen Nachrichtenspeichern, in privaten Speichern anderer Benutzer, in Dateien auf dem Datenträger oder eingebettet in andere empfangene Nachrichten zugreifen kann, enthalten sie in der Regel die Werte, auf die sie beim letzten Senden der Nachricht durch einen Transportanbieter festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="ab176-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ab176-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ab176-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab176-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ab176-123">Protocol specifications</span></span>

<span data-ttu-id="ab176-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab176-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab176-125">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ab176-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ab176-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab176-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab176-127">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ab176-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab176-128">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ab176-128">Header files</span></span>

<span data-ttu-id="ab176-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab176-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab176-130">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ab176-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab176-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ab176-131">Mapitags.h</span></span>
  
> <span data-ttu-id="ab176-132">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ab176-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab176-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab176-133">See also</span></span>



[<span data-ttu-id="ab176-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab176-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab176-135">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ab176-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab176-136">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ab176-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab176-137">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ab176-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

