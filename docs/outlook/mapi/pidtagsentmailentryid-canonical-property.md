---
title: PidTagSentMailEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentMailEntryId
api_type:
- COM
ms.assetid: 8f14dc15-d7d7-4894-b6a8-0d589f576c42
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e7aef8e9ba605d47b110a496e46f629df60a28ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342511"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="43209-103">PidTagSentMailEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="43209-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="43209-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43209-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43209-105">Enthält die Eintrags-ID des Ordners, in den die Nachricht nach der Übermittlung verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="43209-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43209-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="43209-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43209-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="43209-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="43209-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="43209-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43209-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="43209-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="43209-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="43209-110">Data type:</span></span>  <br/> |<span data-ttu-id="43209-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="43209-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="43209-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="43209-112">Area:</span></span>  <br/> |<span data-ttu-id="43209-113">MAPI nicht durchlässig</span><span class="sxs-lookup"><span data-stu-id="43209-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43209-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="43209-114">Remarks</span></span>

<span data-ttu-id="43209-115">Diese Eigenschaft wird häufig aus der **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) -Eigenschaft kopiert, dem Standardordner "Gesendete Elemente" der Clientanwendung.</span><span class="sxs-lookup"><span data-stu-id="43209-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="43209-116">Die Clientanwendung verwendet diese Eigenschaft mit der **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit )-Eigenschaft,](pidtagdeleteaftersubmit-canonical-property.md)um zu steuern, was mit einer Nachricht nach dem Übermitteln geschieht.</span><span class="sxs-lookup"><span data-stu-id="43209-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="43209-117">Entweder die eine oder die andere sollte festgelegt werden, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="43209-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="43209-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="43209-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43209-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="43209-119">Protocol specifications</span></span>

<span data-ttu-id="43209-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43209-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43209-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="43209-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="43209-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43209-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43209-123">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="43209-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="43209-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43209-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43209-125">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="43209-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43209-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="43209-126">Header files</span></span>

<span data-ttu-id="43209-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43209-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="43209-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="43209-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="43209-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="43209-129">Mapitags.h</span></span>
  
> <span data-ttu-id="43209-130">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="43209-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43209-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43209-131">See also</span></span>



[<span data-ttu-id="43209-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43209-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43209-133">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="43209-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43209-134">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="43209-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43209-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="43209-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

