---
title: Kanonische Pidtagcorrelatemtsid (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 96bfc184752b6a3e15434ad67ac8c2b4b26cac4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359934"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="a4c7f-103">Kanonische Pidtagcorrelatemtsid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4c7f-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="a4c7f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4c7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4c7f-105">Enthält den MTS-Bezeichner (Message Transfer System), der bei der Korrelation von Berichten mit gesendeten Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a4c7f-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a4c7f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a4c7f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a4c7f-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="a4c7f-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="a4c7f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a4c7f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a4c7f-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="a4c7f-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="a4c7f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a4c7f-110">Data type:</span></span>  <br/> |<span data-ttu-id="a4c7f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a4c7f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a4c7f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a4c7f-112">Area:</span></span>  <br/> |<span data-ttu-id="a4c7f-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="a4c7f-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4c7f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4c7f-114">Remarks</span></span>

<span data-ttu-id="a4c7f-115">Wenn ein Transportanbieter eine übermittelte Nachricht findet, deren Eigenschaft auf TRUE festgelegt ist, wird diese Eigenschaft auf den MTS-Bezeichner für diese Nachricht gesetzt.</span><span class="sxs-lookup"><span data-stu-id="a4c7f-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="a4c7f-116">Nach der Übertragung wird diese Eigenschaft mit der Nachricht im Ordner "Gesendete Elemente" zwischenmenschlichen Nachrichten (IPM) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a4c7f-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="a4c7f-117">Messaging Systeme, die eine Korrelation durch MTS-ID, wie X. 400, unterstützen, behalten den Bezeichner als Teil des Transport Umschlags der ursprünglichen Nachricht und auch für alle als Antwort generierten Berichte bei.</span><span class="sxs-lookup"><span data-stu-id="a4c7f-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="a4c7f-118">Wenn ein Bericht von einem solchen Messagingsystem übermittelt wird, wird diese Eigenschaft vom Transportanbieter auf den ursprünglichen MTS-Bezeichner aus dem Transport Umschlag des Berichts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a4c7f-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="a4c7f-119">Diese Eigenschaft wird dann mit dem Bericht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a4c7f-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="a4c7f-120">Eine Clientanwendung kann einen Suchergebnisordner aller Nachrichten mit dieser Eigenschaft verwalten.</span><span class="sxs-lookup"><span data-stu-id="a4c7f-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="a4c7f-121">Wenn ein Bericht für eine solche Nachricht eingeht, kann der Client Einschränkungen für den Ordner Suchergebnisse anwenden, die ursprüngliche Version der Nachricht suchen und die ursprünglichen Nachrichten Informationen mit den neuen Informationen korrelieren.</span><span class="sxs-lookup"><span data-stu-id="a4c7f-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a4c7f-122">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a4c7f-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a4c7f-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="a4c7f-123">Header files</span></span>

<span data-ttu-id="a4c7f-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a4c7f-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="a4c7f-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="a4c7f-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="a4c7f-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a4c7f-126">Mapitags.h</span></span>
  
> <span data-ttu-id="a4c7f-127">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="a4c7f-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a4c7f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4c7f-128">See also</span></span>



[<span data-ttu-id="a4c7f-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a4c7f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a4c7f-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a4c7f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a4c7f-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a4c7f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a4c7f-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a4c7f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

