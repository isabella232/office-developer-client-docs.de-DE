---
title: PropertyDefinition Stream-Beispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d0c337bd3e5a73bbbcbb72a109320cfb84efd50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795329"
---
# <a name="propertydefinition-stream-sample"></a><span data-ttu-id="af207-103">PropertyDefinition Stream-Beispiel</span><span class="sxs-lookup"><span data-stu-id="af207-103">PropertyDefinition stream sample</span></span>

<span data-ttu-id="af207-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="af207-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="af207-105">In diesem Thema wird ein Beispiel eines PropertyDefinition Stream-Objekts.</span><span class="sxs-lookup"><span data-stu-id="af207-105">This topic describes an example of a PropertyDefinition stream.</span></span> <span data-ttu-id="af207-106">Das Stream-Objekt enthält eine Definition eines benutzerdefinierten Felds `TextField1`.</span><span class="sxs-lookup"><span data-stu-id="af207-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="af207-107">Der **Text**ist, und die Definition im Format PropDefV2 ist.</span><span class="sxs-lookup"><span data-stu-id="af207-107">The type is **Text**, and the definition is in the PropDefV2 format.</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="af207-108">Daten dump</span><span class="sxs-lookup"><span data-stu-id="af207-108">Data dump</span></span>

<span data-ttu-id="af207-109">Im folgenden finden ein Abbild der Daten des Stream-Objekts, wie er in einem binären-Editor angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af207-109">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="af207-110">Stream-offset</span><span class="sxs-lookup"><span data-stu-id="af207-110">Stream offset</span></span>|<span data-ttu-id="af207-111">Datenbytes</span><span class="sxs-lookup"><span data-stu-id="af207-111">Data bytes</span></span>|<span data-ttu-id="af207-112">ASCII-Daten</span><span class="sxs-lookup"><span data-stu-id="af207-112">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
<span data-ttu-id="af207-113">Es folgt eine Analyse der Beispieldaten für den Datenstrom PropertyDefinition:</span><span class="sxs-lookup"><span data-stu-id="af207-113">The following is a parse of the sample data for the PropertyDefinition stream:</span></span>
  
- <span data-ttu-id="af207-114">Version: Offset 0 x 0, 2 Bytes: 0x0103 (PropDefV2).</span><span class="sxs-lookup"><span data-stu-id="af207-114">Version: Offset 0x0, 2 bytes: 0x0103 (PropDefV2).</span></span>
    
- <span data-ttu-id="af207-115">FieldDefinitionCount: Offset 0 x 2, 4 Bytes: 0 x 1 (1).</span><span class="sxs-lookup"><span data-stu-id="af207-115">FieldDefinitionCount: Offset 0x2, 4 bytes: 0x1 (1).</span></span>
    
