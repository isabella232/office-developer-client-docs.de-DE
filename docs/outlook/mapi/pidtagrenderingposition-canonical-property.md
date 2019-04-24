---
title: Kanonische Pidtagrenderingposition (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRenderingPosition
api_type:
- COM
ms.assetid: bce46687-17dc-4a3f-96be-303d8755158e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d463be4a14ecf478bdcbddc50b4ad9360829befc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355153"
---
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="c6439-103">Kanonische Pidtagrenderingposition (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c6439-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="c6439-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6439-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6439-105">Enthält einen Offset in Zeichen, der beim Rendern einer Anlage im Hauptnachrichtentext verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6439-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c6439-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c6439-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c6439-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="c6439-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="c6439-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c6439-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c6439-109">0x370B</span><span class="sxs-lookup"><span data-stu-id="c6439-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="c6439-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c6439-110">Data type:</span></span>  <br/> |<span data-ttu-id="c6439-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c6439-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c6439-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c6439-112">Area:</span></span>  <br/> |<span data-ttu-id="c6439-113">MAPI-Anlage</span><span class="sxs-lookup"><span data-stu-id="c6439-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6439-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6439-114">Remarks</span></span>

<span data-ttu-id="c6439-115">Wenn der angegebene Offset-1 (0xFFFFFFFF) ist, wird die Anlage nicht mithilfe dieser Eigenschaft gerendert.</span><span class="sxs-lookup"><span data-stu-id="c6439-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="c6439-116">Alle anderen Werte als-1 geben die Position in der **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft an, in der die Anlage gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6439-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="c6439-117">**Hinweis** Das von dieser Eigenschaft in **PR_BODY** angegebene Zeichen wird durch die Anlage ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c6439-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="c6439-118">In der Regel handelt es sich um ein Leerzeichen, auch wenn ein besonderes Platzhalterzeichen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c6439-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="c6439-119">Diese Eigenschaft wird in Zeichen ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="c6439-119">This property is expressed in characters.</span></span> <span data-ttu-id="c6439-120">In einigen Zeichensätzen ist dies nicht gleichbedeutend mit Bytes.</span><span class="sxs-lookup"><span data-stu-id="c6439-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="c6439-121">Unicode-Anwendungen können die Position anhand von zwei-Byte-Zeichen berechnen.</span><span class="sxs-lookup"><span data-stu-id="c6439-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="c6439-122">DBCS-Anwendungen (Double-Byte Character Set) müssen den Text bis zu diesem Eigenschaftswert überprüfen, da ihre Zeichendarstellung zwischen 1 und 2 Byte pro Zeichen variiert.</span><span class="sxs-lookup"><span data-stu-id="c6439-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="c6439-123">Diese Eigenschaft sollte nicht mit RTF-Text (Rich Text Format) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6439-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="c6439-124">Die Wiedergabeposition wird in RTF durch eine Escape-Sequenz mit dem Namen Object Attachment PlaceHolder angegeben.</span><span class="sxs-lookup"><span data-stu-id="c6439-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="c6439-125">Diese Sequenz besteht aus der Zeichen `\objattph` Folge, gefolgt von einem einzelnen Zeichen, normalerweise einem Leerraum, der durch das Anlagen Rendering ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c6439-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c6439-126">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c6439-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c6439-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c6439-127">Protocol specifications</span></span>

<span data-ttu-id="c6439-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6439-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6439-129">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c6439-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c6439-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6439-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6439-131">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="c6439-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c6439-132">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="c6439-132">Header files</span></span>

<span data-ttu-id="c6439-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c6439-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="c6439-134">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="c6439-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="c6439-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c6439-135">Mapitags.h</span></span>
  
> <span data-ttu-id="c6439-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c6439-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6439-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6439-137">See also</span></span>



[<span data-ttu-id="c6439-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6439-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c6439-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6439-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c6439-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c6439-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c6439-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c6439-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

