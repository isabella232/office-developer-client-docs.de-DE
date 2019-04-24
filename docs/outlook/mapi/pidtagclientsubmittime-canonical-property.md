---
title: Kanonische PidTagClientSubmitTime-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 851441e419c17d8f5fef27c785ea4b829a4ae443
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345717"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="afd5d-103">Kanonische PidTagClientSubmitTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="afd5d-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="afd5d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="afd5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="afd5d-105">Enthält das Datum und die Uhrzeit, zu der der Nachrichtenabsender eine Nachricht übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="afd5d-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="afd5d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="afd5d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="afd5d-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="afd5d-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="afd5d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="afd5d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="afd5d-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="afd5d-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="afd5d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="afd5d-110">Data type:</span></span>  <br/> |<span data-ttu-id="afd5d-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="afd5d-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="afd5d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="afd5d-112">Area:</span></span>  <br/> |<span data-ttu-id="afd5d-113">Nachrichten Zeit</span><span class="sxs-lookup"><span data-stu-id="afd5d-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="afd5d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afd5d-114">Remarks</span></span>

<span data-ttu-id="afd5d-115">Der Informationsspeicher Anbieter legt **PR_CLIENT_SUBMIT_TIME** auf die Zeit fest, die die Client Anwendung [IMessage:: SubmitMessage](imessage-submitmessage.md)aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="afd5d-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="afd5d-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="afd5d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="afd5d-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="afd5d-117">Protocol specifications</span></span>

<span data-ttu-id="afd5d-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="afd5d-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="afd5d-119">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="afd5d-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="afd5d-120">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="afd5d-120">Header files</span></span>

<span data-ttu-id="afd5d-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="afd5d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="afd5d-122">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="afd5d-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="afd5d-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="afd5d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="afd5d-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="afd5d-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="afd5d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afd5d-125">See also</span></span>



[<span data-ttu-id="afd5d-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="afd5d-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="afd5d-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="afd5d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="afd5d-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="afd5d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="afd5d-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="afd5d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

