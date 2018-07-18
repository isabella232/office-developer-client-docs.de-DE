---
title: FolderUserFields Stream-Beispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 72c71a6109f55f7ec06499e214a1aa11292a9e52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791702"
---
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="a6862-103">FolderUserFields Stream-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a6862-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="a6862-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6862-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6862-105">In diesem Thema wird ein Beispiel eines FolderUserFields Stream-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a6862-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="a6862-106">Das Stream-Objekt enthält eine Definition eines benutzerdefinierten Felds `TextField1`.</span><span class="sxs-lookup"><span data-stu-id="a6862-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="a6862-107">Der **Text**ist, und der Stream FolderUserFields FolderUserFieldsAnsi und FolderUserFieldsUnicode Teile enthält.</span><span class="sxs-lookup"><span data-stu-id="a6862-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="a6862-108">Weitere Informationen finden Sie unter [Ordner Felder Stream Strukturen](folder-fields-stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="a6862-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="a6862-109">Daten dump</span><span class="sxs-lookup"><span data-stu-id="a6862-109">Data dump</span></span>

<span data-ttu-id="a6862-110">Im folgenden finden ein Abbild der Daten des Stream-Objekts, wie er in einem binären-Editor angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6862-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="a6862-111">Stream-offset</span><span class="sxs-lookup"><span data-stu-id="a6862-111">Stream offset</span></span>|<span data-ttu-id="a6862-112">Datenbytes</span><span class="sxs-lookup"><span data-stu-id="a6862-112">Data bytes</span></span>|<span data-ttu-id="a6862-113">ASCII-Daten</span><span class="sxs-lookup"><span data-stu-id="a6862-113">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `02 00 00 00 01 00 00 00 0A 00 54 65 78 74 46 69` <br/> | `..........TextFi` <br/> |
| `0000000010` <br/> | `65 6C 64 31 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `eld1).......A...` <br/> |
| `0000000020` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `0000000030` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000040` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000050` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000060` <br/> | `00 00 00 00 00 00 02 00 00 00 01 00 00 00 0A 00` <br/> | `................` <br/> |
| `0000000070` <br/> | `54 00 65 00 78 00 74 00 46 00 69 00 65 00 6C 00` <br/> | `T.e.x.t.F.i.e.l.` <br/> |
| `0000000080` <br/> | `64 00 31 00 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `d.1.).......A...` <br/> |
| `0000000090` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `00000000A0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000B0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000C0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000D0` <br/> | `00 00 00 00 00 00` <br/> | `......` <br/> |
   

<span data-ttu-id="a6862-114">Es folgt eine Analyse der Beispieldaten für den Datenstrom **FolderUserFields** :</span><span class="sxs-lookup"><span data-stu-id="a6862-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="a6862-115">FolderUserFieldsAnsi: Offset 0 x 0.</span><span class="sxs-lookup"><span data-stu-id="a6862-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="a6862-116">FieldDefinitionCount: Offset 0 x 0, 4 Bytes: 0 x 00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="a6862-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="a6862-117">FieldDefinitions: Offset 0 x 4, Array 2 FolderFieldDefinitionA Datenströme.</span><span class="sxs-lookup"><span data-stu-id="a6862-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="a6862-118">**Erste Arrayelement**:</span><span class="sxs-lookup"><span data-stu-id="a6862-118">**First array element**:</span></span>
    
    - <span data-ttu-id="a6862-119">FieldType: Offset 0, 4 Bytes x 4: 0 x 00000001 (FtString).</span><span class="sxs-lookup"><span data-stu-id="a6862-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="a6862-120">FieldNameLength: Offset 0 x 8, 2 Bytes: 0x000A (10)</span><span class="sxs-lookup"><span data-stu-id="a6862-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="a6862-121">FieldName: Offset 0xA Array von 10 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a6862-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="a6862-122">ANSI-String-Wert: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="a6862-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="a6862-123">Allgemeine: Offset 0 x 14.</span><span class="sxs-lookup"><span data-stu-id="a6862-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="a6862-124">PropSetGuid: Offset 0 x 14, 16 Byte: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="a6862-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="a6862-125">Fcapm: Offset 0 x 24, 4 Bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="a6862-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="a6862-126">DwString: Offset 0, 4 Bytes x 28: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-127">DwBitmap: Offset 0x2C 4 Bytes: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-128">DwDisplay: Offset 0, 4 Bytes x 30: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-129">iFmt: Offset 0 x 34, 4 Bytes: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-130">WszFormulaLength: Offset 0x38 2 Bytes: 0 x 0000 (0).</span><span class="sxs-lookup"><span data-stu-id="a6862-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="a6862-131">WszFormula: Offset 0x3A, Array von 0 WCHARs so lang wie.</span><span class="sxs-lookup"><span data-stu-id="a6862-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="a6862-132">Leerer String-Wert.</span><span class="sxs-lookup"><span data-stu-id="a6862-132">Empty string value.</span></span>
    
    <span data-ttu-id="a6862-133">**Zweite Arrayelement**:</span><span class="sxs-lookup"><span data-stu-id="a6862-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="a6862-134">FieldType: Offset 0x3A 4 Bytes: 0 x 00000000 (FtNone).</span><span class="sxs-lookup"><span data-stu-id="a6862-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="a6862-135">FieldNameLength: Offset 0x3E 2 Bytes: 0 x 0000 (0).</span><span class="sxs-lookup"><span data-stu-id="a6862-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="a6862-136">FieldName: Offset 0 x 40, 0 char-Array.</span><span class="sxs-lookup"><span data-stu-id="a6862-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="a6862-137">Leerer String-Wert.</span><span class="sxs-lookup"><span data-stu-id="a6862-137">Empty string value.</span></span>
      
    - <span data-ttu-id="a6862-138">Allgemeine: Offset 0 x 40.</span><span class="sxs-lookup"><span data-stu-id="a6862-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="a6862-139">PropSetGuid: Offset 0 x 40, 16 Byte: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="a6862-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="a6862-140">Fcapm: Offset 0 x 50, 4 Bytes: 0 x 00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="a6862-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="a6862-141">DwString: Offset 0, 4 Bytes x 54: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-142">DwBitmap: Offset 0x58 4 Bytes: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-143">DwDisplay: Offset 0x5C 4 Bytes: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-144">iFmt: Offset 0 x 60, 4 Bytes: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-145">WszFormulaLength: Offset 0x64 2 Bytes: 0 x 0000 (0).</span><span class="sxs-lookup"><span data-stu-id="a6862-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="a6862-146">WszFormula: Offset 0x66, Array von 0 WCHARs so lang wie.</span><span class="sxs-lookup"><span data-stu-id="a6862-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="a6862-147">Leerer String-Wert.</span><span class="sxs-lookup"><span data-stu-id="a6862-147">Empty string value.</span></span>
    
- <span data-ttu-id="a6862-148">FolderUserFieldsUnicode: Offset 0x66.</span><span class="sxs-lookup"><span data-stu-id="a6862-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="a6862-149">FieldDefinitionCount: Offset 0x66 4 Bytes: 0 x 00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="a6862-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="a6862-150">FieldDefinitions: Offset 0x6A Array 2 FolderFieldDefinitionW Datenströme.</span><span class="sxs-lookup"><span data-stu-id="a6862-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="a6862-151">**Erste Arrayelement**:</span><span class="sxs-lookup"><span data-stu-id="a6862-151">**First array element**:</span></span>
    
    - <span data-ttu-id="a6862-152">FieldType: Offset 0x6A 4 Bytes: 0 x 00000001 (FtString).</span><span class="sxs-lookup"><span data-stu-id="a6862-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="a6862-153">FieldNameLength: Offset 0x6E 2 Bytes: 0x000A (10).</span><span class="sxs-lookup"><span data-stu-id="a6862-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="a6862-154">FieldName: Offset 0x70 Array von 10 WCHARs so lang wie.</span><span class="sxs-lookup"><span data-stu-id="a6862-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="a6862-155">Unicode-Zeichenfolgenwert: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="a6862-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="a6862-156">Allgemeine: Offset 0 x 84.</span><span class="sxs-lookup"><span data-stu-id="a6862-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="a6862-157">PropSetGuid: Offset 0 x 84, 16 Byte: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="a6862-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="a6862-158">Fcapm: Offset 0x94 4 Bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="a6862-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="a6862-159">DwString: Offset 0x98 4 Bytes: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-160">DwBitmap: Offset 0x9C MACHINE_CHECK_EXCEPTION, 4 Bytes: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-161">DwDisplay: Offset 0xA0 4 Bytes: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-162">iFmt: Offset 0xA4 4 Bytes: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-163">WszFormulaLength: Offset 0xA8 2 Bytes: 0 x 0000 (0).</span><span class="sxs-lookup"><span data-stu-id="a6862-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="a6862-164">WszFormula: Offset 0xAA, Array von 0 WCHARs so lang wie.</span><span class="sxs-lookup"><span data-stu-id="a6862-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="a6862-165">Leerer String-Wert.</span><span class="sxs-lookup"><span data-stu-id="a6862-165">Empty string value.</span></span>
    
    <span data-ttu-id="a6862-166">**Zweite Arrayelement**:</span><span class="sxs-lookup"><span data-stu-id="a6862-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="a6862-167">FieldType: Offset 0xAA 4 Bytes: 0 x 00000000 (FtNone).</span><span class="sxs-lookup"><span data-stu-id="a6862-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="a6862-168">FieldNameLength: Offset 0xAE 2 Bytes: 0 x 0000 (0).</span><span class="sxs-lookup"><span data-stu-id="a6862-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="a6862-169">FieldName: Offset 0xB0 Array von 0 WCHARs so lang wie.</span><span class="sxs-lookup"><span data-stu-id="a6862-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="a6862-170">Leerer String-Wert.</span><span class="sxs-lookup"><span data-stu-id="a6862-170">Empty string value.</span></span>
      
    - <span data-ttu-id="a6862-171">Allgemeine: Offset 0xB0.</span><span class="sxs-lookup"><span data-stu-id="a6862-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="a6862-172">PropSetGuid: Offset 0xB0 16 Byte: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="a6862-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="a6862-173">Fcapm: Offset "0xC0", 4 Bytes: 0 x 00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="a6862-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="a6862-174">DwString: Offset 0xC4 4 Bytes: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-175">DwBitmap: Offset 0xC8 4 Bytes: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-176">DwDisplay: Offset 0xCC 4 Bytes: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-177">iFmt: Offset 0xD0 4 Bytes: 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="a6862-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="a6862-178">WszFormulaLength: Offset 0xD4 2 Bytes: 0 x 0000 (0).</span><span class="sxs-lookup"><span data-stu-id="a6862-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="a6862-179">WszFormula: Offset 0xD6, Array von 0 WCHARs so lang wie.</span><span class="sxs-lookup"><span data-stu-id="a6862-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="a6862-180">Leerer String-Wert.</span><span class="sxs-lookup"><span data-stu-id="a6862-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6862-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6862-181">See also</span></span>

- [<span data-ttu-id="a6862-182">Elemente und Felder in Outlook</span><span class="sxs-lookup"><span data-stu-id="a6862-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="a6862-183">PropertyDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="a6862-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="a6862-184">FieldDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="a6862-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="a6862-185">SkipBlock-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="a6862-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="a6862-186">FirstSkipBlockContent-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="a6862-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="a6862-187">PackedAnsiString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="a6862-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="a6862-188">PackedUnicodeString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="a6862-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

