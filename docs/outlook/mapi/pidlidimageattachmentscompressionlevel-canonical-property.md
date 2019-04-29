---
title: Kanonische Pidlidimageattachmentscompressionlevel (-Eigenschaft
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
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="4aadf-103">Kanonische Pidlidimageattachmentscompressionlevel (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4aadf-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="4aadf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4aadf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4aadf-105">Definiert eine Komprimierungsstufe für Bildanlagen.</span><span class="sxs-lookup"><span data-stu-id="4aadf-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4aadf-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4aadf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4aadf-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="4aadf-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="4aadf-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="4aadf-108">Property set:</span></span>  <br/> |<span data-ttu-id="4aadf-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4aadf-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4aadf-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="4aadf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4aadf-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="4aadf-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="4aadf-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4aadf-112">Data type:</span></span>  <br/> |<span data-ttu-id="4aadf-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4aadf-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4aadf-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4aadf-114">Area:</span></span>  <br/> |<span data-ttu-id="4aadf-115">Laufzeitkonfiguration</span><span class="sxs-lookup"><span data-stu-id="4aadf-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4aadf-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4aadf-116">Remarks</span></span>

<span data-ttu-id="4aadf-117">Es folgen die folgenden gültigen Komprimierungsstufen:</span><span class="sxs-lookup"><span data-stu-id="4aadf-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="4aadf-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4aadf-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4aadf-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4aadf-119">Protocol specifications</span></span>

<span data-ttu-id="4aadf-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="4aadf-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="4aadf-121">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="4aadf-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4aadf-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="4aadf-122">Header files</span></span>

<span data-ttu-id="4aadf-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4aadf-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="4aadf-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="4aadf-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4aadf-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4aadf-125">See also</span></span>



[<span data-ttu-id="4aadf-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4aadf-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4aadf-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4aadf-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4aadf-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4aadf-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4aadf-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4aadf-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

