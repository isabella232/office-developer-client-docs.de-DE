---
title: PidTagDisplayCc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2bf862317ca1d2f2a09a71e1af62b82661b33326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360809"
---
# <a name="pidtagdisplaycc-canonical-property"></a><span data-ttu-id="d6937-103">PidTagDisplayCc (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d6937-103">PidTagDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="d6937-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6937-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6937-105">Enthält eine ASCII-Liste der Anzeigenamen aller Cc -Nachrichtenempfänger (Carbon Copy, Carbon Copy), getrennt durch Semikolons (;).</span><span class="sxs-lookup"><span data-stu-id="d6937-105">Contains an ASCII list of the display names of any carbon copy (CC) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6937-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d6937-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6937-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="d6937-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="d6937-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d6937-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6937-109">0x0E03</span><span class="sxs-lookup"><span data-stu-id="d6937-109">0x0E03</span></span>  <br/> |
|<span data-ttu-id="d6937-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d6937-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6937-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d6937-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d6937-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d6937-112">Area:</span></span>  <br/> |<span data-ttu-id="d6937-113">Message</span><span class="sxs-lookup"><span data-stu-id="d6937-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6937-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6937-114">Remarks</span></span>

<span data-ttu-id="d6937-115">Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte mithilfe der [IMessage::ModifyRecipients-Methode.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="d6937-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="d6937-116">Der Nachrichtenspeicher behält diese Eigenschaften auch bei, sodass er immer den letzten gespeicherten Status einer Nachricht widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="d6937-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="d6937-117">Der Wert wird bei jedem Aufruf von [IMAPIProp::SaveChanges synchronisiert.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="d6937-117">The value is synchronized at the time of every call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> 
  
<span data-ttu-id="d6937-118">Wenn eine Nachricht keine E-Mail-Empfänger hat, sollte der Nachrichtenspeicher auf einen [IMAPIProp::GetProps-Aufruf](imapiprop-getprops.md) mit dem Rückgabewert S_OK und einer leeren Zeichenfolge für diese Eigenschaften reagieren.</span><span class="sxs-lookup"><span data-stu-id="d6937-118">If a message has no carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for these properties.</span></span> 
  
<span data-ttu-id="d6937-119">Aufgrund des möglichen Lokalisierungsbedarfs bietet MAPI die folgenden Richtlinien für alle Empfängernamen:</span><span class="sxs-lookup"><span data-stu-id="d6937-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="d6937-120">Alle Namen sollten lokalisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="d6937-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="d6937-121">Das Semikolon sollte das Zeichen sein, das zum Trennen von Namen in den Eigenschaften **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** und **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d6937-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**, and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="d6937-122">Semikolons sind innerhalb von Empfängernamen in MAPI nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d6937-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="d6937-123">Clients sollten jedes in dieser Eigenschaft gefundene Semikolon in ein lokalisiertes Trennzeichen übersetzen, bevor die Eigenschaftsinformationen auf der Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d6937-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="d6937-124">Beim Weiterleiten von Nachrichten müssen Clients die Trennzeichen in der Empfängerzeile der Carbon copy nicht übersetzen.</span><span class="sxs-lookup"><span data-stu-id="d6937-124">When forwarding messages, clients do not need to translate the separator characters on the carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="d6937-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d6937-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6937-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d6937-126">Protocol specifications</span></span>

<span data-ttu-id="d6937-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6937-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6937-128">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d6937-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6937-129">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d6937-129">Header files</span></span>

<span data-ttu-id="d6937-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6937-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6937-131">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d6937-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6937-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d6937-132">Mapitags.h</span></span>
  
> <span data-ttu-id="d6937-133">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d6937-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6937-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6937-134">See also</span></span>



[<span data-ttu-id="d6937-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d6937-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6937-136">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d6937-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6937-137">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d6937-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6937-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d6937-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

