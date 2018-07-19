---
title: PidLidAutoProcessState (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 86ef98ac7b4084de3a96210298fe0d5509d12103
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793445"
---
# <a name="pidlidautoprocessstate-canonical-property"></a><span data-ttu-id="af887-103">PidLidAutoProcessState (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="af887-103">PidLidAutoProcessState Canonical Property</span></span>

  
  
<span data-ttu-id="af887-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="af887-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="af887-105">Gibt die Optionen an, mit denen auf die automatische Verarbeitung von e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="af887-105">Specifies the options that are used in automatic processing of email messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af887-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="af887-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af887-107">dispidSniffState</span><span class="sxs-lookup"><span data-stu-id="af887-107">dispidSniffState</span></span>  <br/> |
|<span data-ttu-id="af887-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="af887-108">Property set:</span></span>  <br/> |<span data-ttu-id="af887-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="af887-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="af887-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="af887-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="af887-111">0x0000851A</span><span class="sxs-lookup"><span data-stu-id="af887-111">0x0000851A</span></span>  <br/> |
|<span data-ttu-id="af887-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="af887-112">Data type:</span></span>  <br/> |<span data-ttu-id="af887-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="af887-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="af887-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="af887-114">Area:</span></span>  <br/> |<span data-ttu-id="af887-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="af887-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af887-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af887-116">Remarks</span></span>

<span data-ttu-id="af887-117">Die Eigenschaft nicht vorhanden ist, möglicherweise in diesem Fall ist der Standardwert der "0 x 00000000" verwendet.</span><span class="sxs-lookup"><span data-stu-id="af887-117">The property may be absent, in which case the default value of "0x00000000" is used.</span></span> <span data-ttu-id="af887-118">Wenn Sie festlegen möchten, muss diese Eigenschaft auf einen der Werte in der folgenden Tabelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="af887-118">If set, this property must be set to one of the values in the following table.</span></span>
  
|<span data-ttu-id="af887-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="af887-119">**Value**</span></span>|<span data-ttu-id="af887-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af887-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af887-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af887-121">0x00000000</span></span>  <br/> |<span data-ttu-id="af887-122">Verarbeiten Sie die Nachricht nicht automatisch.</span><span class="sxs-lookup"><span data-stu-id="af887-122">Do not automatically process the message.</span></span>  <br/> |
|<span data-ttu-id="af887-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="af887-123">0x00000001</span></span>  <br/> |<span data-ttu-id="af887-124">Die Nachricht automatisch verarbeiten, oder wenn die Nachricht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="af887-124">Process the message automatically or when the message is opened.</span></span>  <br/> |
|<span data-ttu-id="af887-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="af887-125">0x00000002</span></span>  <br/> |<span data-ttu-id="af887-126">Verarbeitet die Nachricht nur, wenn die Nachricht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="af887-126">Process the message only when the message is opened.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="af887-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="af887-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af887-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="af887-128">Protocol specifications</span></span>

<span data-ttu-id="af887-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af887-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af887-130">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="af887-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af887-131">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af887-131">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af887-132">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="af887-132">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af887-133">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="af887-133">Header files</span></span>

<span data-ttu-id="af887-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af887-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="af887-135">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="af887-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af887-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af887-136">See also</span></span>



[<span data-ttu-id="af887-137">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="af887-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af887-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="af887-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af887-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="af887-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af887-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="af887-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

