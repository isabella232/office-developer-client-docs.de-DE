---
title: PidTagOriginalSubmitTime (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 43d0387f1c25c5ac86168caaddddd9fb9171c827
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794723"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="bf869-103">PidTagOriginalSubmitTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bf869-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="bf869-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf869-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf869-105">Die ursprünglichen Übermittlung-Datum und Uhrzeit der Nachricht in den Bericht enthält.</span><span class="sxs-lookup"><span data-stu-id="bf869-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf869-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bf869-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf869-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="bf869-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="bf869-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="bf869-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf869-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="bf869-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="bf869-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bf869-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf869-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="bf869-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="bf869-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bf869-112">Area:</span></span>  <br/> |<span data-ttu-id="bf869-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="bf869-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf869-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf869-114">Remarks</span></span>

<span data-ttu-id="bf869-115">Am ersten Übermittlung einer Nachricht sollte eine Clientanwendung diese Eigenschaft auf den Wert der Eigenschaft **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bf869-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="bf869-116">Er wird nicht geändert, wenn die Nachricht weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="bf869-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="bf869-117">In nur-Berichten wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf869-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bf869-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bf869-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bf869-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bf869-119">Protocol specifications</span></span>

<span data-ttu-id="bf869-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf869-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf869-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bf869-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bf869-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf869-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf869-123">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bf869-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bf869-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bf869-124">Header files</span></span>

<span data-ttu-id="bf869-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf869-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf869-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bf869-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf869-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bf869-127">Mapitags.h</span></span>
  
> <span data-ttu-id="bf869-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bf869-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf869-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf869-129">See also</span></span>



[<span data-ttu-id="bf869-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf869-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf869-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf869-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf869-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bf869-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf869-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bf869-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

