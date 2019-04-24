---
title: Kanonische Pidtagicon (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ad8d6934b5e57429de5039e9420742caa9dd4294
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356728"
---
# <a name="pidtagicon-canonical-property"></a><span data-ttu-id="3e1b4-103">Kanonische Pidtagicon (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3e1b4-103">PidTagIcon Canonical Property</span></span>

  
  
<span data-ttu-id="3e1b4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e1b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e1b4-105">Enthält eine Bitmap eines vollständigen Symbols für ein Formular.</span><span class="sxs-lookup"><span data-stu-id="3e1b4-105">Contains a bitmap of a full size icon for a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e1b4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3e1b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3e1b4-107">PR_ICON</span><span class="sxs-lookup"><span data-stu-id="3e1b4-107">PR_ICON</span></span>  <br/> |
|<span data-ttu-id="3e1b4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="3e1b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3e1b4-109">0x0FFD</span><span class="sxs-lookup"><span data-stu-id="3e1b4-109">0x0FFD</span></span>  <br/> |
|<span data-ttu-id="3e1b4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3e1b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="3e1b4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3e1b4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3e1b4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3e1b4-112">Area:</span></span>  <br/> |<span data-ttu-id="3e1b4-113">Nicht transmitable MAPI</span><span class="sxs-lookup"><span data-stu-id="3e1b4-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e1b4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e1b4-114">Remarks</span></span>

<span data-ttu-id="3e1b4-115">Diese Eigenschaft enthält ein 32 × 32-Pixel Bild eines Symbols, dasselbe wie der Inhalt von a. ICO-Datei.</span><span class="sxs-lookup"><span data-stu-id="3e1b4-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file.</span></span> <span data-ttu-id="3e1b4-116">Diese Eigenschaft wird normalerweise aus der kopiert. ICO-Datei, die in der LargeIcon-Codezeile im entsprechenden Abschnitt [Description] der Formular Konfigurationsdatei angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3e1b4-116">This property is normally copied from the .ICO file specified in the LargeIcon line of the appropriate [Description] section of the form configuration file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3e1b4-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3e1b4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3e1b4-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3e1b4-118">Protocol specifications</span></span>

<span data-ttu-id="3e1b4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e1b4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3e1b4-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3e1b4-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3e1b4-121">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="3e1b4-121">Header files</span></span>

<span data-ttu-id="3e1b4-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3e1b4-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="3e1b4-123">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="3e1b4-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="3e1b4-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="3e1b4-124">Mapitags.h</span></span>
  
> <span data-ttu-id="3e1b4-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="3e1b4-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e1b4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e1b4-126">See also</span></span>



[<span data-ttu-id="3e1b4-127">Kanonische Pidtagminiicon (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3e1b4-127">PidTagMiniIcon Canonical Property</span></span>](pidtagminiicon-canonical-property.md)


[<span data-ttu-id="3e1b4-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3e1b4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3e1b4-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3e1b4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3e1b4-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3e1b4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3e1b4-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3e1b4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

