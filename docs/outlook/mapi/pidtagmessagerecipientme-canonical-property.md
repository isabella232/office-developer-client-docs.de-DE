---
title: PidTagMessageRecipientMe (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325620"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="8e711-103">PidTagMessageRecipientMe (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8e711-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="8e711-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e711-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e711-105">Enthält TRUE, wenn dieser Messagingbenutzer speziell als Primärempfänger (An), Als Carbon Copy (CC) oder Blind Carbon Copy (BCC)-Empfänger dieser Nachricht bezeichnet wird und nicht Teil einer Verteilerliste ist.</span><span class="sxs-lookup"><span data-stu-id="8e711-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e711-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8e711-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e711-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="8e711-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="8e711-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8e711-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e711-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="8e711-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="8e711-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8e711-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e711-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8e711-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8e711-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8e711-112">Area:</span></span>  <br/> |<span data-ttu-id="8e711-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="8e711-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e711-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8e711-114">Remarks</span></span>

<span data-ttu-id="8e711-115">Diese Eigenschaft bietet eine bequeme Möglichkeit, um zu bestimmen, ob der Benutzername explizit in der Empfängerliste angezeigt wird, ohne alle Einträge in der Liste zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="8e711-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="8e711-116">Der Wert stellt den logischen **#A0** der Eigenschaften **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) und **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) und der BCC-Informationen (die andernfalls nicht in einer Eigenschaft angezeigt werden) dar.</span><span class="sxs-lookup"><span data-stu-id="8e711-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="8e711-117">Diese Eigenschaft unterstützt die automatisierte Verarbeitung von empfangenen Nachrichten zum Zeitpunkt des Empfangs.</span><span class="sxs-lookup"><span data-stu-id="8e711-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="8e711-118">Bei der Option des Transportanbieters enthält diese Eigenschaft entweder FALSE oder ist nicht enthalten, wenn der Messagingbenutzer nicht direkt in der Empfängertabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="8e711-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="8e711-119">Die Nachrichtenzustellung, die aus der Erweiterung der Verteilerliste resultiert, führt nicht dazu, dass diese Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8e711-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="8e711-120">Der Empfänger muss explizit benannt werden.</span><span class="sxs-lookup"><span data-stu-id="8e711-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="8e711-121">Nicht gesendete Nachrichten legen diese **Eigenschaft,** PR_MESSAGE_CC_ME oder **PR_MESSAGE_TO_ME.**</span><span class="sxs-lookup"><span data-stu-id="8e711-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="8e711-122">Wenn sie in Nachrichten vorhanden sind, auf die der Benutzer in öffentlichen Nachrichtenspeichern, in privaten Speichern anderer Benutzer, in Dateien auf dem Datenträger oder eingebettet in andere empfangene Nachrichten zugreifen kann, enthalten sie in der Regel die Werte, auf die sie beim letzten Senden der Nachricht durch einen Transportanbieter festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="8e711-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8e711-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8e711-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e711-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8e711-124">Protocol specifications</span></span>

<span data-ttu-id="8e711-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e711-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e711-126">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8e711-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e711-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e711-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e711-128">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8e711-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e711-129">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="8e711-129">Header files</span></span>

<span data-ttu-id="8e711-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e711-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e711-131">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8e711-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e711-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8e711-132">Mapitags.h</span></span>
  
> <span data-ttu-id="8e711-133">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8e711-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e711-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e711-134">See also</span></span>



[<span data-ttu-id="8e711-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e711-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e711-136">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="8e711-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e711-137">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8e711-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e711-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8e711-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

