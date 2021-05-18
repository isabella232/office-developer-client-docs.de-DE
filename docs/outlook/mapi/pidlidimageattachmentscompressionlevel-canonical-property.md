---
title: PidLidImageAttachmentsCompressionLevel (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidImageAttachmentsCompressionLevel
api_type:
- COM
ms.assetid: cc169ba8-e9b7-42ad-8f0e-77b0843f95ea
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8600cc7071fbe5c08d5df074f9bf59f4320b7f18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413829"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="aaf4f-103">PidLidImageAttachmentsCompressionLevel (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aaf4f-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="aaf4f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aaf4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aaf4f-105">Definiert eine Komprimierungsstufe, die auf Bildanlagen angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aaf4f-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aaf4f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="aaf4f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aaf4f-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="aaf4f-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="aaf4f-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="aaf4f-108">Property set:</span></span>  <br/> |<span data-ttu-id="aaf4f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="aaf4f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="aaf4f-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="aaf4f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="aaf4f-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="aaf4f-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="aaf4f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="aaf4f-112">Data type:</span></span>  <br/> |<span data-ttu-id="aaf4f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="aaf4f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="aaf4f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="aaf4f-114">Area:</span></span>  <br/> |<span data-ttu-id="aaf4f-115">Laufzeitkonfiguration</span><span class="sxs-lookup"><span data-stu-id="aaf4f-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aaf4f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aaf4f-116">Remarks</span></span>

<span data-ttu-id="aaf4f-117">Es folgen gültige Komprimierungsstufen:</span><span class="sxs-lookup"><span data-stu-id="aaf4f-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="aaf4f-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aaf4f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aaf4f-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="aaf4f-119">Protocol specifications</span></span>

<span data-ttu-id="aaf4f-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="aaf4f-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="aaf4f-121">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="aaf4f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aaf4f-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="aaf4f-122">Header files</span></span>

<span data-ttu-id="aaf4f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aaf4f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="aaf4f-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="aaf4f-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aaf4f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aaf4f-125">See also</span></span>



[<span data-ttu-id="aaf4f-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aaf4f-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aaf4f-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="aaf4f-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aaf4f-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="aaf4f-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aaf4f-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="aaf4f-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

