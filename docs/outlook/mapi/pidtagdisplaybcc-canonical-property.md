---
title: Kanonische PidTagDisplayBcc-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayBcc
api_type:
- HeaderDef
ms.assetid: ab5bcd67-d54e-46e9-b94e-a652aac3e81c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 55ee55fefd82f29c8b780a350ecdfe0285b3d649
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794318"
---
# <a name="pidtagdisplaybcc-canonical-property"></a><span data-ttu-id="39ba0-103">Kanonische PidTagDisplayBcc-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="39ba0-103">PidTagDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="39ba0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39ba0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39ba0-105">Enthält eine Liste ASCII, der den Anzeigenamen der alle blind Carbon Copy, Blindkopie (BCC) Empfänger der Nachricht, durch Semikolons (;) voneinander getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="39ba0-105">Contains an ASCII list of the display names of any blind carbon copy (BCC) message recipients, separated by semicolons (;).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="39ba0-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="39ba0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="39ba0-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="39ba0-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="39ba0-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="39ba0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="39ba0-109">0x0E02</span><span class="sxs-lookup"><span data-stu-id="39ba0-109">0x0E02</span></span>  <br/> |
|<span data-ttu-id="39ba0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="39ba0-110">Data type:</span></span>  <br/> |<span data-ttu-id="39ba0-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="39ba0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="39ba0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="39ba0-112">Area:</span></span>  <br/> |<span data-ttu-id="39ba0-113">Nachricht</span><span class="sxs-lookup"><span data-stu-id="39ba0-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39ba0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39ba0-114">Remarks</span></span>

<span data-ttu-id="39ba0-115">Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte, die mit der [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="39ba0-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="39ba0-116">Der Nachrichtenspeicher verwaltet auch diese Eigenschaften, sodass es immer den letzten gespeicherten Zustand einer Nachricht widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="39ba0-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="39ba0-117">Zeitpunkt der jeder Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode wird der Wert synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="39ba0-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="39ba0-118">Wenn eine Nachricht keine Bcc-Empfänger enthält, sollte einen [IMAPIProp::GetProps](imapiprop-getprops.md) Anruf mit der Rückgabewert S_OK und eine leere Zeichenfolge für **PR_DISPLAY_BCC**des Nachrichtenspeichers beantworten.</span><span class="sxs-lookup"><span data-stu-id="39ba0-118">If a message has no blind carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_BCC**.</span></span> 
  
<span data-ttu-id="39ba0-119">Aufgrund der möglichen Notwendigkeit Lokalisierung bietet MAPI diese Richtlinien für alle Empfängernamen:</span><span class="sxs-lookup"><span data-stu-id="39ba0-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="39ba0-120">Alle Namen sollte lokalisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="39ba0-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="39ba0-121">Das Semikolon sollte das Zeichen, mit dem Namen in der **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und Eigenschaften **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) zu trennen.</span><span class="sxs-lookup"><span data-stu-id="39ba0-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="39ba0-122">Semikolons dürfen nicht innerhalb von Empfängernamen in MAPI.</span><span class="sxs-lookup"><span data-stu-id="39ba0-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="39ba0-123">Clients sollte jedem Semikolon in dieser Eigenschaft auf eine lokalisierte Trennzeichen aufgetreten ist, bevor Informationen über die Eigenschaft in der Benutzeroberfläche sichtbar gemacht übersetzen.</span><span class="sxs-lookup"><span data-stu-id="39ba0-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="39ba0-124">Beim Weiterleiten von Nachrichten müssen Clients nicht die Trennzeichen in der Empfänger Bcc-Zeile übersetzen.</span><span class="sxs-lookup"><span data-stu-id="39ba0-124">When forwarding messages, clients do not need to translate the separator characters on the blind carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="39ba0-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="39ba0-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="39ba0-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="39ba0-126">Protocol specifications</span></span>

<span data-ttu-id="39ba0-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39ba0-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39ba0-128">Beschreibt das Format von Nachrichten, die zum Senden von Informationen im Zusammenhang mit der Freigabe von Ordnern auf dem Client verwendet.</span><span class="sxs-lookup"><span data-stu-id="39ba0-128">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="39ba0-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="39ba0-129">Header files</span></span>

<span data-ttu-id="39ba0-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="39ba0-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="39ba0-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="39ba0-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="39ba0-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="39ba0-132">Mapitags.h</span></span>
  
> <span data-ttu-id="39ba0-133">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="39ba0-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39ba0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39ba0-134">See also</span></span>



[<span data-ttu-id="39ba0-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39ba0-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="39ba0-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39ba0-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="39ba0-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="39ba0-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="39ba0-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="39ba0-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

