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
ms.openlocfilehash: 1db41bc5c7ea71d65d892da520d4258354eb53cf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401538"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="dd966-103">PidTagTextAttachmentCharset (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dd966-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="dd966-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd966-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd966-105">Enthält eine e-Mail-Nachrichtenanhang Zeichen festgelegter Wert.</span><span class="sxs-lookup"><span data-stu-id="dd966-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd966-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dd966-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dd966-107">Keine</span><span class="sxs-lookup"><span data-stu-id="dd966-107">None</span></span>  <br/> |
|<span data-ttu-id="dd966-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="dd966-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dd966-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="dd966-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="dd966-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dd966-110">Data type:</span></span>  <br/> |<span data-ttu-id="dd966-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dd966-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dd966-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dd966-112">Area:</span></span>  <br/> |<span data-ttu-id="dd966-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="dd966-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd966-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dd966-114">Remarks</span></span>

<span data-ttu-id="dd966-115">Diese Eigenschaft Daten aus einem Feld der MIME-Inhaltstyp-Header, die mit beginnt abgeleitet ist "Text /", wenn der Parameter "Charset" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="dd966-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dd966-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dd966-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dd966-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="dd966-117">Protocol specifications</span></span>

<span data-ttu-id="dd966-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd966-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd966-119">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="dd966-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dd966-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="dd966-120">Header files</span></span>

<span data-ttu-id="dd966-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dd966-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="dd966-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="dd966-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="dd966-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dd966-123">Mapitags.h</span></span>
  
> <span data-ttu-id="dd966-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dd966-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dd966-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd966-125">See also</span></span>



[<span data-ttu-id="dd966-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd966-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dd966-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd966-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dd966-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dd966-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dd966-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dd966-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

