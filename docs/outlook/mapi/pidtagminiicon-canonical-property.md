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
ms.openlocfilehash: 5514e0553f719e2e875aad7001bb38a6a52e8e08
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589777"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="00745-103">PidTagMiniIcon (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="00745-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="00745-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00745-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00745-105">Eine Bitmap eines Symbols halber Größe für ein Formular enthält.</span><span class="sxs-lookup"><span data-stu-id="00745-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00745-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="00745-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00745-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="00745-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="00745-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="00745-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00745-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="00745-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="00745-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="00745-110">Data type:</span></span>  <br/> |<span data-ttu-id="00745-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="00745-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="00745-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="00745-112">Area:</span></span>  <br/> |<span data-ttu-id="00745-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="00745-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00745-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="00745-114">Remarks</span></span>

<span data-ttu-id="00745-115">Diese Eigenschaft enthält ein Bild mit 32 x 32 Pixeln eines Symbols, identisch mit den Inhalt ein. Gelten erhebliche ICO-Datei, aber nur der oberen linken Ecke 16 x 16 Pixel.</span><span class="sxs-lookup"><span data-stu-id="00745-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="00745-116">Diese Eigenschaft wird normalerweise übernommen aus der. ICO-Datei in der SmallIcon-Zeile der entsprechenden Abschnitt der Konfigurationsdatei Formular [Beschreibung] angegeben.</span><span class="sxs-lookup"><span data-stu-id="00745-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="00745-117">**Hinweis** Einige Plattformen werden nicht unterstützt 16 x 16 Pixel-Symbol.</span><span class="sxs-lookup"><span data-stu-id="00745-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="00745-118">Das Format 32 x 32 dieser Eigenschaft kann in einem solchen Fall verwendet werden, aber Clientanwendungen Beachten der Anzeige Inkonsistenzen.</span><span class="sxs-lookup"><span data-stu-id="00745-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="00745-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="00745-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="00745-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="00745-120">Header files</span></span>

<span data-ttu-id="00745-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00745-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="00745-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="00745-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="00745-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="00745-123">Mapitags.h</span></span>
  
> <span data-ttu-id="00745-124">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="00745-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00745-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00745-125">See also</span></span>



[<span data-ttu-id="00745-126">PidTagIcon (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="00745-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="00745-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00745-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00745-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="00745-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00745-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="00745-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00745-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="00745-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

