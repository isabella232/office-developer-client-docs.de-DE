---
title: Kanonische PidTagTextAttachmentCharset-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTextAttachmentCharset
api_type:
- COM
ms.assetid: d347c949-d0c3-4a36-8447-3fa01111cdc1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c728799832b10ad2d4533a9a040582b67054baad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795265"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="c4e67-103">Kanonische PidTagTextAttachmentCharset-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c4e67-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="c4e67-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4e67-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4e67-105">Enthält eine e-Mail-Nachrichtenanhang Zeichen festgelegter Wert.</span><span class="sxs-lookup"><span data-stu-id="c4e67-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4e67-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c4e67-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4e67-107">Keine</span><span class="sxs-lookup"><span data-stu-id="c4e67-107">None</span></span>  <br/> |
|<span data-ttu-id="c4e67-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="c4e67-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c4e67-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="c4e67-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="c4e67-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c4e67-110">Data type:</span></span>  <br/> |<span data-ttu-id="c4e67-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c4e67-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c4e67-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c4e67-112">Area:</span></span>  <br/> |<span data-ttu-id="c4e67-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="c4e67-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4e67-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c4e67-114">Remarks</span></span>

<span data-ttu-id="c4e67-115">Diese Eigenschaft Daten aus einem Feld der MIME-Inhaltstyp-Header, die mit beginnt abgeleitet ist "Text /", wenn der Parameter "Charset" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c4e67-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c4e67-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c4e67-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4e67-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c4e67-117">Protocol specifications</span></span>

<span data-ttu-id="c4e67-118">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4e67-118">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4e67-119">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="c4e67-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4e67-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c4e67-120">Header files</span></span>

<span data-ttu-id="c4e67-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4e67-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4e67-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c4e67-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="c4e67-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c4e67-123">Mapitags.h</span></span>
  
> <span data-ttu-id="c4e67-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c4e67-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4e67-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4e67-125">See also</span></span>



[<span data-ttu-id="c4e67-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4e67-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4e67-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4e67-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4e67-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c4e67-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4e67-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c4e67-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

