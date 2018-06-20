---
title: Kanonische PidTagMiniIcon-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 04d78bddc7bae27ba23cccf676eb6e7412ffc0db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794629"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="9d2be-103">Kanonische PidTagMiniIcon-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9d2be-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="9d2be-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d2be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d2be-105">Eine Bitmap eines Symbols halber Größe für ein Formular enthält.</span><span class="sxs-lookup"><span data-stu-id="9d2be-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d2be-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9d2be-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d2be-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="9d2be-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="9d2be-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="9d2be-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d2be-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="9d2be-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="9d2be-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9d2be-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d2be-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d2be-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9d2be-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9d2be-112">Area:</span></span>  <br/> |<span data-ttu-id="9d2be-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="9d2be-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d2be-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d2be-114">Remarks</span></span>

<span data-ttu-id="9d2be-115">Diese Eigenschaft enthält ein Bild mit 32 x 32 Pixeln eines Symbols, identisch mit den Inhalt ein. Gelten erhebliche ICO-Datei, aber nur der oberen linken Ecke 16 x 16 Pixel.</span><span class="sxs-lookup"><span data-stu-id="9d2be-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="9d2be-116">Diese Eigenschaft wird normalerweise übernommen aus der. ICO-Datei in der SmallIcon-Zeile der entsprechenden Abschnitt der Konfigurationsdatei Formular [Beschreibung] angegeben.</span><span class="sxs-lookup"><span data-stu-id="9d2be-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="9d2be-117">**Hinweis** Einige Plattformen werden nicht unterstützt 16 x 16 Pixel-Symbol.</span><span class="sxs-lookup"><span data-stu-id="9d2be-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="9d2be-118">Das Format 32 x 32 dieser Eigenschaft kann in einem solchen Fall verwendet werden, aber Clientanwendungen Beachten der Anzeige Inkonsistenzen.</span><span class="sxs-lookup"><span data-stu-id="9d2be-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9d2be-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9d2be-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9d2be-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="9d2be-120">Header files</span></span>

<span data-ttu-id="9d2be-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d2be-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d2be-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9d2be-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d2be-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9d2be-123">Mapitags.h</span></span>
  
> <span data-ttu-id="9d2be-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9d2be-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d2be-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d2be-125">See also</span></span>



[<span data-ttu-id="9d2be-126">Kanonische PidTagIcon-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9d2be-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="9d2be-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d2be-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d2be-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d2be-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d2be-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9d2be-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d2be-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9d2be-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

