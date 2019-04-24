---
title: Kanonische Pidtagstatusstring (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9b4510a32fe14e4316a6bcddafcc163ee899436e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278893"
---
# <a name="pidtagstatusstring-canonical-property"></a><span data-ttu-id="2a69d-103">Kanonische Pidtagstatusstring (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2a69d-103">PidTagStatusString Canonical Property</span></span>

  
  
<span data-ttu-id="2a69d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a69d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a69d-105">Enthält eine Meldung, die den aktuellen Status einer Sitzungs Ressource angibt.</span><span class="sxs-lookup"><span data-stu-id="2a69d-105">Contains a message that indicates the current status of a session resource.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a69d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2a69d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a69d-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span><span class="sxs-lookup"><span data-stu-id="2a69d-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span></span>  <br/> |
|<span data-ttu-id="2a69d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2a69d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2a69d-109">0x3E08</span><span class="sxs-lookup"><span data-stu-id="2a69d-109">0x3E08</span></span>  <br/> |
|<span data-ttu-id="2a69d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2a69d-110">Data type:</span></span>  <br/> |<span data-ttu-id="2a69d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2a69d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2a69d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2a69d-112">Area:</span></span>  <br/> |<span data-ttu-id="2a69d-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="2a69d-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a69d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a69d-114">Remarks</span></span>

<span data-ttu-id="2a69d-115">Diese Eigenschaften bieten Dienstanbietern und MAPI die Möglichkeit, bestimmte Informationen zum Status einer Sitzungs Ressource anzugeben, beispielsweise das integrierte Adressbuch oder einen bestimmten Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="2a69d-115">These properties give service providers and MAPI the opportunity to supply specific information about the status of a session resource, such as the integrated address book or a particular service provider.</span></span> <span data-ttu-id="2a69d-116">Diese Eigenschaft erläutert und bietet zusätzliche Informationen zu einem Statuscode oder der **PR_STATUS_CODE** ([pidtagstatuscode (](pidtagstatuscode-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2a69d-116">This property explains and provides additional information about a status code, or the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property.</span></span> <span data-ttu-id="2a69d-117">Während **PR_STATUS_CODE** für alle Status-Objekte erforderlich ist, sind **PR_STATUS_STRING** und zugehörige Eigenschaften optional.</span><span class="sxs-lookup"><span data-stu-id="2a69d-117">Whereas **PR_STATUS_CODE** is required for all status objects, **PR_STATUS_STRING** and associated properties are optional.</span></span> <span data-ttu-id="2a69d-118">Wenn der Transportanbieter keinen Wert angibt, stellt der MAPI-Spooler einen Standardwert bereit.</span><span class="sxs-lookup"><span data-stu-id="2a69d-118">When the transport provider does not supply a value, the MAPI spooler supplies a default value.</span></span> 
  
<span data-ttu-id="2a69d-119">Die Zeichenfolge wird auf derselben Seite des Remoteprozeduraufrufs als MAPI-Spooler generiert; Sie durchläuft Shared Memory, statt über eine Prozessgrenze hinweg gemarshallt zu werden.</span><span class="sxs-lookup"><span data-stu-id="2a69d-119">The string is generated on the same side of the remote procedure call as the MAPI spooler; it travels through shared memory rather than being marshaled across a process boundary.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2a69d-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2a69d-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2a69d-121">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="2a69d-121">Header files</span></span>

<span data-ttu-id="2a69d-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2a69d-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a69d-123">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="2a69d-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="2a69d-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2a69d-124">Mapitags.h</span></span>
  
> <span data-ttu-id="2a69d-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2a69d-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a69d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a69d-126">See also</span></span>



[<span data-ttu-id="2a69d-127">Kanonische Pidtagstatuscode (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2a69d-127">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)


[<span data-ttu-id="2a69d-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a69d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a69d-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a69d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a69d-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2a69d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a69d-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2a69d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