- <span data-ttu-id="af207-116">FieldDefinitions: Offset 0 x 6, Array 1 FieldDefinition Stream-Objekts.</span><span class="sxs-lookup"><span data-stu-id="af207-116">FieldDefinitions: Offset 0x6, array of 1 FieldDefinition stream.</span></span>
    
  - <span data-ttu-id="af207-117">Flags: Offset 0, 4 Bytes x 6: 0 x 45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).</span><span class="sxs-lookup"><span data-stu-id="af207-117">Flags: Offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF).</span></span>
    
  - <span data-ttu-id="af207-118">VT: Offset 0xA 2 Bytes: 0 x 8 (**VT_BSTR**).</span><span class="sxs-lookup"><span data-stu-id="af207-118">VT: Offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span></span>
    
  - <span data-ttu-id="af207-119">DispId: Offset 0xC 4 Bytes: 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="af207-119">DispId: Offset 0xC, 4 bytes: 0x0 (0).</span></span>
    
  - <span data-ttu-id="af207-120">NmidNameLength: Offset 0 x 10, 2 Bytes: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="af207-120">NmidNameLength: Offset 0x10, 2 bytes: 0xA (10).</span></span>
    
  - <span data-ttu-id="af207-121">NmidName: Offset 0 x 12, Array von 10 WCHARs so lang wie.</span><span class="sxs-lookup"><span data-stu-id="af207-121">NmidName: Offset 0x12, array of 10 WCHARs.</span></span> <span data-ttu-id="af207-122">Unicode-Zeichenfolgenwert: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="af207-122">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="af207-123">NameANSI: Offset 0 x 26, PackedAnsiString-Stream.</span><span class="sxs-lookup"><span data-stu-id="af207-123">NameANSI: Offset 0x26, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="af207-124">Länge: Offset 0 x 26, 1 Byte: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="af207-124">Length: Offset 0x26, 1 byte: 0xA (10).</span></span>
      
    - <span data-ttu-id="af207-125">Zeichen: Offset 0 x 27, Array von 10 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="af207-125">Characters: Offset 0x27, array of 10 CHARs.</span></span> <span data-ttu-id="af207-126">ANSI-String-Wert: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="af207-126">ANSI string value: "TextField1".</span></span>
    
  - <span data-ttu-id="af207-127">FormulaANSI: Offset 0x31, PackedAnsiString-Stream.</span><span class="sxs-lookup"><span data-stu-id="af207-127">FormulaANSI: Offset 0x31, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="af207-128">Länge: Offset 0x31, 1 Byte: 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="af207-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="af207-129">Zeichen: Offset 0 x 32, Array von 0 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="af207-129">Characters: Offset 0x32, array of 0 CHARs.</span></span> <span data-ttu-id="af207-130">Leere ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="af207-130">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="af207-131">ValidationRuleANSI: Offset 0 x 32, PackedAnsiString-Stream.</span><span class="sxs-lookup"><span data-stu-id="af207-131">ValidationRuleANSI: Offset 0x32, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="af207-132">Länge: Offset 0 x 32, 1 Byte: 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="af207-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="af207-133">Zeichen: Offset 0 x 33, Array von 0 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="af207-133">Characters: Offset 0x33, array of 0 CHARs.</span></span> <span data-ttu-id="af207-134">Leere ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="af207-134">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="af207-135">ValidationTextANSI: Offset 0 x 33, PackedAnsiString-Stream.</span><span class="sxs-lookup"><span data-stu-id="af207-135">ValidationTextANSI: Offset 0x33, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="af207-136">Länge: Offset 0 x 33, 1 Byte: 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="af207-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="af207-137">Zeichen: Offset 0 x 34, 0 char-Array.</span><span class="sxs-lookup"><span data-stu-id="af207-137">Characters: Offset 0x34, array of 0 CHARs.</span></span> <span data-ttu-id="af207-138">Leere ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="af207-138">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="af207-139">ErrorANSI: Offset 0 x 34, PackedAnsiString-Stream.</span><span class="sxs-lookup"><span data-stu-id="af207-139">ErrorANSI: Offset 0x34, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="af207-140">Länge: Offset 0 x 34, 1 Byte: 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="af207-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="af207-141">Zeichen: Offset 0x35 Array von 0 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="af207-141">Characters: Offset 0x35, array of 0 CHARs.</span></span> <span data-ttu-id="af207-142">Leere ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="af207-142">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="af207-143">InternalType: Offset 0x35 4 Bytes: 0 x 0 (iTypeString).</span><span class="sxs-lookup"><span data-stu-id="af207-143">InternalType: Offset 0x35, 4 bytes: 0x0 (iTypeString).</span></span>
    
  - <span data-ttu-id="af207-144">SkipBlocks: Offset 0 x 39, Serie SkipBlock Datenströme.</span><span class="sxs-lookup"><span data-stu-id="af207-144">SkipBlocks: Offset 0x39, series of SkipBlock streams.</span></span>
    
  - <span data-ttu-id="af207-145">Erste SkipBlock</span><span class="sxs-lookup"><span data-stu-id="af207-145">First SkipBlock</span></span>
    
    - <span data-ttu-id="af207-146">Größe: Offset 0, 4 Bytes x 39: 0x15 (21).</span><span class="sxs-lookup"><span data-stu-id="af207-146">Size: Offset 0x39, 4 bytes: 0x15 (21).</span></span>
      
    - <span data-ttu-id="af207-147">Inhalt: Offset 0x3D 21 Bytearray.</span><span class="sxs-lookup"><span data-stu-id="af207-147">Content: Offset 0x3D, array of 21 bytes.</span></span> <span data-ttu-id="af207-148">Dies ist der erste SkipBlock Datenstrom dieses Array einen FirstSkipBlockContent Stream enthält.</span><span class="sxs-lookup"><span data-stu-id="af207-148">This is the first SkipBlock stream, so this array contains a FirstSkipBlockContent stream.</span></span>
      
      - <span data-ttu-id="af207-149">FieldName: Offset 0x3D, PackedUnicodeString-Stream.</span><span class="sxs-lookup"><span data-stu-id="af207-149">FieldName: Offset 0x3D, PackedUnicodeString stream.</span></span>
        
        - <span data-ttu-id="af207-150">Länge: Offset 0x3D, 1 Byte: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="af207-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span></span>
          
        - <span data-ttu-id="af207-151">Zeichen: Offset 0x3E Array von 10 WCHARs so lang wie.</span><span class="sxs-lookup"><span data-stu-id="af207-151">Characters: Offset 0x3E, array of 10 WCHARs.</span></span> <span data-ttu-id="af207-152">Unicode-Zeichenfolgenwert: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="af207-152">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="af207-153">Zweite SkipBlock</span><span class="sxs-lookup"><span data-stu-id="af207-153">Second SkipBlock</span></span>
    
    - <span data-ttu-id="af207-154">Größe: Offset 0, 4 Bytes x 52: 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="af207-154">Size: Offset 0x52, 4 bytes: 0x0 (0).</span></span> <span data-ttu-id="af207-155">Dies ist der abschließende SkipBlock-Stream.</span><span class="sxs-lookup"><span data-stu-id="af207-155">This is the terminating SkipBlock stream.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af207-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af207-156">See also</span></span>

- [<span data-ttu-id="af207-157">Elemente und Felder in Outlook</span><span class="sxs-lookup"><span data-stu-id="af207-157">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="af207-158">Streamstrukturen</span><span class="sxs-lookup"><span data-stu-id="af207-158">Stream Structures</span></span>](stream-structures.md)
- [<span data-ttu-id="af207-159">PropertyDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="af207-159">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="af207-160">FieldDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="af207-160">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="af207-161">SkipBlock-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="af207-161">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="af207-162">FirstSkipBlockContent-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="af207-162">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="af207-163">PackedAnsiString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="af207-163">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="af207-164">PackedUnicodeString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="af207-164">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

