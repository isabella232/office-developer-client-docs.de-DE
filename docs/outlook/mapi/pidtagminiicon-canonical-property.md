---
title: Kanonische Pidtagminiicon (-Eigenschaft
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
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="4ea45-103">Kanonische Pidtagminiicon (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4ea45-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="4ea45-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ea45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ea45-105">Enthält eine Bitmap mit einem halben Symbol für ein Formular.</span><span class="sxs-lookup"><span data-stu-id="4ea45-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ea45-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4ea45-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ea45-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="4ea45-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="4ea45-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4ea45-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ea45-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="4ea45-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="4ea45-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4ea45-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ea45-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4ea45-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4ea45-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4ea45-112">Area:</span></span>  <br/> |<span data-ttu-id="4ea45-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="4ea45-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ea45-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ea45-114">Remarks</span></span>

<span data-ttu-id="4ea45-115">Diese Eigenschaft enthält ein 32 × 32-Pixel Bild eines Symbols, dasselbe wie der Inhalt von a. ICO-Datei, aber nur die oberen linken 16 × 16 Pixel gelten als signifikant.</span><span class="sxs-lookup"><span data-stu-id="4ea45-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="4ea45-116">Diese Eigenschaft wird normalerweise aus der kopiert. ICO-Datei, die in der SmallIcon-Codezeile im entsprechenden Abschnitt [Description] der Formular Konfigurationsdatei angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4ea45-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="4ea45-117">**Hinweis** Einige Plattformen unterstützen keine 16 × 16-Pixel-Symbole.</span><span class="sxs-lookup"><span data-stu-id="4ea45-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="4ea45-118">Das 32 × 32-Format dieser Eigenschaft kann in einem solchen Fall verwendet werden, die Anzeige Inkonsistenzen sollten jedoch von Clientanwendungen beachtet werden.</span><span class="sxs-lookup"><span data-stu-id="4ea45-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4ea45-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4ea45-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4ea45-120">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="4ea45-120">Header files</span></span>

<span data-ttu-id="4ea45-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4ea45-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ea45-122">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="4ea45-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ea45-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4ea45-123">Mapitags.h</span></span>
  
> <span data-ttu-id="4ea45-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4ea45-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ea45-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ea45-125">See also</span></span>



[<span data-ttu-id="4ea45-126">Kanonische Pidtagicon (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4ea45-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="4ea45-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ea45-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ea45-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ea45-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ea45-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4ea45-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ea45-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4ea45-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

