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
ms.openlocfilehash: 9b4510a32fe14e4316a6bcddafcc163ee899436e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421564"
---
# <a name="pidtagstatusstring-canonical-property"></a><span data-ttu-id="89184-103">PidTagStatusString (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="89184-103">PidTagStatusString Canonical Property</span></span>

  
  
<span data-ttu-id="89184-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89184-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89184-105">Enthält eine Meldung, die den aktuellen Status einer Sitzungsressource angibt.</span><span class="sxs-lookup"><span data-stu-id="89184-105">Contains a message that indicates the current status of a session resource.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89184-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="89184-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="89184-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span><span class="sxs-lookup"><span data-stu-id="89184-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span></span>  <br/> |
|<span data-ttu-id="89184-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="89184-108">Identifier:</span></span>  <br/> |<span data-ttu-id="89184-109">0x3E08</span><span class="sxs-lookup"><span data-stu-id="89184-109">0x3E08</span></span>  <br/> |
|<span data-ttu-id="89184-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="89184-110">Data type:</span></span>  <br/> |<span data-ttu-id="89184-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="89184-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="89184-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="89184-112">Area:</span></span>  <br/> |<span data-ttu-id="89184-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="89184-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89184-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="89184-114">Remarks</span></span>

<span data-ttu-id="89184-115">Diese Eigenschaften bieten Dienstanbietern und MAPI die Möglichkeit, spezifische Informationen über den Status einer Sitzungsressource, z. B. das integrierte Adressbuch oder einen bestimmten Dienstanbieter, zur Verfügung zu haben.</span><span class="sxs-lookup"><span data-stu-id="89184-115">These properties give service providers and MAPI the opportunity to supply specific information about the status of a session resource, such as the integrated address book or a particular service provider.</span></span> <span data-ttu-id="89184-116">Diese Eigenschaft erläutert und stellt zusätzliche Informationen zu einem Statuscode oder der **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) -Eigenschaft zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="89184-116">This property explains and provides additional information about a status code, or the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property.</span></span> <span data-ttu-id="89184-117">Während **PR_STATUS_CODE** für alle Statusobjekte erforderlich ist, **sind PR_STATUS_STRING** und zugeordnete Eigenschaften optional.</span><span class="sxs-lookup"><span data-stu-id="89184-117">Whereas **PR_STATUS_CODE** is required for all status objects, **PR_STATUS_STRING** and associated properties are optional.</span></span> <span data-ttu-id="89184-118">Wenn der Transportanbieter keinen Wert liefert, gibt der MAPI-Spooler einen Standardwert an.</span><span class="sxs-lookup"><span data-stu-id="89184-118">When the transport provider does not supply a value, the MAPI spooler supplies a default value.</span></span> 
  
<span data-ttu-id="89184-119">Die Zeichenfolge wird auf derselben Seite des Remoteprozeduraufrufs wie der #A0 generiert. Es wird durch freigegebenen Speicher anstatt über eine Prozessgrenze ge marshallt.</span><span class="sxs-lookup"><span data-stu-id="89184-119">The string is generated on the same side of the remote procedure call as the MAPI spooler; it travels through shared memory rather than being marshaled across a process boundary.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="89184-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="89184-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="89184-121">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="89184-121">Header files</span></span>

<span data-ttu-id="89184-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89184-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="89184-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="89184-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="89184-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="89184-124">Mapitags.h</span></span>
  
> <span data-ttu-id="89184-125">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="89184-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89184-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89184-126">See also</span></span>



[<span data-ttu-id="89184-127">PidTagStatusCode (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="89184-127">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)


[<span data-ttu-id="89184-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89184-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89184-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="89184-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89184-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="89184-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89184-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="89184-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

