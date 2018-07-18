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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cef412d212bf29cfd1a1d5c4b2911440fae6a15e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794120"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a><span data-ttu-id="2408b-103">PidTagAttachPayloadClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2408b-103">PidTagAttachPayloadClass Canonical Property</span></span>

  
  
<span data-ttu-id="2408b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2408b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2408b-105">Enthält den Wert eines Felds Kopfzeile MIME-X-Nutzlast-Klasse.</span><span class="sxs-lookup"><span data-stu-id="2408b-105">Contains the value of a MIME X-Payload-Class header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2408b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2408b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2408b-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="2408b-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="2408b-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="2408b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2408b-109">0x371A</span><span class="sxs-lookup"><span data-stu-id="2408b-109">0x371A</span></span>  <br/> |
|<span data-ttu-id="2408b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2408b-110">Data type:</span></span>  <br/> |<span data-ttu-id="2408b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2408b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2408b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2408b-112">Area:</span></span>  <br/> |<span data-ttu-id="2408b-113">Outlook-Anwendung</span><span class="sxs-lookup"><span data-stu-id="2408b-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2408b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2408b-114">Remarks</span></span>

<span data-ttu-id="2408b-115">Um den Wert dieser Eigenschaften festzulegen, sollte MIME-Clients ein Kopfzeilenfeld X-Nutzlast-Klasse in eine MIME-Entität geschrieben werden, die als Anlage analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="2408b-115">To set the value of these properties, MIME clients should write an X-Payload-Class header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="2408b-116">MIME-Leser müssen diese Kopfzeile Feldwert auf den Wert der entsprechenden Eigenschaft kopieren.</span><span class="sxs-lookup"><span data-stu-id="2408b-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="2408b-117">MIME-Leser sollten diese Kopfzeilenfeld ignorieren, wenn sie auf eine Entität MIME angezeigt, die als einer Nachricht oder dem Nachrichtentext, statt die Daten als Anlage analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="2408b-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2408b-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2408b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2408b-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2408b-119">Protocol specifications</span></span>

<span data-ttu-id="2408b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2408b-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2408b-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2408b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2408b-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2408b-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2408b-123">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="2408b-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2408b-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2408b-124">Header files</span></span>

<span data-ttu-id="2408b-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2408b-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2408b-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2408b-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="2408b-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2408b-127">Mapitags.h</span></span>
  
> <span data-ttu-id="2408b-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2408b-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2408b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2408b-129">See also</span></span>



[<span data-ttu-id="2408b-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2408b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2408b-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2408b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2408b-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2408b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2408b-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2408b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

