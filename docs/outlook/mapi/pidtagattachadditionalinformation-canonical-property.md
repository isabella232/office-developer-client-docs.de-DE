---
title: PidTagAttachAdditionalInformation (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 83de3a4ad7c93b2dfee8063ab63bfbf0724a5f61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794077"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a><span data-ttu-id="5c987-103">PidTagAttachAdditionalInformation (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5c987-103">PidTagAttachAdditionalInformation Canonical Property</span></span>

  
  
<span data-ttu-id="5c987-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5c987-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5c987-105">Dateitypinformationen für eine nicht-Windows-Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="5c987-105">Provides file type information for a non-Windows attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c987-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5c987-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c987-107">PR_ATTACH_ADDITIONAL_INFO</span><span class="sxs-lookup"><span data-stu-id="5c987-107">PR_ATTACH_ADDITIONAL_INFO</span></span>  <br/> |
|<span data-ttu-id="5c987-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5c987-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5c987-109">0x370F</span><span class="sxs-lookup"><span data-stu-id="5c987-109">0x370F</span></span>  <br/> |
|<span data-ttu-id="5c987-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5c987-110">Data type:</span></span>  <br/> |<span data-ttu-id="5c987-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5c987-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5c987-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5c987-112">Area:</span></span>  <br/> |<span data-ttu-id="5c987-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="5c987-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c987-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c987-114">Remarks</span></span>

<span data-ttu-id="5c987-115">Diese Eigenschaft stellt die Metadaten für eine bestimmte Anlage basierend auf der Anlage-Codierung.</span><span class="sxs-lookup"><span data-stu-id="5c987-115">This property provides metadata about a particular attachment based on the attachment's encoding.</span></span> <span data-ttu-id="5c987-116">Wenn die Eigenschaft **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) MacBinary enthält, enthält **PR_ATTACH_ADDITIONAL_INFO** beispielsweise eine Zeichenfolge, die der Ersteller der Macintosh-Datei und der Dateityp, formatiert als ":CREA:TYPE" darstellt für die codierte Macintosh-Datei.</span><span class="sxs-lookup"><span data-stu-id="5c987-116">For example, when the **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) property contains MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contains a string that represents the Macintosh file creator and file type, formatted as ":CREA:TYPE" for the encoded Macintosh file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5c987-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5c987-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5c987-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5c987-118">Protocol specifications</span></span>

<span data-ttu-id="5c987-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c987-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c987-120">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="5c987-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5c987-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5c987-121">Header files</span></span>

<span data-ttu-id="5c987-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c987-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c987-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5c987-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="5c987-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5c987-124">Mapitags.h</span></span>
  
> <span data-ttu-id="5c987-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5c987-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c987-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c987-126">See also</span></span>



[<span data-ttu-id="5c987-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c987-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c987-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c987-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c987-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5c987-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c987-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5c987-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

