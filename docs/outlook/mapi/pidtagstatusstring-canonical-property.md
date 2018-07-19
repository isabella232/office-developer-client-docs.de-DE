---
title: PidTagStatusString (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ea24b5e721317668c8f43278a5e4c38d73b3e91c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795200"
---
# <a name="pidtagstatusstring-canonical-property"></a><span data-ttu-id="53774-103">PidTagStatusString (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="53774-103">PidTagStatusString Canonical Property</span></span>

  
  
<span data-ttu-id="53774-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53774-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="53774-105">Enthält eine Meldung, die den aktuellen Status einer Sitzung Ressource angibt.</span><span class="sxs-lookup"><span data-stu-id="53774-105">Contains a message that indicates the current status of a session resource.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53774-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="53774-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53774-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span><span class="sxs-lookup"><span data-stu-id="53774-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span></span>  <br/> |
|<span data-ttu-id="53774-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="53774-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53774-109">0x3E08</span><span class="sxs-lookup"><span data-stu-id="53774-109">0x3E08</span></span>  <br/> |
|<span data-ttu-id="53774-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="53774-110">Data type:</span></span>  <br/> |<span data-ttu-id="53774-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="53774-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="53774-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="53774-112">Area:</span></span>  <br/> |<span data-ttu-id="53774-113">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="53774-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53774-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53774-114">Remarks</span></span>

<span data-ttu-id="53774-115">Diese Eigenschaften geben Dienstanbieter und MAPI-die Möglichkeit, bestimmte Informationen über den Status einer Sitzung Ressource, wie die integrierte Adressbuch oder einem bestimmten Dienstanbieter anzugeben.</span><span class="sxs-lookup"><span data-stu-id="53774-115">These properties give service providers and MAPI the opportunity to supply specific information about the status of a session resource, such as the integrated address book or a particular service provider.</span></span> <span data-ttu-id="53774-116">Diese Eigenschaft erläutert und liefert zusätzliche Informationen über einen Statuscode oder die Eigenschaft **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="53774-116">This property explains and provides additional information about a status code, or the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property.</span></span> <span data-ttu-id="53774-117">**PR_STATUS_CODE** für alle Status erforderlich ist, sind die **PR_STATUS_STRING** und die zugehörigen Eigenschaften optional.</span><span class="sxs-lookup"><span data-stu-id="53774-117">Whereas **PR_STATUS_CODE** is required for all status objects, **PR_STATUS_STRING** and associated properties are optional.</span></span> <span data-ttu-id="53774-118">Wenn der Adressbuchhierarchie kein Wert angegeben, stellt die MAPI-Warteschlange einen Standardwert bereit.</span><span class="sxs-lookup"><span data-stu-id="53774-118">When the transport provider does not supply a value, the MAPI spooler supplies a default value.</span></span> 
  
<span data-ttu-id="53774-119">Die Zeichenfolge wird auf derselben Seite die remote Procedure call, als die MAPI-Warteschlange generiert. Übertragung über gemeinsam genutzten Speicher, statt über eine Prozessgrenze gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="53774-119">The string is generated on the same side of the remote procedure call as the MAPI spooler; it travels through shared memory rather than being marshaled across a process boundary.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="53774-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="53774-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="53774-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="53774-121">Header files</span></span>

<span data-ttu-id="53774-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53774-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="53774-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="53774-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="53774-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="53774-124">Mapitags.h</span></span>
  
> <span data-ttu-id="53774-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="53774-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53774-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53774-126">See also</span></span>



[<span data-ttu-id="53774-127">PidTagStatusCode (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="53774-127">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)


[<span data-ttu-id="53774-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53774-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53774-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53774-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53774-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="53774-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53774-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="53774-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

