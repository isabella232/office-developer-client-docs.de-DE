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
ms.openlocfilehash: 96bfc184752b6a3e15434ad67ac8c2b4b26cac4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426835"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="4d8e2-103">PidTagCorrelateMtsid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4d8e2-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="4d8e2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d8e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d8e2-105">Enthält die ID des Nachrichtenübertragungssystems (Message Transfer System, MTS), die bei der Korrelierung von Berichten mit gesendeten Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4d8e2-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d8e2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4d8e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d8e2-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="4d8e2-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="4d8e2-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4d8e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4d8e2-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="4d8e2-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="4d8e2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4d8e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="4d8e2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4d8e2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4d8e2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4d8e2-112">Area:</span></span>  <br/> |<span data-ttu-id="4d8e2-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="4d8e2-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d8e2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4d8e2-114">Remarks</span></span>

<span data-ttu-id="4d8e2-115">Wenn ein Transportanbieter eine übermittelte Nachricht mit dieser Eigenschaft auf TRUE trifft, wird diese Eigenschaft auf den MTS-Bezeichner für diese Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4d8e2-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="4d8e2-116">Nach der Übertragung wird diese Eigenschaft mit der Nachricht im Ordner "Interpersonal Message( IPM) Gesendete Elemente" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4d8e2-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="4d8e2-117">Messagingsysteme, die die Korrelation nach MTS-Id unterstützen, z. B. X.400, behalten den Bezeichner als Teil des Transportumschlags der ursprünglichen Nachricht sowie aller berichte bei, die als Reaktion darauf generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="4d8e2-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="4d8e2-118">Wenn ein Bericht von einem solchen Messagingsystem zugestellt wird, legt der Transportanbieter diese Eigenschaft auf den ursprünglichen MTS-Bezeichner aus dem Transportumschlag des Berichts fest.</span><span class="sxs-lookup"><span data-stu-id="4d8e2-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="4d8e2-119">Diese Eigenschaft wird dann mit dem Bericht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4d8e2-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="4d8e2-120">Eine Clientanwendung kann einen Suchergebnisordner aller Nachrichten mit dieser Eigenschaft verwalten.</span><span class="sxs-lookup"><span data-stu-id="4d8e2-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="4d8e2-121">Wenn ein Bericht für eine solche Nachricht einkommt, kann der Client Einschränkungen auf den Suchergebnisordner anwenden, die ursprüngliche Version der Nachricht suchen und die ursprünglichen Nachrichteninformationen mit den neuen Informationen korrelieren.</span><span class="sxs-lookup"><span data-stu-id="4d8e2-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4d8e2-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4d8e2-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4d8e2-123">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="4d8e2-123">Header files</span></span>

<span data-ttu-id="4d8e2-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d8e2-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d8e2-125">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4d8e2-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4d8e2-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4d8e2-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4d8e2-127">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4d8e2-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d8e2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d8e2-128">See also</span></span>



[<span data-ttu-id="4d8e2-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d8e2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d8e2-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="4d8e2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d8e2-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4d8e2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d8e2-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4d8e2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

