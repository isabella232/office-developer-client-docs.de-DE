---
title: PidTagDisplayTo (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0c7ae8951b02f099161871b17ff59ea23f8fbcc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360788"
---
# <a name="pidtagdisplayto-canonical-property"></a><span data-ttu-id="e94e2-103">PidTagDisplayTo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e94e2-103">PidTagDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="e94e2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e94e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e94e2-105">Enthält eine Liste der Anzeigenamen der primären (An)-Nachrichtenempfänger, getrennt durch Semikolons (;).</span><span class="sxs-lookup"><span data-stu-id="e94e2-105">Contains a list of the display names of the primary (To) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e94e2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e94e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e94e2-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="e94e2-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="e94e2-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e94e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e94e2-109">0x0E04</span><span class="sxs-lookup"><span data-stu-id="e94e2-109">0x0E04</span></span>  <br/> |
|<span data-ttu-id="e94e2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e94e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="e94e2-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e94e2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e94e2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e94e2-112">Area:</span></span>  <br/> |<span data-ttu-id="e94e2-113">Message</span><span class="sxs-lookup"><span data-stu-id="e94e2-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e94e2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e94e2-114">Remarks</span></span>

<span data-ttu-id="e94e2-115">Der Nachrichtenspeicher berechnet diese Eigenschaften für Nachrichtenobjekte mithilfe der [IMessage::ModifyRecipients-Methode.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="e94e2-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="e94e2-116">Der Nachrichtenspeicher behält diese Eigenschaften auch bei, sodass er immer den letzten gespeicherten Status einer Nachricht widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="e94e2-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="e94e2-117">Der Wert wird bei jedem Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="e94e2-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="e94e2-118">Wenn eine Nachricht keine primären Empfänger hat, sollte der Nachrichtenspeicher auf einen [IMAPIProp::GetProps-Aufruf](imapiprop-getprops.md) mit dem Rückgabewert S_OK und einer leeren Zeichenfolge für PR_DISPLAY_TO **.**</span><span class="sxs-lookup"><span data-stu-id="e94e2-118">If a message has no primary recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_TO**.</span></span> 
  
<span data-ttu-id="e94e2-119">Aufgrund des möglichen Lokalisierungsbedarfs bietet MAPI die folgenden Richtlinien für alle Empfängernamen:</span><span class="sxs-lookup"><span data-stu-id="e94e2-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="e94e2-120">Alle Namen sollten lokalisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="e94e2-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="e94e2-121">Das Semikolon sollte das Zeichen sein, das zum Trennen von Namen in den Eigenschaften **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) und **PR_DISPLAY_TO** wird.</span><span class="sxs-lookup"><span data-stu-id="e94e2-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** properties.</span></span> <span data-ttu-id="e94e2-122">Semikolons sind innerhalb von Empfängernamen in MAPI nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="e94e2-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="e94e2-123">Clients sollten jedes Semikolon,  das in der PR_DISPLAY_TO und zugehörigen Eigenschaften auftritt, in ein lokalisiertes Trennzeichen übersetzen, bevor die Informationen auf der Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e94e2-123">Clients should translate each semicolon encountered in the **PR_DISPLAY_TO** and related properties to a localized separator character before making the information visible in the user interface.</span></span> 
    
- <span data-ttu-id="e94e2-124">Beim Weiterleiten von Nachrichten müssen Clients die Trennzeichen in der primären Empfängerzeile nicht übersetzen.</span><span class="sxs-lookup"><span data-stu-id="e94e2-124">When forwarding messages, clients do not need to translate the separator characters on the primary recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="e94e2-125">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e94e2-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e94e2-126">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e94e2-126">Protocol specifications</span></span>

<span data-ttu-id="e94e2-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e94e2-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e94e2-128">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e94e2-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e94e2-129">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="e94e2-129">Header files</span></span>

<span data-ttu-id="e94e2-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e94e2-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="e94e2-131">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e94e2-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="e94e2-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e94e2-132">Mapitags.h</span></span>
  
> <span data-ttu-id="e94e2-133">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e94e2-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e94e2-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e94e2-134">See also</span></span>



[<span data-ttu-id="e94e2-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e94e2-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e94e2-136">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="e94e2-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e94e2-137">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e94e2-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e94e2-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e94e2-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

