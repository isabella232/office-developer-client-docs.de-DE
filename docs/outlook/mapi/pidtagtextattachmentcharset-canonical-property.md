---
title: PidTagTextAttachmentCharset (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cec34819cfa2c6e790f8808eb5bab70412f286b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591429"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="40fd7-103">PidTagTextAttachmentCharset (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="40fd7-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="40fd7-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40fd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40fd7-105">Enthält eine e-Mail-Nachrichtenanhang Zeichen festgelegter Wert.</span><span class="sxs-lookup"><span data-stu-id="40fd7-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40fd7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="40fd7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40fd7-107">Keine</span><span class="sxs-lookup"><span data-stu-id="40fd7-107">None</span></span>  <br/> |
|<span data-ttu-id="40fd7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="40fd7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="40fd7-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="40fd7-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="40fd7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="40fd7-110">Data type:</span></span>  <br/> |<span data-ttu-id="40fd7-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40fd7-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="40fd7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="40fd7-112">Area:</span></span>  <br/> |<span data-ttu-id="40fd7-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="40fd7-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40fd7-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="40fd7-114">Remarks</span></span>

<span data-ttu-id="40fd7-115">Diese Eigenschaft Daten aus einem Feld der MIME-Inhaltstyp-Header, die mit beginnt abgeleitet ist "Text /", wenn der Parameter "Charset" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="40fd7-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="40fd7-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="40fd7-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40fd7-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="40fd7-117">Protocol specifications</span></span>

<span data-ttu-id="40fd7-118">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40fd7-118">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40fd7-119">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="40fd7-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40fd7-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="40fd7-120">Header files</span></span>

<span data-ttu-id="40fd7-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40fd7-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="40fd7-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="40fd7-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="40fd7-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="40fd7-123">Mapitags.h</span></span>
  
> <span data-ttu-id="40fd7-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="40fd7-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40fd7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40fd7-125">See also</span></span>



[<span data-ttu-id="40fd7-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40fd7-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40fd7-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="40fd7-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40fd7-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="40fd7-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40fd7-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="40fd7-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

