---
title: PidTagCorrelateMtsid (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 57da2d4c78914323b5dafa4f5ba5b7628d0e2f2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794276"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="bcb2b-103">PidTagCorrelateMtsid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bcb2b-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="bcb2b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bcb2b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bcb2b-105">Enthält die Nachricht Transfer System (MTS)-ID in Korrelation Berichte mit gesendete Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bcb2b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bcb2b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bcb2b-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="bcb2b-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="bcb2b-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="bcb2b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bcb2b-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="bcb2b-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="bcb2b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bcb2b-110">Data type:</span></span>  <br/> |<span data-ttu-id="bcb2b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bcb2b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bcb2b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bcb2b-112">Area:</span></span>  <br/> |<span data-ttu-id="bcb2b-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="bcb2b-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcb2b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcb2b-114">Remarks</span></span>

<span data-ttu-id="bcb2b-115">Wenn ein Transportdienstes eine gesendete Nachricht mit dieser Eigenschaft auf true fest, erkennt, wird diese Eigenschaft die MTS-ID für diese Nachricht.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="bcb2b-116">Nach der Übermittlung wird diese Eigenschaft mit der Nachricht im Ordner Gesendete Elemente zwischen Personen Nachricht (IPM) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="bcb2b-117">Behalten Sie den Bezeichner als Teil des Umschlags Transport die ursprüngliche Nachricht wird und Berichte, die als Reaktion auf es generiert Messaging-Systeme, die Korrelations-ID MTS unterstützen, beispielsweise x. 400.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="bcb2b-118">Wenn ein Bericht aus einem solchen messaging System übermittelt werden, wird der Adressbuchhierarchie diese Eigenschaft auf den ursprünglichen MTS Bezeichner aus den Bericht Transport Umschlag an.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="bcb2b-119">Diese Eigenschaft wird mit dem Bericht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="bcb2b-120">Eine Clientanwendung kann alle Nachrichten, die mit dieser Eigenschaft einen Suchergebnisse Ordner verwalten.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="bcb2b-121">Wenn ein Bericht für diese Meldung eingeht, kann der Client gelten Beschränkungen in den Suchergebnissen Ordner, suchen Sie nach der ursprünglichen Version der Nachricht und korrelieren die ursprünglichen Nachrichteninformationen mit den neuen Informationen.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bcb2b-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bcb2b-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bcb2b-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bcb2b-123">Header files</span></span>

<span data-ttu-id="bcb2b-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bcb2b-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="bcb2b-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="bcb2b-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bcb2b-126">Mapitags.h</span></span>
  
> <span data-ttu-id="bcb2b-127">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcb2b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcb2b-128">See also</span></span>



[<span data-ttu-id="bcb2b-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bcb2b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bcb2b-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bcb2b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bcb2b-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bcb2b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bcb2b-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bcb2b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

