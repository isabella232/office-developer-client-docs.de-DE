---
title: FolderUserFields-Streambeispiel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e5251a619c70221987847830897ba349d63fd9cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433976"
---
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="f4736-103">FolderUserFields-Streambeispiel</span><span class="sxs-lookup"><span data-stu-id="f4736-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="f4736-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4736-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4736-105">In diesem Thema wird ein Beispiel für einen FolderUserFields-Stream beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f4736-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="f4736-106">Der Datenstrom enthält eine Definition eines benutzerdefinierten Felds,  `TextField1` .</span><span class="sxs-lookup"><span data-stu-id="f4736-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="f4736-107">Der Typ ist **Text**, und der FolderUserFields-Stream enthält sowohl FolderUserFieldsAnsi- als auch FolderUserFieldsUnicode-Teile.</span><span class="sxs-lookup"><span data-stu-id="f4736-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="f4736-108">Weitere Informationen finden Sie unter [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="f4736-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="f4736-109">Datenabbild</span><span class="sxs-lookup"><span data-stu-id="f4736-109">Data dump</span></span>

<span data-ttu-id="f4736-110">Es folgt ein Datenabbild des Datenstroms, wie er in einem binären Editor angezeigt würde.</span><span class="sxs-lookup"><span data-stu-id="f4736-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="f4736-111">Stream offset</span><span class="sxs-lookup"><span data-stu-id="f4736-111">Stream offset</span></span>|<span data-ttu-id="f4736-112">Datenbytes</span><span class="sxs-lookup"><span data-stu-id="f4736-112">Data bytes</span></span>|<span data-ttu-id="f4736-113">ASCII-Daten</span><span class="sxs-lookup"><span data-stu-id="f4736-113">ASCII data</span></span>|
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
   

<span data-ttu-id="f4736-114">Nachfolgend finden Sie eine Analyse der Beispieldaten für den **FolderUserFields-Stream:**</span><span class="sxs-lookup"><span data-stu-id="f4736-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="f4736-115">FolderUserFieldsAnsi: Offset 0x0.</span><span class="sxs-lookup"><span data-stu-id="f4736-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="f4736-116">FieldDefinitionCount: Offset 0x0, 4 Bytes: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="f4736-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="f4736-117">FieldDefinitions: Offset 0x4, Array von 2 FolderFieldDefinitionA-Datenströmen.</span><span class="sxs-lookup"><span data-stu-id="f4736-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="f4736-118">**Erstes Arrayelement**:</span><span class="sxs-lookup"><span data-stu-id="f4736-118">**First array element**:</span></span>
    
    - <span data-ttu-id="f4736-119">FieldType: Offset 0x4, 4 Bytes: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="f4736-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="f4736-120">FieldNameLength: Offset 0x8, 2 Bytes: 0x000A (10)</span><span class="sxs-lookup"><span data-stu-id="f4736-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="f4736-121">FieldName: Offset 0xA, Array von 10 CHARs.</span><span class="sxs-lookup"><span data-stu-id="f4736-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="f4736-122">ANSI-Zeichenfolgenwert: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="f4736-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="f4736-123">Common: Offset 0x14.</span><span class="sxs-lookup"><span data-stu-id="f4736-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="f4736-124">PropSetGuid: Offset 0x14, 16 Bytes: {00020329-0000-0000-C000-0000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="f4736-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="f4736-125">fcapm: Offset 0x24, 4 Bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="f4736-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="f4736-126">dwString: Offset 0x28, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-127">dwBitmap: Offset 0x2C, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-128">dwDisplay: Offset 0x30, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-129">iFmt: Offset 0x34, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-130">wszFormulaLength: Offset 0x38, 2 Bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="f4736-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="f4736-131">wszFormula: Offset 0x3A, Array von 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="f4736-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="f4736-132">Leerer Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="f4736-132">Empty string value.</span></span>
    
    <span data-ttu-id="f4736-133">**Zweites Arrayelement**:</span><span class="sxs-lookup"><span data-stu-id="f4736-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="f4736-134">FieldType: Offset 0x3A, 4 Bytes: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="f4736-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="f4736-135">FieldNameLength: Offset 0x3E, 2 Bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="f4736-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="f4736-136">FieldName: Offset 0x40, Array von 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="f4736-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="f4736-137">Leerer Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="f4736-137">Empty string value.</span></span>
      
    - <span data-ttu-id="f4736-138">Common: Offset 0x40.</span><span class="sxs-lookup"><span data-stu-id="f4736-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="f4736-139">PropSetGuid: Offset 0x40, 16 Bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="f4736-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="f4736-140">fcapm: Offset 0x50, 4 Bytes: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="f4736-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="f4736-141">dwString: Offset 0x54, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-142">dwBitmap: Offset 0x58, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-143">dwDisplay: Offset 0x5C, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-144">iFmt: Offset 0x60, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-145">wszFormulaLength: Offset 0x64, 2 Bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="f4736-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="f4736-146">wszFormula: Offset 0x66, Array von 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="f4736-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="f4736-147">Leerer Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="f4736-147">Empty string value.</span></span>
    
