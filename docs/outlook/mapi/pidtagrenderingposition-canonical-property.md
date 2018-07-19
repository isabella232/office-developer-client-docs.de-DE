---
title: PidTagRenderingPosition (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aa149a81102a4981712ea3ca897d8b1ad448a1eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794955"
---
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="c0b2e-103">PidTagRenderingPosition (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c0b2e-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="c0b2e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0b2e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0b2e-105">Enthält einen Offset in Zeichen, die beim Rendern einer Anlage im Hauptfenster Nachrichtentext verwenden.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0b2e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c0b2e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c0b2e-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="c0b2e-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="c0b2e-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="c0b2e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c0b2e-109">0x370B</span><span class="sxs-lookup"><span data-stu-id="c0b2e-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="c0b2e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c0b2e-110">Data type:</span></span>  <br/> |<span data-ttu-id="c0b2e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c0b2e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c0b2e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c0b2e-112">Area:</span></span>  <br/> |<span data-ttu-id="c0b2e-113">MAPI-Anlage</span><span class="sxs-lookup"><span data-stu-id="c0b2e-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0b2e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0b2e-114">Remarks</span></span>

<span data-ttu-id="c0b2e-115">Wenn der angegebene Offset-1 (0xFFFFFFFF) ist, wird die Anlage unter Verwendung dieser Eigenschaft nicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="c0b2e-116">Alle Werte, die als-1 Geben Sie an der Position innerhalb der **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft, an der die Anlage ist gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="c0b2e-117">**Hinweis** Die von dieser Eigenschaft in **PR_BODY** angegebene Zeichen wird durch die Anlage ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="c0b2e-118">In der Regel ist dieses Zeichen ein Leerzeichen, obwohl eine spezielle Platzhalterzeichen auch verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="c0b2e-119">Diese Eigenschaft wird in Zeichen angegeben.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-119">This property is expressed in characters.</span></span> <span data-ttu-id="c0b2e-120">In einigen Zeichensätzen entspricht dies nicht Bytes.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="c0b2e-121">Unicode-Anwendungen können die Position, basierend auf 2-Byte-Zeichen berechnen.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="c0b2e-122">Double-Byte-Zeichen (DBCS) Applications müssen den Text bis zum den Wert Eigenschaft überprüft den Ordner, da deren Darstellung von Zeichen zwischen ein oder zwei Bytes pro Zeichen variiert.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="c0b2e-123">Diese Eigenschaft sollte nicht mit Rich Text Format (RTF) Text verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="c0b2e-124">Die Renderingposition wird durch Escapesequenz aufgerufen, den Platzhalter Objekt Anlage im RTF angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="c0b2e-125">In den folgenden Schritten die Zeichenfolge besteht aus `\objattph` gefolgt von einem einzelnen Zeichen, normalerweise ein Leerzeichen, die durch das Rendering Anlage ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c0b2e-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c0b2e-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c0b2e-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c0b2e-127">Protocol specifications</span></span>

<span data-ttu-id="c0b2e-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0b2e-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0b2e-129">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c0b2e-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0b2e-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0b2e-131">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c0b2e-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c0b2e-132">Header files</span></span>

<span data-ttu-id="c0b2e-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0b2e-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="c0b2e-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="c0b2e-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c0b2e-135">Mapitags.h</span></span>
  
> <span data-ttu-id="c0b2e-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c0b2e-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0b2e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0b2e-137">See also</span></span>



[<span data-ttu-id="c0b2e-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0b2e-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c0b2e-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0b2e-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c0b2e-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c0b2e-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c0b2e-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c0b2e-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

