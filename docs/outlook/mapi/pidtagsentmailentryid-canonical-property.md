---
title: Kanonische Pidtagsentmailentryid (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e7aef8e9ba605d47b110a496e46f629df60a28ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342511"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="bea69-103">Kanonische Pidtagsentmailentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bea69-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="bea69-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bea69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bea69-105">Enthält die Eintrags-ID des Ordners, in den die Nachricht nach der Übermittlung verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="bea69-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bea69-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bea69-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bea69-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bea69-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="bea69-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bea69-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bea69-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="bea69-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="bea69-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bea69-110">Data type:</span></span>  <br/> |<span data-ttu-id="bea69-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bea69-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bea69-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bea69-112">Area:</span></span>  <br/> |<span data-ttu-id="bea69-113">Nicht transmitable MAPI</span><span class="sxs-lookup"><span data-stu-id="bea69-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bea69-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bea69-114">Remarks</span></span>

<span data-ttu-id="bea69-115">Diese Eigenschaft wird häufig aus der **PR_IPM_SENTMAIL_ENTRYID** ([pidtagipmsentmailentryid (](pidtagipmsentmailentryid-canonical-property.md))-Eigenschaft, dem standardOrdner "Gesendete Elemente" der Clientanwendung, kopiert.</span><span class="sxs-lookup"><span data-stu-id="bea69-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="bea69-116">Die Clientanwendung verwendet diese Eigenschaft mit der **PR_DELETE_AFTER_SUBMIT** ([pidtagdeleteaftersubmit (](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft, um zu steuern, was mit einer Nachricht geschieht, nachdem Sie übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="bea69-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="bea69-117">Entweder die eine oder die andere sollte festgelegt werden, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="bea69-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bea69-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bea69-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bea69-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bea69-119">Protocol specifications</span></span>

<span data-ttu-id="bea69-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bea69-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bea69-121">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bea69-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bea69-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bea69-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bea69-123">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bea69-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="bea69-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bea69-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bea69-125">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="bea69-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bea69-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="bea69-126">Header files</span></span>

<span data-ttu-id="bea69-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bea69-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="bea69-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="bea69-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="bea69-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bea69-129">Mapitags.h</span></span>
  
> <span data-ttu-id="bea69-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bea69-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bea69-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bea69-131">See also</span></span>



[<span data-ttu-id="bea69-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bea69-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bea69-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bea69-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bea69-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bea69-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bea69-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bea69-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

