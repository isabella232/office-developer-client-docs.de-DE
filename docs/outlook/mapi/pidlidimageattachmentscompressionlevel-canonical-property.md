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
ms.openlocfilehash: 55b965374bb1d7e5859f0cac5cc2f61956ea5b55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578920"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="53dc9-103">PidLidImageAttachmentsCompressionLevel (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="53dc9-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="53dc9-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53dc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53dc9-105">Definiert eine Komprimierungsebene auf Bildanlagen angewendet.</span><span class="sxs-lookup"><span data-stu-id="53dc9-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53dc9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="53dc9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53dc9-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="53dc9-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="53dc9-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="53dc9-108">Property set:</span></span>  <br/> |<span data-ttu-id="53dc9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="53dc9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="53dc9-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="53dc9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="53dc9-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="53dc9-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="53dc9-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="53dc9-112">Data type:</span></span>  <br/> |<span data-ttu-id="53dc9-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="53dc9-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="53dc9-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="53dc9-114">Area:</span></span>  <br/> |<span data-ttu-id="53dc9-115">Laufzeit-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="53dc9-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53dc9-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="53dc9-116">Remarks</span></span>

<span data-ttu-id="53dc9-117">Im folgenden sind die gültigen Komprimierung Ebenen:</span><span class="sxs-lookup"><span data-stu-id="53dc9-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="53dc9-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="53dc9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53dc9-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="53dc9-119">Protocol specifications</span></span>

<span data-ttu-id="53dc9-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="53dc9-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="53dc9-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="53dc9-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="53dc9-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="53dc9-122">Header files</span></span>

<span data-ttu-id="53dc9-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53dc9-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="53dc9-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="53dc9-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53dc9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53dc9-125">See also</span></span>



[<span data-ttu-id="53dc9-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53dc9-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53dc9-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53dc9-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53dc9-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="53dc9-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53dc9-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="53dc9-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