- <span data-ttu-id="f4736-148">FolderUserFieldsUnicode: Offset 0x66.</span><span class="sxs-lookup"><span data-stu-id="f4736-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="f4736-149">FieldDefinitionCount: Offset 0x66, 4 Bytes: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="f4736-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="f4736-150">FieldDefinitions: Offset 0x6A, Array von 2 FolderFieldDefinitionW-Datenströmen.</span><span class="sxs-lookup"><span data-stu-id="f4736-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="f4736-151">**Erstes Arrayelement**:</span><span class="sxs-lookup"><span data-stu-id="f4736-151">**First array element**:</span></span>
    
    - <span data-ttu-id="f4736-152">FieldType: Offset 0x6A, 4 Bytes: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="f4736-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="f4736-153">FieldNameLength: Offset 0x6E, 2 Bytes: 0x000A (10).</span><span class="sxs-lookup"><span data-stu-id="f4736-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="f4736-154">FieldName: Offset 0x70, Array von 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="f4736-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="f4736-155">Unicode-Zeichenfolgenwert: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="f4736-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="f4736-156">Common: Offset 0x84.</span><span class="sxs-lookup"><span data-stu-id="f4736-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="f4736-157">PropSetGuid: Offset 0x84, 16 Bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="f4736-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="f4736-158">fcapm: Offset 0x94, 4 Bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="f4736-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="f4736-159">dwString: Offset 0x98, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-160">dwBitmap: Offset 0x9C, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-161">dwDisplay: Offset 0xA0, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-162">iFmt: Offset 0xA4, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-163">wszFormulaLength: Offset 0xA8, 2 Bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="f4736-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="f4736-164">wszFormula: Offset 0xAA, Array von 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="f4736-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="f4736-165">Leerer Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="f4736-165">Empty string value.</span></span>
    
    <span data-ttu-id="f4736-166">**Zweites Arrayelement**:</span><span class="sxs-lookup"><span data-stu-id="f4736-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="f4736-167">FieldType: Offset 0xAA, 4 Bytes: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="f4736-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="f4736-168">FieldNameLength: Offset 0xAE, 2 Bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="f4736-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="f4736-169">FieldName: Offset 0xB0, Array von 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="f4736-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="f4736-170">Leerer Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="f4736-170">Empty string value.</span></span>
      
    - <span data-ttu-id="f4736-171">Common: Offset 0xB0.</span><span class="sxs-lookup"><span data-stu-id="f4736-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="f4736-172">PropSetGuid: Offset 0xB0, 16 Bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="f4736-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="f4736-173">fcapm: Offset 0xC0, 4 Bytes: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="f4736-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="f4736-174">dwString: Offset 0xC4, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-175">dwBitmap: Offset 0xC8, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-176">dwDisplay: Offset 0xCC, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-177">iFmt: Offset 0xD0, 4 Bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f4736-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="f4736-178">wszFormulaLength: Offset 0xD4, 2 Bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="f4736-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="f4736-179">wszFormula: Offset 0xD6, Array von 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="f4736-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="f4736-180">Leerer Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="f4736-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4736-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4736-181">See also</span></span>

- [<span data-ttu-id="f4736-182">Outlook Elemente und Felder</span><span class="sxs-lookup"><span data-stu-id="f4736-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="f4736-183">PropertyDefinition Stream Structure</span><span class="sxs-lookup"><span data-stu-id="f4736-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="f4736-184">FieldDefinition Stream Structure</span><span class="sxs-lookup"><span data-stu-id="f4736-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="f4736-185">SkipBlock Stream Structure</span><span class="sxs-lookup"><span data-stu-id="f4736-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="f4736-186">FirstSkipBlockContent Stream Structure</span><span class="sxs-lookup"><span data-stu-id="f4736-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="f4736-187">PackedAnsiString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="f4736-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="f4736-188">PackedUnicodeString-Datenstromstruktur</span><span class="sxs-lookup"><span data-stu-id="f4736-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

