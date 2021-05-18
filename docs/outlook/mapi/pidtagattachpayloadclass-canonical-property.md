---
title: PidTagAttachPayloadClass (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadClass
api_type:
- HeaderDef
ms.assetid: bc4de217-8241-45e7-9e97-8f0c1b16691a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6a84e51325fcb60c54c2f6b42af0c26a0efd3382
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327237"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a><span data-ttu-id="4bfb7-103">PidTagAttachPayloadClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4bfb7-103">PidTagAttachPayloadClass Canonical Property</span></span>

  
  
<span data-ttu-id="4bfb7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4bfb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4bfb7-105">Enthält den Wert eines MIME X-Payload-Class-Headerfelds.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-105">Contains the value of a MIME X-Payload-Class header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4bfb7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4bfb7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4bfb7-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="4bfb7-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="4bfb7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4bfb7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4bfb7-109">0x371A</span><span class="sxs-lookup"><span data-stu-id="4bfb7-109">0x371A</span></span>  <br/> |
|<span data-ttu-id="4bfb7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4bfb7-110">Data type:</span></span>  <br/> |<span data-ttu-id="4bfb7-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4bfb7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4bfb7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4bfb7-112">Area:</span></span>  <br/> |<span data-ttu-id="4bfb7-113">Outlook-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4bfb7-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4bfb7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4bfb7-114">Remarks</span></span>

<span data-ttu-id="4bfb7-115">Zum Festlegen des Werts dieser Eigenschaften sollten MIME-Clients ein X-Payload-Class-Headerfeld in eine MIME-Entität schreiben, die als Anlage analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-115">To set the value of these properties, MIME clients should write an X-Payload-Class header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="4bfb7-116">MIME-Reader müssen diesen Headerfeldwert in den Wert der entsprechenden Eigenschaft kopieren.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="4bfb7-117">MIME-Leser sollten dieses Kopfzeilenfeld ignorieren, wenn es in einer MIME-Entität angezeigt wird, die als Nachrichten- oder Nachrichtentext und nicht als Anlage analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4bfb7-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4bfb7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4bfb7-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4bfb7-119">Protocol specifications</span></span>

<span data-ttu-id="4bfb7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4bfb7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4bfb7-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4bfb7-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4bfb7-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4bfb7-123">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4bfb7-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="4bfb7-124">Header files</span></span>

<span data-ttu-id="4bfb7-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4bfb7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4bfb7-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="4bfb7-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4bfb7-127">Mapitags.h</span></span>
  
> <span data-ttu-id="4bfb7-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4bfb7-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4bfb7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bfb7-129">See also</span></span>



[<span data-ttu-id="4bfb7-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4bfb7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4bfb7-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="4bfb7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4bfb7-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4bfb7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4bfb7-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4bfb7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

