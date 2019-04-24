---
title: Kanonische Pidtagattachsize (-Eigenschaft
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
ms.openlocfilehash: f3e4f19ab43a3da7c4840d762d5131813c83d996
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361089"
---
# <a name="pidtagattachsize-canonical-property"></a><span data-ttu-id="252dd-103">Kanonische Pidtagattachsize (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="252dd-103">PidTagAttachSize Canonical Property</span></span>

  
  
<span data-ttu-id="252dd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="252dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="252dd-105">Enthält die Summe der Größen aller Eigenschaften einer Anlage in Byte.</span><span class="sxs-lookup"><span data-stu-id="252dd-105">Contains the sum, in bytes, of the sizes of all properties on an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="252dd-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="252dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="252dd-107">PR_ATTACH_SIZE</span><span class="sxs-lookup"><span data-stu-id="252dd-107">PR_ATTACH_SIZE</span></span>  <br/> |
|<span data-ttu-id="252dd-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="252dd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="252dd-109">0x0E20</span><span class="sxs-lookup"><span data-stu-id="252dd-109">0x0E20</span></span>  <br/> |
|<span data-ttu-id="252dd-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="252dd-110">Data type:</span></span>  <br/> |<span data-ttu-id="252dd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="252dd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="252dd-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="252dd-112">Area:</span></span>  <br/> |<span data-ttu-id="252dd-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="252dd-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="252dd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="252dd-114">Remarks</span></span>

<span data-ttu-id="252dd-115">Es wird empfohlen, dass Attachment-unter Objekte die **PR_ATTACH_SIZE** -Eigenschaft verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="252dd-115">It is recommended that attachment subobjects expose the **PR_ATTACH_SIZE** property.</span></span> <span data-ttu-id="252dd-116">Die in **PR_ATTACH_SIZE** enthaltene Summe enthält die Größe der **PR_ATTACH_DATA_BIN** ([pidtagattachdatabinary (](pidtagattachdatabinary-canonical-property.md)) oder **PR_ATTACH_DATA_OBJ** ([pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="252dd-116">The sum contained in **PR_ATTACH_SIZE** includes the size of the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> <span data-ttu-id="252dd-117">Dementsprechend ist **PR_ATTACH_SIZE** in der Regel größer als der Inhalt der Anlage allein.</span><span class="sxs-lookup"><span data-stu-id="252dd-117">Accordingly, **PR_ATTACH_SIZE** is usually larger than the contents of the attachment alone.</span></span> 
  
<span data-ttu-id="252dd-118">Diese Eigenschaft kann verwendet werden, um die ungefähre Größe der Anlage zu überprüfen, bevor eine Remoteübertragung per Modem durchgeführt wird und Status anzeigen beim Speichern der Anlage auf dem Datenträger angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="252dd-118">This property can be used to check the approximate size of the attachment before performing a remote transfer by modem and to display progress indicators when saving the attachment to disk.</span></span> <span data-ttu-id="252dd-119">Sie ist besonders nützlich bei angefügten OLE-Objekten.</span><span class="sxs-lookup"><span data-stu-id="252dd-119">It is particularly useful with attached OLE objects.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="252dd-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="252dd-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="252dd-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="252dd-121">Protocol specifications</span></span>

<span data-ttu-id="252dd-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="252dd-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="252dd-123">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="252dd-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="252dd-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="252dd-124">Header files</span></span>

<span data-ttu-id="252dd-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="252dd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="252dd-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="252dd-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="252dd-127">mapitags. h</span><span class="sxs-lookup"><span data-stu-id="252dd-127">mapitags.h</span></span>
  
> <span data-ttu-id="252dd-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="252dd-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="252dd-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="252dd-129">See also</span></span>



[<span data-ttu-id="252dd-130">Kanonische Pidtagmessagesize (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="252dd-130">PidTagMessageSize Canonical Property</span></span>](pidtagmessagesize-canonical-property.md)


[<span data-ttu-id="252dd-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="252dd-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="252dd-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="252dd-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="252dd-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="252dd-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="252dd-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="252dd-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

