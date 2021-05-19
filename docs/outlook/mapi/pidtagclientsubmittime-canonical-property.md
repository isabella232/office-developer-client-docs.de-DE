---
title: PidTagClientSubmitTime (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 851441e419c17d8f5fef27c785ea4b829a4ae443
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345717"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="d6281-103">PidTagClientSubmitTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d6281-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="d6281-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6281-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6281-105">Enthält das Datum und die Uhrzeit, zu der der Absender der Nachricht eine Nachricht übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="d6281-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6281-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d6281-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6281-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="d6281-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="d6281-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d6281-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6281-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="d6281-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="d6281-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d6281-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6281-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d6281-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d6281-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d6281-112">Area:</span></span>  <br/> |<span data-ttu-id="d6281-113">Nachrichtenzeit</span><span class="sxs-lookup"><span data-stu-id="d6281-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6281-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6281-114">Remarks</span></span>

<span data-ttu-id="d6281-115">Der Speicheranbieter legt **PR_CLIENT_SUBMIT_TIME** auf den Zeitpunkt fest, zu dem die Clientanwendung [IMessage::SubmitMessage aufgerufen hat.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="d6281-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d6281-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d6281-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d6281-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d6281-117">Protocol specifications</span></span>

<span data-ttu-id="d6281-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d6281-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d6281-119">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="d6281-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d6281-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d6281-120">Header files</span></span>

<span data-ttu-id="d6281-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6281-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6281-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d6281-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6281-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d6281-123">Mapitags.h</span></span>
  
> <span data-ttu-id="d6281-124">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d6281-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6281-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6281-125">See also</span></span>



[<span data-ttu-id="d6281-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d6281-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6281-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d6281-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6281-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d6281-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6281-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d6281-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

