---
title: PidTagMiniIcon (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405415"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="8f71d-103">PidTagMiniIcon (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8f71d-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="8f71d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f71d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f71d-105">Enthält eine Bitmap eines Halbformatsymbols für ein Formular.</span><span class="sxs-lookup"><span data-stu-id="8f71d-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8f71d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8f71d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f71d-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="8f71d-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="8f71d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8f71d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8f71d-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="8f71d-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="8f71d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8f71d-110">Data type:</span></span>  <br/> |<span data-ttu-id="8f71d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8f71d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8f71d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8f71d-112">Area:</span></span>  <br/> |<span data-ttu-id="8f71d-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="8f71d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f71d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8f71d-114">Remarks</span></span>

<span data-ttu-id="8f71d-115">Diese Eigenschaft enthält ein 32-× 32-Pixel-Bild eines Symbols, das mit dem Inhalt eines identisch ist. ICO-Datei, aber nur die obere linke 16 × 16 Pixel werden als signifikant betrachtet.</span><span class="sxs-lookup"><span data-stu-id="8f71d-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="8f71d-116">Diese Eigenschaft wird normalerweise aus der kopiert. ICO-Datei, die in der SmallIcon-Zeile des entsprechenden Abschnitts [Beschreibung] der Formularkonfigurationsdatei angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8f71d-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="8f71d-117">**Hinweis** Einige Plattformen unterstützen keine Symbole mit 16 × 16 Pixeln.</span><span class="sxs-lookup"><span data-stu-id="8f71d-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="8f71d-118">Das 32-× 32-Format dieser Eigenschaft ist in einem solchen Fall verwendbar, clientanwendungen sollten jedoch Anzeigeinkonsistenzen beachten.</span><span class="sxs-lookup"><span data-stu-id="8f71d-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8f71d-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8f71d-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8f71d-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="8f71d-120">Header files</span></span>

<span data-ttu-id="8f71d-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8f71d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f71d-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8f71d-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="8f71d-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8f71d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="8f71d-124">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8f71d-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f71d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f71d-125">See also</span></span>



[<span data-ttu-id="8f71d-126">PidTagIcon (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8f71d-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="8f71d-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f71d-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f71d-128">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="8f71d-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f71d-129">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8f71d-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f71d-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8f71d-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

