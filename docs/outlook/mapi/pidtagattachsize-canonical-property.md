---
title: PidTagAttachSize (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f3e4f19ab43a3da7c4840d762d5131813c83d996
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361089"
---
# <a name="pidtagattachsize-canonical-property"></a><span data-ttu-id="d72e1-103">PidTagAttachSize (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d72e1-103">PidTagAttachSize Canonical Property</span></span>

  
  
<span data-ttu-id="d72e1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d72e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d72e1-105">Enthält die Summe aller Eigenschaften einer Anlage in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d72e1-105">Contains the sum, in bytes, of the sizes of all properties on an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d72e1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d72e1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d72e1-107">PR_ATTACH_SIZE</span><span class="sxs-lookup"><span data-stu-id="d72e1-107">PR_ATTACH_SIZE</span></span>  <br/> |
|<span data-ttu-id="d72e1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d72e1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d72e1-109">0x0E20</span><span class="sxs-lookup"><span data-stu-id="d72e1-109">0x0E20</span></span>  <br/> |
|<span data-ttu-id="d72e1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d72e1-110">Data type:</span></span>  <br/> |<span data-ttu-id="d72e1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d72e1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d72e1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d72e1-112">Area:</span></span>  <br/> |<span data-ttu-id="d72e1-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="d72e1-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d72e1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d72e1-114">Remarks</span></span>

<span data-ttu-id="d72e1-115">Es wird empfohlen, dass Anlagenunterobjekte die PR_ATTACH_SIZE **verfügbar** machen.</span><span class="sxs-lookup"><span data-stu-id="d72e1-115">It is recommended that attachment subobjects expose the **PR_ATTACH_SIZE** property.</span></span> <span data-ttu-id="d72e1-116">Die summe in **PR_ATTACH_SIZE** enthält die Größe der **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) oder **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d72e1-116">The sum contained in **PR_ATTACH_SIZE** includes the size of the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> <span data-ttu-id="d72e1-117">Dementsprechend ist **PR_ATTACH_SIZE** in der Regel größer als der Inhalt der Anlage allein.</span><span class="sxs-lookup"><span data-stu-id="d72e1-117">Accordingly, **PR_ATTACH_SIZE** is usually larger than the contents of the attachment alone.</span></span> 
  
<span data-ttu-id="d72e1-118">Diese Eigenschaft kann verwendet werden, um die ungefähre Größe der Anlage vor der Remoteübertragung per Modem zu überprüfen und Statusanzeigen beim Speichern der Anlage auf dem Datenträger zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="d72e1-118">This property can be used to check the approximate size of the attachment before performing a remote transfer by modem and to display progress indicators when saving the attachment to disk.</span></span> <span data-ttu-id="d72e1-119">Dies ist besonders bei angefügten OLE-Objekten hilfreich.</span><span class="sxs-lookup"><span data-stu-id="d72e1-119">It is particularly useful with attached OLE objects.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d72e1-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d72e1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d72e1-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d72e1-121">Protocol specifications</span></span>

<span data-ttu-id="d72e1-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d72e1-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d72e1-123">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="d72e1-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d72e1-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d72e1-124">Header files</span></span>

<span data-ttu-id="d72e1-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d72e1-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d72e1-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d72e1-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d72e1-127">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d72e1-127">mapitags.h</span></span>
  
> <span data-ttu-id="d72e1-128">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d72e1-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d72e1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d72e1-129">See also</span></span>



[<span data-ttu-id="d72e1-130">PidTagMessageSize (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d72e1-130">PidTagMessageSize Canonical Property</span></span>](pidtagmessagesize-canonical-property.md)


[<span data-ttu-id="d72e1-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d72e1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d72e1-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d72e1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d72e1-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d72e1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d72e1-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d72e1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

