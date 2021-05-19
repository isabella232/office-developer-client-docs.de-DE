---
title: PidTagIcon (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIcon
api_type:
- HeaderDef
ms.assetid: 815dabf3-3cac-40e1-b6ff-51db2ff5096a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ad8d6934b5e57429de5039e9420742caa9dd4294
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356728"
---
# <a name="pidtagicon-canonical-property"></a><span data-ttu-id="b5378-103">PidTagIcon (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b5378-103">PidTagIcon Canonical Property</span></span>

  
  
<span data-ttu-id="b5378-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5378-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5378-105">Enthält eine Bitmap eines Vollformatsymbols für ein Formular.</span><span class="sxs-lookup"><span data-stu-id="b5378-105">Contains a bitmap of a full size icon for a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b5378-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b5378-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5378-107">PR_ICON</span><span class="sxs-lookup"><span data-stu-id="b5378-107">PR_ICON</span></span>  <br/> |
|<span data-ttu-id="b5378-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b5378-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5378-109">0x0FFD</span><span class="sxs-lookup"><span data-stu-id="b5378-109">0x0FFD</span></span>  <br/> |
|<span data-ttu-id="b5378-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b5378-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5378-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b5378-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b5378-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b5378-112">Area:</span></span>  <br/> |<span data-ttu-id="b5378-113">MAPI nicht durchlässig</span><span class="sxs-lookup"><span data-stu-id="b5378-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5378-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5378-114">Remarks</span></span>

<span data-ttu-id="b5378-115">Diese Eigenschaft enthält ein 32-× 32-Pixel-Bild eines Symbols, das mit dem Inhalt eines identisch ist. ICO-Datei.</span><span class="sxs-lookup"><span data-stu-id="b5378-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file.</span></span> <span data-ttu-id="b5378-116">Diese Eigenschaft wird normalerweise aus der kopiert. ICO-Datei, die in der Zeile LargeIcon des entsprechenden Abschnitts [Beschreibung] der Formularkonfigurationsdatei angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b5378-116">This property is normally copied from the .ICO file specified in the LargeIcon line of the appropriate [Description] section of the form configuration file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b5378-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b5378-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b5378-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b5378-118">Protocol specifications</span></span>

<span data-ttu-id="b5378-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5378-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5378-120">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b5378-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b5378-121">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b5378-121">Header files</span></span>

<span data-ttu-id="b5378-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5378-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5378-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b5378-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5378-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b5378-124">Mapitags.h</span></span>
  
> <span data-ttu-id="b5378-125">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b5378-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5378-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5378-126">See also</span></span>



[<span data-ttu-id="b5378-127">PidTagMiniIcon (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b5378-127">PidTagMiniIcon Canonical Property</span></span>](pidtagminiicon-canonical-property.md)


[<span data-ttu-id="b5378-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5378-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5378-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b5378-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5378-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b5378-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5378-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b5378-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

