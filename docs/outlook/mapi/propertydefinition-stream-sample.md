---
title: PropertyDefinition-Stream-Beispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 63a8141221c0ff7a8c6ffee20587b682386f87b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406661"
---
# <a name="propertydefinition-stream-sample"></a><span data-ttu-id="da7f6-103">PropertyDefinition-Stream-Beispiel</span><span class="sxs-lookup"><span data-stu-id="da7f6-103">PropertyDefinition stream sample</span></span>

<span data-ttu-id="da7f6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da7f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da7f6-105">In diesem Thema wird ein Beispiel für einen PropertyDefinition-Stream beschrieben.</span><span class="sxs-lookup"><span data-stu-id="da7f6-105">This topic describes an example of a PropertyDefinition stream.</span></span> <span data-ttu-id="da7f6-106">Der Stream enthält eine Definition eines benutzerdefinierten Felds `TextField1`.</span><span class="sxs-lookup"><span data-stu-id="da7f6-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="da7f6-107">Der Typ ist **Text**, und die Definition befindet sich im PropDefV2-Format.</span><span class="sxs-lookup"><span data-stu-id="da7f6-107">The type is **Text**, and the definition is in the PropDefV2 format.</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="da7f6-108">Daten Dump</span><span class="sxs-lookup"><span data-stu-id="da7f6-108">Data dump</span></span>

<span data-ttu-id="da7f6-109">Es folgt ein Daten Dump des Streams, wie er in einem binären Editor angezeigt würde.</span><span class="sxs-lookup"><span data-stu-id="da7f6-109">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="da7f6-110">Datenstrom Offset</span><span class="sxs-lookup"><span data-stu-id="da7f6-110">Stream offset</span></span>|<span data-ttu-id="da7f6-111">Datenbytes</span><span class="sxs-lookup"><span data-stu-id="da7f6-111">Data bytes</span></span>|<span data-ttu-id="da7f6-112">ASCII-Daten</span><span class="sxs-lookup"><span data-stu-id="da7f6-112">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
<span data-ttu-id="da7f6-113">Es folgt eine Analyse der Beispieldaten für den PropertyDefinition-Stream:</span><span class="sxs-lookup"><span data-stu-id="da7f6-113">The following is a parse of the sample data for the PropertyDefinition stream:</span></span>
  
- <span data-ttu-id="da7f6-114">Version: Offset 0x0 festlegen, 2 Bytes: 0x0103 (PropDefV2).</span><span class="sxs-lookup"><span data-stu-id="da7f6-114">Version: Offset 0x0, 2 bytes: 0x0103 (PropDefV2).</span></span>
    
- <span data-ttu-id="da7f6-115">FieldDefinitionCount: Offset 0x2, 4 Bytes: 0x1 (1).</span><span class="sxs-lookup"><span data-stu-id="da7f6-115">FieldDefinitionCount: Offset 0x2, 4 bytes: 0x1 (1).</span></span>
    
