---
title: Kanonische Pidtagmessagesubmissionid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSubmissionId
api_type:
- HeaderDef
ms.assetid: 0a799fe5-04e2-4e1d-b0cd-9bdd2577d299
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 723affa054cb35a9cc7a2ee28e051e3b9a6d04e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329400"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a><span data-ttu-id="6a2cb-103">Kanonische Pidtagmessagesubmissionid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6a2cb-103">PidTagMessageSubmissionId Canonical Property</span></span>

  
  
<span data-ttu-id="6a2cb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a2cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a2cb-105">Enthält einen MTS-Bezeichner (Message Transfer System) für den MTA (Message Transfer Agent).</span><span class="sxs-lookup"><span data-stu-id="6a2cb-105">Contains a message transfer system (MTS) identifier for the message transfer agent (MTA).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a2cb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6a2cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6a2cb-107">PR_MESSAGE_SUBMISSION_ID</span><span class="sxs-lookup"><span data-stu-id="6a2cb-107">PR_MESSAGE_SUBMISSION_ID</span></span>  <br/> |
|<span data-ttu-id="6a2cb-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6a2cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6a2cb-109">0x0047</span><span class="sxs-lookup"><span data-stu-id="6a2cb-109">0x0047</span></span>  <br/> |
|<span data-ttu-id="6a2cb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6a2cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="6a2cb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6a2cb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6a2cb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6a2cb-112">Area:</span></span>  <br/> |<span data-ttu-id="6a2cb-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="6a2cb-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a2cb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a2cb-114">Remarks</span></span>

<span data-ttu-id="6a2cb-115">Diese Eigenschaft wird vom MTA nach erfolgreichem Abschluss der Nachrichtenübermittlung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6a2cb-115">This property is returned by the MTA upon successful completion of message submission.</span></span> <span data-ttu-id="6a2cb-116">Jeder zukünftige Kontakt mit dem MTA zu dieser Nachricht, wie zum Beispiel das Anfordern einer Stornierung, verwendet den MTS-Bezeichner in dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6a2cb-116">Any future contact with the MTA regarding this message, such as requesting cancellation, uses the MTS identifier in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6a2cb-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6a2cb-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6a2cb-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6a2cb-118">Protocol specifications</span></span>

<span data-ttu-id="6a2cb-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a2cb-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a2cb-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6a2cb-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6a2cb-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a2cb-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a2cb-122">Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.</span><span class="sxs-lookup"><span data-stu-id="6a2cb-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6a2cb-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="6a2cb-123">Header files</span></span>

<span data-ttu-id="6a2cb-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6a2cb-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a2cb-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="6a2cb-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6a2cb-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6a2cb-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6a2cb-127">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="6a2cb-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a2cb-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a2cb-128">See also</span></span>



[<span data-ttu-id="6a2cb-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a2cb-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a2cb-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a2cb-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a2cb-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6a2cb-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a2cb-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6a2cb-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

