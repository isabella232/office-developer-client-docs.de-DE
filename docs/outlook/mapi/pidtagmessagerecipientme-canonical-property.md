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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e8ae52df1dd9775f706e2b1b2dc8b17b1f47a0bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794631"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a><span data-ttu-id="6dd90-103">PidTagMessageRecipientMe (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6dd90-103">PidTagMessageRecipientMe Canonical Property</span></span>

  
  
<span data-ttu-id="6dd90-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6dd90-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6dd90-105">Enthält True, wenn dieser Benutzer messaging speziell als primäre (To), Carbon Copy, Kopie (CC) oder blind Carbon Copy, Blindkopie (BCC) Empfänger dieser Nachricht heißt und nicht Bestandteil einer Verteilerliste ist.</span><span class="sxs-lookup"><span data-stu-id="6dd90-105">Contains TRUE if this messaging user is specifically named as a primary (To), carbon copy (CC), or blind carbon copy (BCC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6dd90-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6dd90-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6dd90-107">PR_MESSAGE_RECIP_ME</span><span class="sxs-lookup"><span data-stu-id="6dd90-107">PR_MESSAGE_RECIP_ME</span></span>  <br/> |
|<span data-ttu-id="6dd90-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="6dd90-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6dd90-109">0x0059</span><span class="sxs-lookup"><span data-stu-id="6dd90-109">0x0059</span></span>  <br/> |
|<span data-ttu-id="6dd90-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6dd90-110">Data type:</span></span>  <br/> |<span data-ttu-id="6dd90-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6dd90-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6dd90-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6dd90-112">Area:</span></span>  <br/> |<span data-ttu-id="6dd90-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="6dd90-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6dd90-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6dd90-114">Remarks</span></span>

<span data-ttu-id="6dd90-115">Diese Eigenschaft bietet eine bequeme Möglichkeit zum bestimmen, ob der Benutzername in der Empfängerliste explizit angezeigt wird, ohne alle Einträge in der Liste untersuchen.</span><span class="sxs-lookup"><span data-stu-id="6dd90-115">This property provides a convenient way to determine whether the user name appears explicitly in the recipient list, without examining all entries in the list.</span></span> <span data-ttu-id="6dd90-116">Der Wert des logischen Operators **OR** die Eigenschaften **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) und **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) sowie die BCC-Informationen darstellt (die andernfalls erscheint nicht in einer (Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="6dd90-116">The value represents the logical **OR** operation of the properties **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) and **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), and the BCC information (which does not otherwise appear in a property).</span></span> 
  
<span data-ttu-id="6dd90-117">Diese Eigenschaft unterstützt automatisierte Verarbeitung von erhaltenen Nachrichten zum Zeitpunkt des Eingangs.</span><span class="sxs-lookup"><span data-stu-id="6dd90-117">This property assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="6dd90-118">Unter der Adressbuchhierarchie verwenden wird, diese Eigenschaft enthält FALSE oder nicht einbezogen wird, wenn der messaging-Benutzer nicht direkt in der Empfänger Tabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="6dd90-118">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="6dd90-119">Übermittlung von Nachrichten, die durch die Erweiterung der Verteilerliste erstellt bewirkt keine diese Eigenschaft festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6dd90-119">Message delivery that results from distribution list expansion does not cause this property to be set.</span></span> <span data-ttu-id="6dd90-120">Der Empfänger muss explizit heißen.</span><span class="sxs-lookup"><span data-stu-id="6dd90-120">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="6dd90-121">Nicht gesendete Nachrichten im Allgemeinen legen diese Eigenschaft, **PR_MESSAGE_CC_ME**oder **PR_MESSAGE_TO_ME**Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="6dd90-121">Unsent messages generally do not set this property, **PR_MESSAGE_CC_ME**, or **PR_MESSAGE_TO_ME**.</span></span> <span data-ttu-id="6dd90-122">Wenn sie in der Benutzer kann in öffentliche Nachrichtenspeichern, in der anderen Benutzer privaten Speicher, in den Dateien auf dem Datenträger, zugreifen oder in anderen empfangenen Nachrichten eingebettet, sie in der Regel die Werte, die festgelegt wurden, enthalten Nachrichten vorhanden sind der letzten Ausführung ein Transportdienstes übermittelt die Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="6dd90-122">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6dd90-123">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6dd90-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6dd90-124">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6dd90-124">Protocol specifications</span></span>

<span data-ttu-id="6dd90-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6dd90-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6dd90-126">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6dd90-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6dd90-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6dd90-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6dd90-128">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6dd90-128">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6dd90-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6dd90-129">Header files</span></span>

<span data-ttu-id="6dd90-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6dd90-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="6dd90-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6dd90-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="6dd90-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6dd90-132">Mapitags.h</span></span>
  
> <span data-ttu-id="6dd90-133">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6dd90-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6dd90-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dd90-134">See also</span></span>



[<span data-ttu-id="6dd90-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6dd90-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6dd90-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6dd90-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6dd90-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6dd90-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6dd90-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6dd90-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

