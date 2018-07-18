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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2d6b585c00ffb3d9dd5fb0864d98b0a221c7d8c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794122"
---
# <a name="pidtagattachsize-canonical-property"></a><span data-ttu-id="137e2-103">PidTagAttachSize (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="137e2-103">PidTagAttachSize Canonical Property</span></span>

  
  
<span data-ttu-id="137e2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="137e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="137e2-105">Enthält die Summe der Größen aller Eigenschaften auf eine Anlage in Bytes.</span><span class="sxs-lookup"><span data-stu-id="137e2-105">Contains the sum, in bytes, of the sizes of all properties on an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="137e2-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="137e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="137e2-107">PR_ATTACH_SIZE</span><span class="sxs-lookup"><span data-stu-id="137e2-107">PR_ATTACH_SIZE</span></span>  <br/> |
|<span data-ttu-id="137e2-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="137e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="137e2-109">0x0E20</span><span class="sxs-lookup"><span data-stu-id="137e2-109">0x0E20</span></span>  <br/> |
|<span data-ttu-id="137e2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="137e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="137e2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="137e2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="137e2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="137e2-112">Area:</span></span>  <br/> |<span data-ttu-id="137e2-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="137e2-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="137e2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="137e2-114">Remarks</span></span>

<span data-ttu-id="137e2-115">Es wird empfohlen, dass Anlage Unterobjekte die **PR_ATTACH_SIZE** -Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="137e2-115">It is recommended that attachment subobjects expose the **PR_ATTACH_SIZE** property.</span></span> <span data-ttu-id="137e2-116">Die Summe in **PR_ATTACH_SIZE** enthaltenen enthält die Größe des **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) oder **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="137e2-116">The sum contained in **PR_ATTACH_SIZE** includes the size of the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> <span data-ttu-id="137e2-117">Dementsprechend ist **PR_ATTACH_SIZE** in der Regel größer als der Inhalt der Anlage allein.</span><span class="sxs-lookup"><span data-stu-id="137e2-117">Accordingly, **PR_ATTACH_SIZE** is usually larger than the contents of the attachment alone.</span></span> 
  
<span data-ttu-id="137e2-118">Diese Eigenschaft kann die ungefähre Größe der Anlage vor dem Ausführen einer remote-Übertragung von Modem überprüfen und Statusanzeigen angezeigt wird, wenn die Anlage auf Datenträger speichern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="137e2-118">This property can be used to check the approximate size of the attachment before performing a remote transfer by modem and to display progress indicators when saving the attachment to disk.</span></span> <span data-ttu-id="137e2-119">Es ist besonders nützlich, mit angefügten OLE-Objekten.</span><span class="sxs-lookup"><span data-stu-id="137e2-119">It is particularly useful with attached OLE objects.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="137e2-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="137e2-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="137e2-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="137e2-121">Protocol specifications</span></span>

<span data-ttu-id="137e2-122">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="137e2-122">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="137e2-123">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="137e2-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="137e2-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="137e2-124">Header files</span></span>

<span data-ttu-id="137e2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="137e2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="137e2-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="137e2-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="137e2-127">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="137e2-127">mapitags.h</span></span>
  
> <span data-ttu-id="137e2-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="137e2-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="137e2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="137e2-129">See also</span></span>



[<span data-ttu-id="137e2-130">PidTagMessageSize (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="137e2-130">PidTagMessageSize Canonical Property</span></span>](pidtagmessagesize-canonical-property.md)


[<span data-ttu-id="137e2-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="137e2-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="137e2-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="137e2-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="137e2-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="137e2-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="137e2-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="137e2-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

