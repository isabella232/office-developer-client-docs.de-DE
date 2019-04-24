---
title: Kanonische Pidtagattachpayloadproviderguidstring (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5051784ea08316477f3c8888ada9170e3d99c2b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361103"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a><span data-ttu-id="23600-103">Kanonische Pidtagattachpayloadproviderguidstring (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="23600-103">PidTagAttachPayloadProviderGuidString Canonical Property</span></span>

  
  
<span data-ttu-id="23600-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23600-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23600-105">Enthält den Wert eines MIME-Headerfelds für X-Payload-Provider-GUID.</span><span class="sxs-lookup"><span data-stu-id="23600-105">Contains the value of a MIME X-Payload-Provider-Guid header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23600-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="23600-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23600-107">PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W</span><span class="sxs-lookup"><span data-stu-id="23600-107">PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W</span></span>  <br/> |
|<span data-ttu-id="23600-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="23600-108">Identifier:</span></span>  <br/> |<span data-ttu-id="23600-109">0x3719</span><span class="sxs-lookup"><span data-stu-id="23600-109">0x3719</span></span>  <br/> |
|<span data-ttu-id="23600-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="23600-110">Data type:</span></span>  <br/> |<span data-ttu-id="23600-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="23600-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="23600-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="23600-112">Area:</span></span>  <br/> |<span data-ttu-id="23600-113">Outlook-Anwendung</span><span class="sxs-lookup"><span data-stu-id="23600-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23600-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23600-114">Remarks</span></span>

<span data-ttu-id="23600-115">Um den Wert dieser Eigenschaften festzulegen, sollten MIME-Clients ein Headerfeld X-Payload-Provider-GUID in eine MIME-Entität schreiben, die als Anlage analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="23600-115">To set the value of these properties, MIME clients should write an X-Payload-Provider-Guid header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="23600-116">MIME-Leser müssen diesen Kopfzeilen Feldwert in den Wert der entsprechenden Eigenschaft kopieren.</span><span class="sxs-lookup"><span data-stu-id="23600-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="23600-117">MIME-Leser sollten dieses Kopfzeilenfeld ignorieren, wenn es auf einer MIME-Entität angezeigt wird, die als Nachricht oder Nachrichtentext analysiert wird, und nicht als Anlage.</span><span class="sxs-lookup"><span data-stu-id="23600-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="23600-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="23600-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23600-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="23600-119">Protocol specifications</span></span>

<span data-ttu-id="23600-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23600-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23600-121">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="23600-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="23600-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23600-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23600-123">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="23600-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23600-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="23600-124">Header files</span></span>

<span data-ttu-id="23600-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="23600-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="23600-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="23600-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="23600-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="23600-127">Mapitags.h</span></span>
  
> <span data-ttu-id="23600-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="23600-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23600-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23600-129">See also</span></span>



[<span data-ttu-id="23600-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23600-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23600-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23600-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23600-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="23600-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23600-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="23600-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

