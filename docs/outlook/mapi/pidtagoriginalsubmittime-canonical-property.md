---
title: Kanonische Pidtagoriginalsubmittime (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubmitTime
api_type:
- COM
ms.assetid: 2e027c0c-2370-437a-ad98-2bbb5e41e525
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 07aea33f54a29d497646b62f1f8bd96a383cbd7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341048"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="5b773-103">Kanonische Pidtagoriginalsubmittime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5b773-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="5b773-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b773-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b773-105">Enthält das Datum und die Uhrzeit der ursprünglichen Übermittlung der Nachricht im Bericht.</span><span class="sxs-lookup"><span data-stu-id="5b773-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b773-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5b773-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b773-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="5b773-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="5b773-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5b773-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b773-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="5b773-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="5b773-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5b773-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b773-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5b773-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5b773-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5b773-112">Area:</span></span>  <br/> |<span data-ttu-id="5b773-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="5b773-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b773-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b773-114">Remarks</span></span>

<span data-ttu-id="5b773-115">Bei der ersten Übermittlung einer Nachricht sollte eine Clientanwendung diese Eigenschaft auf den Wert der **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="5b773-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="5b773-116">Sie wird nicht geändert, wenn die Nachricht weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="5b773-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="5b773-117">Diese wird nur in Berichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b773-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5b773-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5b773-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b773-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5b773-119">Protocol specifications</span></span>

<span data-ttu-id="5b773-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b773-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b773-121">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5b773-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5b773-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b773-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b773-123">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5b773-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b773-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="5b773-124">Header files</span></span>

<span data-ttu-id="5b773-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5b773-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b773-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5b773-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b773-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5b773-127">Mapitags.h</span></span>
  
> <span data-ttu-id="5b773-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5b773-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b773-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b773-129">See also</span></span>



[<span data-ttu-id="5b773-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b773-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b773-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b773-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b773-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5b773-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b773-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5b773-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

