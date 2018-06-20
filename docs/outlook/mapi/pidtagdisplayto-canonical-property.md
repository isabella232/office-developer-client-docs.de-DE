---
title: Kanonische-Eigenschaft PidTagDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d83683fded6a650a947caa7119d138f6f4105e1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794329"
---
# <a name="pidtagdisplayto-canonical-property"></a><span data-ttu-id="c5f25-103">Kanonische-Eigenschaft PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="c5f25-103">PidTagDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="c5f25-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c5f25-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c5f25-105">Enthält eine Liste der den Anzeigenamen der primären (Empfänger der Nachricht, durch Semikolons (;) voneinander getrennt sind To).</span><span class="sxs-lookup"><span data-stu-id="c5f25-105">Contains a list of the display names of the primary (To) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5f25-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c5f25-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5f25-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="c5f25-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="c5f25-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="c5f25-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c5f25-109">0x0E04</span><span class="sxs-lookup"><span data-stu-id="c5f25-109">0x0E04</span></span>  <br/> |
|<span data-ttu-id="c5f25-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c5f25-110">Data type:</span></span>  <br/> |<span data-ttu-id="c5f25-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c5f25-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c5f25-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c5f25-112">Area:</span></span>  <br/> |<span data-ttu-id="c5f25-113">Nachricht</span><span class="sxs-lookup"><span data-stu-id="c5f25-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5f25-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c5f25-114">Remarks</span></span>

<span data-ttu-id="c5f25-115">Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte, die mit der [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c5f25-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="c5f25-116">Der Nachrichtenspeicher verwaltet auch diese Eigenschaften, sodass es immer den letzten gespeicherten Zustand einer Nachricht widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="c5f25-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="c5f25-117">Zeitpunkt der jeder Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode wird der Wert synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="c5f25-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="c5f25-118">Wenn eine Nachricht keine primären Empfänger enthält, sollte der Nachrichtenspeicher auf einen [IMAPIProp::GetProps](imapiprop-getprops.md) Anruf mit der Rückgabewert S_OK und eine leere Zeichenfolge für **PR_DISPLAY_TO**reagieren.</span><span class="sxs-lookup"><span data-stu-id="c5f25-118">If a message has no primary recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_TO**.</span></span> 
  
<span data-ttu-id="c5f25-119">Aufgrund der möglichen Notwendigkeit Lokalisierung bietet MAPI diese Richtlinien für alle Empfängernamen:</span><span class="sxs-lookup"><span data-stu-id="c5f25-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="c5f25-120">Alle Namen sollte lokalisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="c5f25-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="c5f25-121">Das Semikolon sollte das Zeichen, mit dem Namen in der **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und **PR_DISPLAY_TO** Eigenschaften zu trennen.</span><span class="sxs-lookup"><span data-stu-id="c5f25-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** properties.</span></span> <span data-ttu-id="c5f25-122">Semikolons dürfen nicht innerhalb von Empfängernamen in MAPI.</span><span class="sxs-lookup"><span data-stu-id="c5f25-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="c5f25-123">Clients sollte jedem Semikolon festgestellt übersetzen im **PR_DISPLAY_TO** und verwandten Eigenschaften eine lokalisierte Trennzeichen, bevor die Informationen in der Benutzeroberfläche sichtbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="c5f25-123">Clients should translate each semicolon encountered in the **PR_DISPLAY_TO** and related properties to a localized separator character before making the information visible in the user interface.</span></span> 
    
- <span data-ttu-id="c5f25-124">Beim Weiterleiten von Nachrichten müssen Clients nicht die Trennzeichen in der primären Empfänger Zeile übersetzen.</span><span class="sxs-lookup"><span data-stu-id="c5f25-124">When forwarding messages, clients do not need to translate the separator characters on the primary recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="c5f25-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c5f25-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c5f25-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c5f25-126">Protocol specifications</span></span>

<span data-ttu-id="c5f25-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5f25-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5f25-128">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c5f25-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c5f25-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c5f25-129">Header files</span></span>

<span data-ttu-id="c5f25-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5f25-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5f25-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c5f25-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="c5f25-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c5f25-132">Mapitags.h</span></span>
  
> <span data-ttu-id="c5f25-133">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c5f25-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5f25-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5f25-134">See also</span></span>



[<span data-ttu-id="c5f25-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5f25-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5f25-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5f25-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5f25-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c5f25-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5f25-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c5f25-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