- <span data-ttu-id="da7f6-116">FieldDefinitions: Offset 0x6, Array of 1 FieldDefinition streamstruktur Stream.</span><span class="sxs-lookup"><span data-stu-id="da7f6-116">FieldDefinitions: Offset 0x6, array of 1 FieldDefinition stream.</span></span>
    
  - <span data-ttu-id="da7f6-117">Flags: Offset 0x6 bytes: 0x45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).</span><span class="sxs-lookup"><span data-stu-id="da7f6-117">Flags: Offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF).</span></span>
    
  - <span data-ttu-id="da7f6-118">VT: Offset 0xA, 2 Bytes: 0x8 (**VT_BSTR**).</span><span class="sxs-lookup"><span data-stu-id="da7f6-118">VT: Offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span></span>
    
  - <span data-ttu-id="da7f6-119">DispId: Offset 0xC bytes: 0x0 festlegen (0).</span><span class="sxs-lookup"><span data-stu-id="da7f6-119">DispId: Offset 0xC, 4 bytes: 0x0 (0).</span></span>
    
  - <span data-ttu-id="da7f6-120">NmidNameLength: Offset 0x10, 2 Bytes: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="da7f6-120">NmidNameLength: Offset 0x10, 2 bytes: 0xA (10).</span></span>
    
  - <span data-ttu-id="da7f6-121">NmidName: Offset 0x12, Array von 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="da7f6-121">NmidName: Offset 0x12, array of 10 WCHARs.</span></span> <span data-ttu-id="da7f6-122">Unicode-Zeichenfolgenwert: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="da7f6-122">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="da7f6-123">NameANSI: Offset 0x26, Packedansistring streamstruktur-Stream.</span><span class="sxs-lookup"><span data-stu-id="da7f6-123">NameANSI: Offset 0x26, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="da7f6-124">Length: Offset 0x26, 1 Byte: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="da7f6-124">Length: Offset 0x26, 1 byte: 0xA (10).</span></span>
      
    - <span data-ttu-id="da7f6-125">Characters: Offset 0x27, Array of 10 CHARs.</span><span class="sxs-lookup"><span data-stu-id="da7f6-125">Characters: Offset 0x27, array of 10 CHARs.</span></span> <span data-ttu-id="da7f6-126">ANSI-Zeichenfolgenwert: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="da7f6-126">ANSI string value: "TextField1".</span></span>
    
  - <span data-ttu-id="da7f6-127">FormulaANSI: Offset 0x31, Packedansistring streamstruktur-Stream.</span><span class="sxs-lookup"><span data-stu-id="da7f6-127">FormulaANSI: Offset 0x31, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="da7f6-128">Length: Offset 0x31, 1 Byte: 0x0 festlegen (0).</span><span class="sxs-lookup"><span data-stu-id="da7f6-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="da7f6-129">Characters: Offset 0x32, Array of 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="da7f6-129">Characters: Offset 0x32, array of 0 CHARs.</span></span> <span data-ttu-id="da7f6-130">Leere ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="da7f6-130">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="da7f6-131">ValidationRuleANSI: Offset 0x32, Packedansistring streamstruktur-Stream.</span><span class="sxs-lookup"><span data-stu-id="da7f6-131">ValidationRuleANSI: Offset 0x32, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="da7f6-132">Length: Offset 0x32, 1 Byte: 0x0 festlegen (0).</span><span class="sxs-lookup"><span data-stu-id="da7f6-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="da7f6-133">Characters: Offset 0x33, Array of 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="da7f6-133">Characters: Offset 0x33, array of 0 CHARs.</span></span> <span data-ttu-id="da7f6-134">Leere ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="da7f6-134">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="da7f6-135">ValidationTextANSI: Offset 0x33, Packedansistring streamstruktur-Stream.</span><span class="sxs-lookup"><span data-stu-id="da7f6-135">ValidationTextANSI: Offset 0x33, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="da7f6-136">Length: Offset 0x33, 1 Byte: 0x0 festlegen (0).</span><span class="sxs-lookup"><span data-stu-id="da7f6-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="da7f6-137">Characters: Offset 0x34, Array of 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="da7f6-137">Characters: Offset 0x34, array of 0 CHARs.</span></span> <span data-ttu-id="da7f6-138">Leere ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="da7f6-138">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="da7f6-139">ErrorANSI: Offset 0x34, Packedansistring streamstruktur-Stream.</span><span class="sxs-lookup"><span data-stu-id="da7f6-139">ErrorANSI: Offset 0x34, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="da7f6-140">Length: Offset 0x34, 1 Byte: 0x0 festlegen (0).</span><span class="sxs-lookup"><span data-stu-id="da7f6-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="da7f6-141">Characters: Offset 0x35, Array of 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="da7f6-141">Characters: Offset 0x35, array of 0 CHARs.</span></span> <span data-ttu-id="da7f6-142">Leere ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="da7f6-142">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="da7f6-143">Internaltype: Offset 0x35 bytes: 0x0 festlegen (iTypeString).</span><span class="sxs-lookup"><span data-stu-id="da7f6-143">InternalType: Offset 0x35, 4 bytes: 0x0 (iTypeString).</span></span>
    
  - <span data-ttu-id="da7f6-144">SkipBlocks: Offset-0x39, Reihe von SkipBlock streamstruktur-Streams.</span><span class="sxs-lookup"><span data-stu-id="da7f6-144">SkipBlocks: Offset 0x39, series of SkipBlock streams.</span></span>
    
  - <span data-ttu-id="da7f6-145">Erster SkipBlock streamstruktur</span><span class="sxs-lookup"><span data-stu-id="da7f6-145">First SkipBlock</span></span>
    
    - <span data-ttu-id="da7f6-146">Größe: Offset 0x39 bytes: 0x15 (21).</span><span class="sxs-lookup"><span data-stu-id="da7f6-146">Size: Offset 0x39, 4 bytes: 0x15 (21).</span></span>
      
    - <span data-ttu-id="da7f6-147">Inhalt: Offset 0x3D, Array mit 21 bytes.</span><span class="sxs-lookup"><span data-stu-id="da7f6-147">Content: Offset 0x3D, array of 21 bytes.</span></span> <span data-ttu-id="da7f6-148">Dies ist der erste SkipBlock streamstruktur-Datenstrom, daher enthält dieses Array einen Firstskipblockcontent streamstruktur-Stream.</span><span class="sxs-lookup"><span data-stu-id="da7f6-148">This is the first SkipBlock stream, so this array contains a FirstSkipBlockContent stream.</span></span>
      
      - <span data-ttu-id="da7f6-149">FieldName: Offset 0x3D, Packedunicodestring streamstruktur Stream.</span><span class="sxs-lookup"><span data-stu-id="da7f6-149">FieldName: Offset 0x3D, PackedUnicodeString stream.</span></span>
        
        - <span data-ttu-id="da7f6-150">Length: Offset 0x3D, 1 Byte: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="da7f6-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span></span>
          
        - <span data-ttu-id="da7f6-151">Characters: Offset 0x3E, Array of 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="da7f6-151">Characters: Offset 0x3E, array of 10 WCHARs.</span></span> <span data-ttu-id="da7f6-152">Unicode-Zeichenfolgenwert: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="da7f6-152">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="da7f6-153">Zweite SkipBlock streamstruktur</span><span class="sxs-lookup"><span data-stu-id="da7f6-153">Second SkipBlock</span></span>
    
    - <span data-ttu-id="da7f6-154">Größe: Offset 0x52 bytes: 0x0 festlegen (0).</span><span class="sxs-lookup"><span data-stu-id="da7f6-154">Size: Offset 0x52, 4 bytes: 0x0 (0).</span></span> <span data-ttu-id="da7f6-155">Dies ist der abschließende SkipBlock streamstruktur-Stream.</span><span class="sxs-lookup"><span data-stu-id="da7f6-155">This is the terminating SkipBlock stream.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da7f6-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da7f6-156">See also</span></span>

- [<span data-ttu-id="da7f6-157">Outlook-Elemente und-Felder</span><span class="sxs-lookup"><span data-stu-id="da7f6-157">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="da7f6-158">Stream-Strukturen</span><span class="sxs-lookup"><span data-stu-id="da7f6-158">Stream Structures</span></span>](stream-structures.md)
- [<span data-ttu-id="da7f6-159">PropertyDefinition-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="da7f6-159">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="da7f6-160">FieldDefinition streamstruktur-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="da7f6-160">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="da7f6-161">SkipBlock streamstruktur-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="da7f6-161">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="da7f6-162">Firstskipblockcontent streamstruktur-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="da7f6-162">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="da7f6-163">Packedansistring streamstruktur-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="da7f6-163">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="da7f6-164">Packedunicodestring streamstruktur-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="da7f6-164">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

