---
title: PidTagMessageCcMe (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 82d043adfe6e480b4d490f44ad89d73535c80c9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569778"
---
# <a name="pidtagmessageccme-canonical-property"></a><span data-ttu-id="62884-103">PidTagMessageCcMe (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="62884-103">PidTagMessageCcMe Canonical Property</span></span>

  
  
<span data-ttu-id="62884-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62884-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62884-105">Enthält True, wenn dieser Benutzer messaging speziell als Kopie (CC) Empfänger dieser Nachricht heißt und nicht Bestandteil einer Verteilerliste ist.</span><span class="sxs-lookup"><span data-stu-id="62884-105">Contains TRUE if this messaging user is specifically named as a carbon copy (CC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="62884-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="62884-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62884-107">PR_MESSAGE_CC_ME</span><span class="sxs-lookup"><span data-stu-id="62884-107">PR_MESSAGE_CC_ME</span></span>  <br/> |
|<span data-ttu-id="62884-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="62884-108">Identifier:</span></span>  <br/> |<span data-ttu-id="62884-109">0x0058</span><span class="sxs-lookup"><span data-stu-id="62884-109">0x0058</span></span>  <br/> |
|<span data-ttu-id="62884-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="62884-110">Data type:</span></span>  <br/> |<span data-ttu-id="62884-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="62884-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="62884-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="62884-112">Area:</span></span>  <br/> |<span data-ttu-id="62884-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="62884-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62884-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="62884-114">Remarks</span></span>

<span data-ttu-id="62884-115">Diese Eigenschaft bietet eine bequeme Möglichkeit zum bestimmen, ob der Benutzername in der Empfängerliste Carbon Copy, Blindkopie, explizit angezeigt wird, ohne Betrachtung der alle Einträge in der Liste.</span><span class="sxs-lookup"><span data-stu-id="62884-115">This property provides a convenient way to determine whether the user name appears explicitly in the carbon copy recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="62884-116">Diese Eigenschaft unterstützt Sie auch automatisierte Verarbeitung von erhaltenen Nachrichten zum Zeitpunkt des Eingangs.</span><span class="sxs-lookup"><span data-stu-id="62884-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="62884-117">Unter der Adressbuchhierarchie verwenden wird, diese Eigenschaft enthält FALSE oder ist nicht festgelegt, wenn der messaging-Benutzer nicht direkt in der Empfänger Tabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="62884-117">At the transport provider's option, this property either contains FALSE or is not set if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="62884-118">Nachrichtenübermittlung entsteht Verteilerlistenerweiterung oder eine Bezeichnung blind Carbon Copy, Blindkopie bewirkt keine diese Eigenschaft festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="62884-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="62884-119">Der Empfänger muss explizit heißen.</span><span class="sxs-lookup"><span data-stu-id="62884-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="62884-120">Nicht gesendete Nachrichten führen Sie diese Eigenschaft, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) oder **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) in der Regel nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="62884-120">Unsent messages generally do not set this property, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span></span> <span data-ttu-id="62884-121">Wenn sie in der Benutzer kann in öffentliche Nachrichtenspeichern, in der anderen Benutzer privaten Speicher, in den Dateien auf dem Datenträger, zugreifen oder in anderen empfangenen Nachrichten eingebettet, sie in der Regel die Werte, die festgelegt wurden, enthalten Nachrichten vorhanden sind der letzten Ausführung ein Transportdienstes übermittelt die Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="62884-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="62884-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="62884-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62884-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="62884-123">Protocol specifications</span></span>

<span data-ttu-id="62884-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62884-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62884-125">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="62884-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="62884-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62884-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62884-127">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="62884-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62884-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="62884-128">Header files</span></span>

<span data-ttu-id="62884-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62884-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="62884-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="62884-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="62884-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="62884-131">Mapitags.h</span></span>
  
> <span data-ttu-id="62884-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="62884-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62884-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62884-133">See also</span></span>



[<span data-ttu-id="62884-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62884-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62884-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62884-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62884-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="62884-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62884-137">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="62884-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

