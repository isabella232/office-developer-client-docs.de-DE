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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358814"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="f7f77-103">PidTagTextAttachmentCharset (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f7f77-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="f7f77-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7f77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7f77-105">Enthält den Zeichensatzwert einer Nachrichtenanlage.</span><span class="sxs-lookup"><span data-stu-id="f7f77-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7f77-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f7f77-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7f77-107">Keine</span><span class="sxs-lookup"><span data-stu-id="f7f77-107">None</span></span>  <br/> |
|<span data-ttu-id="f7f77-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f7f77-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7f77-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="f7f77-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="f7f77-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f7f77-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7f77-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f7f77-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f7f77-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f7f77-112">Area:</span></span>  <br/> |<span data-ttu-id="f7f77-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="f7f77-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7f77-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f7f77-114">Remarks</span></span>

<span data-ttu-id="f7f77-115">Die Daten dieser Eigenschaft werden von einem Content-Type-MIME-Headerfeld abgeleitet, das mit "text/" beginnt, wenn ein "charset"-Parameter vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f7f77-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f7f77-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f7f77-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7f77-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f7f77-117">Protocol specifications</span></span>

<span data-ttu-id="f7f77-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7f77-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7f77-119">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="f7f77-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7f77-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="f7f77-120">Header files</span></span>

<span data-ttu-id="f7f77-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7f77-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7f77-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f7f77-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7f77-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7f77-123">Mapitags.h</span></span>
  
> <span data-ttu-id="f7f77-124">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f7f77-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7f77-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7f77-125">See also</span></span>



[<span data-ttu-id="f7f77-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f7f77-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7f77-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="f7f77-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7f77-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f7f77-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7f77-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f7f77-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

