---
title: Kanonische PidTagMessageToMe-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 42aec7a8d617bdf1abd385add30d903efa2b73d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794621"
---
# <a name="pidtagmessagetome-canonical-property"></a><span data-ttu-id="5d2ad-103">Kanonische PidTagMessageToMe-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5d2ad-103">PidTagMessageToMe Canonical Property</span></span>

  
  
<span data-ttu-id="5d2ad-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d2ad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d2ad-105">Enthält True, wenn dieser Benutzer messaging speziell als primäre (Empfänger dieser Nachricht To heißt) und nicht Bestandteil einer Verteilerliste ist.</span><span class="sxs-lookup"><span data-stu-id="5d2ad-105">Contains TRUE if this messaging user is specifically named as a primary (To) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d2ad-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5d2ad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d2ad-107">PR_MESSAGE_TO_ME</span><span class="sxs-lookup"><span data-stu-id="5d2ad-107">PR_MESSAGE_TO_ME</span></span>  <br/> |
|<span data-ttu-id="5d2ad-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5d2ad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d2ad-109">0x0057</span><span class="sxs-lookup"><span data-stu-id="5d2ad-109">0x0057</span></span>  <br/> |
|<span data-ttu-id="5d2ad-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5d2ad-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d2ad-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5d2ad-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5d2ad-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5d2ad-112">Area:</span></span>  <br/> |<span data-ttu-id="5d2ad-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="5d2ad-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d2ad-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5d2ad-114">Remarks</span></span>

<span data-ttu-id="5d2ad-115">Diese Eigenschaft bietet eine bequeme Möglichkeit zum bestimmen, ob der Benutzername in der primären Empfängerliste explizit angezeigt wird, ohne alle Einträge in der Liste untersuchen.</span><span class="sxs-lookup"><span data-stu-id="5d2ad-115">This property provides a convenient way to determine whether the user name appears explicitly in the primary recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="5d2ad-116">Diese Eigenschaft unterstützt Sie auch automatisierte Verarbeitung von erhaltenen Nachrichten zum Zeitpunkt des Eingangs.</span><span class="sxs-lookup"><span data-stu-id="5d2ad-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="5d2ad-117">Unter der Adressbuchhierarchie verwenden wird, diese Eigenschaft enthält FALSE oder nicht einbezogen wird, wenn der messaging-Benutzer nicht direkt in der Empfänger Tabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="5d2ad-117">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="5d2ad-118">Nachrichtenübermittlung entsteht Verteilerlistenerweiterung oder eine Bezeichnung blind Carbon Copy, Blindkopie bewirkt keine diese Eigenschaft festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d2ad-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="5d2ad-119">Der Empfänger muss explizit heißen.</span><span class="sxs-lookup"><span data-stu-id="5d2ad-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="5d2ad-120">Nicht gesendete Nachrichten werden im Allgemeinen nicht **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) oder diese Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5d2ad-120">Unsent messages generally do not set the **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or this property.</span></span> <span data-ttu-id="5d2ad-121">Wenn sie in der Benutzer kann in öffentliche Nachrichtenspeichern, in der anderen Benutzer privaten Speicher, in den Dateien auf dem Datenträger, zugreifen oder in anderen empfangenen Nachrichten eingebettet, sie in der Regel die Werte, die festgelegt wurden, enthalten Nachrichten vorhanden sind der letzten Ausführung ein Transportdienstes übermittelt die Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="5d2ad-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5d2ad-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5d2ad-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d2ad-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5d2ad-123">Protocol specifications</span></span>

<span data-ttu-id="5d2ad-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d2ad-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d2ad-125">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5d2ad-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5d2ad-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d2ad-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d2ad-127">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5d2ad-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d2ad-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5d2ad-128">Header files</span></span>

<span data-ttu-id="5d2ad-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d2ad-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d2ad-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5d2ad-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="5d2ad-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5d2ad-131">Mapitags.h</span></span>
  
> <span data-ttu-id="5d2ad-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5d2ad-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d2ad-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d2ad-133">See also</span></span>



[<span data-ttu-id="5d2ad-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d2ad-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d2ad-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d2ad-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d2ad-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5d2ad-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d2ad-137">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5d2ad-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

