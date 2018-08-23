---
title: PidTagAttachPayloadProviderGuidString (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadProviderGuidString
api_type:
- HeaderDef
ms.assetid: c9d4b561-53b3-492b-9324-9376dd7abddf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1313ac62bd2ee6c1db27bd1c583f56dadc1bff1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574300"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a><span data-ttu-id="0a901-103">PidTagAttachPayloadProviderGuidString (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0a901-103">PidTagAttachPayloadProviderGuidString Canonical Property</span></span>

  
  
<span data-ttu-id="0a901-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a901-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a901-105">Enthält den Wert eines Felds Kopfzeile MIME-X-Nutzlast-Anbieter-Guid.</span><span class="sxs-lookup"><span data-stu-id="0a901-105">Contains the value of a MIME X-Payload-Provider-Guid header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a901-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0a901-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a901-107">PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W</span><span class="sxs-lookup"><span data-stu-id="0a901-107">PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W</span></span>  <br/> |
|<span data-ttu-id="0a901-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0a901-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0a901-109">0x3719</span><span class="sxs-lookup"><span data-stu-id="0a901-109">0x3719</span></span>  <br/> |
|<span data-ttu-id="0a901-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0a901-110">Data type:</span></span>  <br/> |<span data-ttu-id="0a901-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0a901-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0a901-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0a901-112">Area:</span></span>  <br/> |<span data-ttu-id="0a901-113">Outlook-Anwendung</span><span class="sxs-lookup"><span data-stu-id="0a901-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a901-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="0a901-114">Remarks</span></span>

<span data-ttu-id="0a901-115">Um den Wert dieser Eigenschaften festzulegen, sollte MIME-Clients ein Kopfzeilenfeld X-Nutzlast-Anbieter-Guid in eine MIME-Entität geschrieben werden, die als Anlage analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a901-115">To set the value of these properties, MIME clients should write an X-Payload-Provider-Guid header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="0a901-116">MIME-Leser müssen diese Kopfzeile Feldwert auf den Wert der entsprechenden Eigenschaft kopieren.</span><span class="sxs-lookup"><span data-stu-id="0a901-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="0a901-117">MIME-Leser sollten diese Kopfzeilenfeld ignorieren, wenn sie auf eine Entität MIME angezeigt, die als einer Nachricht oder dem Nachrichtentext, statt die Daten als Anlage analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a901-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0a901-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0a901-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0a901-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0a901-119">Protocol specifications</span></span>

<span data-ttu-id="0a901-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a901-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a901-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0a901-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0a901-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a901-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a901-123">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="0a901-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0a901-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0a901-124">Header files</span></span>

<span data-ttu-id="0a901-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a901-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a901-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0a901-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0a901-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0a901-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0a901-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0a901-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a901-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a901-129">See also</span></span>



[<span data-ttu-id="0a901-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a901-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a901-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a901-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a901-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0a901-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a901-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0a901-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

