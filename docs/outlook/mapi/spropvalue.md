---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f378bdd473410b846328cbe1f911eba9401f88cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795626"
---
# <a name="spropvalue"></a><span data-ttu-id="40495-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="40495-103">SPropValue</span></span>

  
  
<span data-ttu-id="40495-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40495-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40495-105">Beschreibt eine MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="40495-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40495-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="40495-106">Header file:</span></span>  <br/> |<span data-ttu-id="40495-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40495-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="40495-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="40495-108">Related macros:</span></span>  <br/> |<span data-ttu-id="40495-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [eigensch_id](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="40495-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="40495-110">Members</span><span class="sxs-lookup"><span data-stu-id="40495-110">Members</span></span>

 <span data-ttu-id="40495-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="40495-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="40495-112">Eigenschaftentag für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="40495-112">Property tag for the property.</span></span> <span data-ttu-id="40495-113">Eigenschaftentags sind nicht signierte 32-Bit-Ganzzahl bestehend aus der Eigenschaftenbezeichner in die obere 16-Bit und den Typ der Eigenschaft in den niederwertige 16 Bit.</span><span class="sxs-lookup"><span data-stu-id="40495-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="40495-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="40495-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="40495-115">Reserviert für die MAPI. Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="40495-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="40495-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="40495-116">**Value**</span></span>
  
> <span data-ttu-id="40495-117">Union von Datenwerten, die bestimmten Wert durch den Eigenschaftentyp vorgegeben.</span><span class="sxs-lookup"><span data-stu-id="40495-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="40495-118">Die folgende Tabelle enthält für jeden Eigenschaftentyp, das Mitglied der Union, die verwendet werden soll und dem entsprechenden Datentyp.</span><span class="sxs-lookup"><span data-stu-id="40495-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="40495-119">**Eigenschaftstyp**</span><span class="sxs-lookup"><span data-stu-id="40495-119">**Property type**</span></span>|<span data-ttu-id="40495-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="40495-120">**Value**</span></span>|<span data-ttu-id="40495-121">**Datentyp des Werts**</span><span class="sxs-lookup"><span data-stu-id="40495-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="40495-122">PT_I2 oder PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="40495-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="40495-123">**Ich**</span><span class="sxs-lookup"><span data-stu-id="40495-123">**i**</span></span> <br/> |<span data-ttu-id="40495-124">kurze int</span><span class="sxs-lookup"><span data-stu-id="40495-124">short int</span></span>  <br/> |
|<span data-ttu-id="40495-125">PT_I4 oder PT_LONG (mit Vorzeichen)</span><span class="sxs-lookup"><span data-stu-id="40495-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="40495-126">**l**</span><span class="sxs-lookup"><span data-stu-id="40495-126">**l**</span></span> <br/> |<span data-ttu-id="40495-127">LANGE</span><span class="sxs-lookup"><span data-stu-id="40495-127">LONG</span></span>  <br/> |
|<span data-ttu-id="40495-128">PT_I4 oder PT_LONG (ohne Vorzeichen)</span><span class="sxs-lookup"><span data-stu-id="40495-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="40495-129">**UL**</span><span class="sxs-lookup"><span data-stu-id="40495-129">**ul**</span></span> <br/> |<span data-ttu-id="40495-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="40495-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="40495-131">PT_R4 oder PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="40495-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="40495-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="40495-132">**flt**</span></span> <br/> |<span data-ttu-id="40495-133">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="40495-133">float</span></span>  <br/> |
|<span data-ttu-id="40495-134">PT_R8 oder PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="40495-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="40495-135">**Doppelte Japan**</span><span class="sxs-lookup"><span data-stu-id="40495-135">**dbl**</span></span> <br/> |<span data-ttu-id="40495-136">double</span><span class="sxs-lookup"><span data-stu-id="40495-136">double</span></span>  <br/> |
|<span data-ttu-id="40495-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="40495-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="40495-138">**b**</span><span class="sxs-lookup"><span data-stu-id="40495-138">**b**</span></span> <br/> |<span data-ttu-id="40495-139">nicht signierte kurze int</span><span class="sxs-lookup"><span data-stu-id="40495-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="40495-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="40495-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="40495-141">**Übernehmen**</span><span class="sxs-lookup"><span data-stu-id="40495-141">**cur**</span></span> <br/> |[<span data-ttu-id="40495-142">WÄHRUNG</span><span class="sxs-lookup"><span data-stu-id="40495-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="40495-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="40495-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="40495-144">**unter**</span><span class="sxs-lookup"><span data-stu-id="40495-144">**at**</span></span> <br/> |<span data-ttu-id="40495-145">double</span><span class="sxs-lookup"><span data-stu-id="40495-145">double</span></span>  <br/> |
|<span data-ttu-id="40495-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="40495-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="40495-147">**FT**</span><span class="sxs-lookup"><span data-stu-id="40495-147">**ft**</span></span> <br/> |[<span data-ttu-id="40495-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="40495-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="40495-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="40495-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="40495-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="40495-150">**lpszA**</span></span> <br/> |<span data-ttu-id="40495-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="40495-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="40495-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="40495-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="40495-153">**Papierkorb**</span><span class="sxs-lookup"><span data-stu-id="40495-153">**bin**</span></span> <br/> |<span data-ttu-id="40495-154">[BYTEARRAYS]</span><span class="sxs-lookup"><span data-stu-id="40495-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="40495-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40495-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="40495-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="40495-156">**lpszW**</span></span> <br/> |<span data-ttu-id="40495-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="40495-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="40495-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="40495-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="40495-159">**x lpguid**</span><span class="sxs-lookup"><span data-stu-id="40495-159">**lpguid**</span></span> <br/> |<span data-ttu-id="40495-160">X LPGUID</span><span class="sxs-lookup"><span data-stu-id="40495-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="40495-161">PT_I8 oder PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="40495-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="40495-162">**li**</span><span class="sxs-lookup"><span data-stu-id="40495-162">**li**</span></span> <br/> |<span data-ttu-id="40495-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="40495-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="40495-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="40495-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="40495-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="40495-165">**MVi**</span></span> <br/> |[<span data-ttu-id="40495-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="40495-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="40495-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="40495-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="40495-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="40495-168">**MVI**</span></span> <br/> |[<span data-ttu-id="40495-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="40495-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="40495-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="40495-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="40495-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="40495-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="40495-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="40495-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="40495-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="40495-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="40495-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="40495-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="40495-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="40495-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="40495-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="40495-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="40495-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="40495-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="40495-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="40495-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="40495-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="40495-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="40495-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="40495-180">**MVat**</span></span> <br/> |[<span data-ttu-id="40495-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="40495-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="40495-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="40495-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="40495-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="40495-183">**MVft**</span></span> <br/> |[<span data-ttu-id="40495-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="40495-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="40495-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="40495-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="40495-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="40495-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="40495-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="40495-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="40495-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="40495-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="40495-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="40495-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="40495-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="40495-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="40495-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40495-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="40495-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="40495-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="40495-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="40495-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="40495-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="40495-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="40495-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="40495-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="40495-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="40495-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="40495-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="40495-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="40495-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="40495-198">**MVli**</span></span> <br/> |[<span data-ttu-id="40495-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="40495-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="40495-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="40495-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="40495-201">**Err**</span><span class="sxs-lookup"><span data-stu-id="40495-201">**err**</span></span> <br/> |[<span data-ttu-id="40495-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="40495-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="40495-203">PT_NULL oder PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="40495-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="40495-204">**x**</span><span class="sxs-lookup"><span data-stu-id="40495-204">**x**</span></span> <br/> |<span data-ttu-id="40495-205">LANGE</span><span class="sxs-lookup"><span data-stu-id="40495-205">LONG</span></span>  <br/> |
|<span data-ttu-id="40495-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="40495-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="40495-207">**LPV**</span><span class="sxs-lookup"><span data-stu-id="40495-207">**lpv**</span></span> <br/> |<span data-ttu-id="40495-208">VOID\*</span><span class="sxs-lookup"><span data-stu-id="40495-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40495-209">Hinweise</span><span class="sxs-lookup"><span data-stu-id="40495-209">Remarks</span></span>

<span data-ttu-id="40495-210">Das Element **UlPropTag** besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="40495-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="40495-211">Ein Bezeichner in der hohen 16 Bits.</span><span class="sxs-lookup"><span data-stu-id="40495-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="40495-212">Ein Typ in den niederwertige 16 Bit.</span><span class="sxs-lookup"><span data-stu-id="40495-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="40495-213">Der Bezeichner ist einen numerischen Wert in einem bestimmten Bereich.</span><span class="sxs-lookup"><span data-stu-id="40495-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="40495-214">MAPI definiert Bereiche für Bezeichner zum Beschreiben der für die-Eigenschaft verwendet wird und die, die für die Verwaltung zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="40495-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="40495-215">MAPI definiert Einschränkungen für jede Eigenschaft Tags, die sie in der Headerdatei Mapitags.h unterstützt.</span><span class="sxs-lookup"><span data-stu-id="40495-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="40495-216">Der Typ gibt das Format für den Wert der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="40495-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="40495-217">MAPI definiert Konstanten für jede Eigenschaftentypen, die in der Headerdatei Mapidefs.h unterstützt.</span><span class="sxs-lookup"><span data-stu-id="40495-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="40495-218">Eine vollständige Liste der Bereiche gültige Eigenschaft für Bezeichner und Eigenschaftentypen finden Sie im Anhang [Eigenschaftenbezeichner und Typen](property-identifiers-and-types.md) .</span><span class="sxs-lookup"><span data-stu-id="40495-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="40495-219">Das **DwAlignPad** -Element wird als Abstand verwendet, um sicherzustellen, dass ordnungsgemäße Ausrichtung auf Computern erstellen, die 8-Byte-Ausrichtung für 8-Byte-Wert erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="40495-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="40495-220">Entwickler, die auf solchen Computern Code schreiben sollten Memory Allocation Routinen verwenden, die die **SPropValue** Arrays auf 8-Byte-Grenzen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="40495-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="40495-221">Weitere Informationen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md) und [Aktualisieren von MAPI-Eigenschaften](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="40495-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40495-222">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40495-222">See also</span></span>



[<span data-ttu-id="40495-223">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="40495-223">MAPI Structures</span></span>](mapi-structures.md)

