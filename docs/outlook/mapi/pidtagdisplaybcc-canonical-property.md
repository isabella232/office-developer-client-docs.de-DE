---
title: Kanonische Pidtagdisplaybcc (-Eigenschaft
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
ms.openlocfilehash: 74669d102462e1a825568615d1d30346e99e90a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360816"
---
# <a name="pidtagdisplaybcc-canonical-property"></a><span data-ttu-id="d8b1e-103">Kanonische Pidtagdisplaybcc (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d8b1e-103">PidTagDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="d8b1e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8b1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8b1e-105">Enthält eine ASCII-Liste mit den Anzeigenamen aller BCC-Empfänger (Blind Carbon Copy), die durch Semikolons getrennt sind (;).</span><span class="sxs-lookup"><span data-stu-id="d8b1e-105">Contains an ASCII list of the display names of any blind carbon copy (BCC) message recipients, separated by semicolons (;).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8b1e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d8b1e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d8b1e-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="d8b1e-107">PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="d8b1e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d8b1e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d8b1e-109">0x0E02</span><span class="sxs-lookup"><span data-stu-id="d8b1e-109">0x0E02</span></span>  <br/> |
|<span data-ttu-id="d8b1e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d8b1e-110">Data type:</span></span>  <br/> |<span data-ttu-id="d8b1e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d8b1e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d8b1e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d8b1e-112">Area:</span></span>  <br/> |<span data-ttu-id="d8b1e-113">Nachricht</span><span class="sxs-lookup"><span data-stu-id="d8b1e-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8b1e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8b1e-114">Remarks</span></span>

<span data-ttu-id="d8b1e-115">Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte mithilfe der [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d8b1e-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="d8b1e-116">Der Nachrichtenspeicher verwaltet diese Eigenschaften auch so, dass er immer den zuletzt gespeicherten Status einer Nachricht widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="d8b1e-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="d8b1e-117">Der Wert wird bei jedem Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="d8b1e-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="d8b1e-118">Wenn eine Nachricht keine blinden Kopie-Empfänger hat, sollte der Nachrichtenspeicher auf einen [IMAPIProp::](imapiprop-getprops.md) GetProps-Aufruf mit einem Rückgabewert von S_OK und einer leeren Zeichenfolge für **PR_DISPLAY_BCC**reagieren.</span><span class="sxs-lookup"><span data-stu-id="d8b1e-118">If a message has no blind carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_BCC**.</span></span> 
  
<span data-ttu-id="d8b1e-119">Aufgrund der möglichen Lokalisierungsanforderungen bietet MAPI folgende Richtlinien für alle Empfängernamen:</span><span class="sxs-lookup"><span data-stu-id="d8b1e-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="d8b1e-120">Alle Namen sollten lokalisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="d8b1e-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="d8b1e-121">Das Semikolon sollte das Zeichen sein, das zum Trennen von Namen in den Eigenschaften **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8b1e-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="d8b1e-122">Innerhalb von Empfängernamen in MAPI sind keine Semikolons zulässig.</span><span class="sxs-lookup"><span data-stu-id="d8b1e-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="d8b1e-123">Clients sollten jedes Semikolon, das in dieser Eigenschaft vorliegt, in ein lokalisiertes Trennzeichen übersetzen, bevor die Eigenschaftsinformationen auf der Benutzeroberfläche sichtbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="d8b1e-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="d8b1e-124">Beim Weiterleiten von Nachrichten müssen die Trennzeichen in der Empfänger Linie für die Blindkopie nicht übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="d8b1e-124">When forwarding messages, clients do not need to translate the separator characters on the blind carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="d8b1e-125">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d8b1e-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d8b1e-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d8b1e-126">Protocol specifications</span></span>

<span data-ttu-id="d8b1e-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8b1e-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8b1e-128">Beschreibt das Format der Nachrichten, die zum Senden von Informationen im Zusammenhang mit Freigabeordnern auf dem Client verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8b1e-128">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d8b1e-129">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="d8b1e-129">Header files</span></span>

<span data-ttu-id="d8b1e-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d8b1e-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="d8b1e-131">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="d8b1e-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="d8b1e-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d8b1e-132">Mapitags.h</span></span>
  
> <span data-ttu-id="d8b1e-133">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d8b1e-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8b1e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8b1e-134">See also</span></span>



[<span data-ttu-id="d8b1e-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8b1e-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d8b1e-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8b1e-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d8b1e-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d8b1e-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d8b1e-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d8b1e-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

