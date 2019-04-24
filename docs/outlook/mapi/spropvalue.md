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
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326586"
---
# <a name="spropvalue"></a><span data-ttu-id="ff6bc-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ff6bc-103">SPropValue</span></span>

  
  
<span data-ttu-id="ff6bc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff6bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff6bc-105">Beschreibt eine MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff6bc-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ff6bc-106">Header file:</span></span>  <br/> |<span data-ttu-id="ff6bc-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ff6bc-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ff6bc-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="ff6bc-108">Related macros:</span></span>  <br/> |<span data-ttu-id="ff6bc-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="ff6bc-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="ff6bc-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="ff6bc-110">Members</span></span>

 <span data-ttu-id="ff6bc-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="ff6bc-112">Property-Tag für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-112">Property tag for the property.</span></span> <span data-ttu-id="ff6bc-113">Eigenschaftstags sind 32-Bit-Ganzzahlen ohne Vorzeichen, bestehend aus dem eindeutigen Bezeichner der Eigenschaft in den hochwertigen 16 Bits und dem Typ der Eigenschaft in den niedrigwertigen 16 Bits.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="ff6bc-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="ff6bc-115">Reserviert für MAPI; nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="ff6bc-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-116">**Value**</span></span>
  
> <span data-ttu-id="ff6bc-117">Vereinigung von Datenwerten, der spezifische Wert, der vom Eigenschaftentyp diktiert wird.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="ff6bc-118">In der folgenden Tabelle werden die einzelnen Eigenschaftentypen, das zu verwendende Mitglied der Union und der zugehörige Datentyp aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="ff6bc-119">**Eigenschaftentyp**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-119">**Property type**</span></span>|<span data-ttu-id="ff6bc-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-120">**Value**</span></span>|<span data-ttu-id="ff6bc-121">**Datentyp des Werts**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff6bc-122">PT_I2 oder PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="ff6bc-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="ff6bc-123">**i**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-123">**i**</span></span> <br/> |<span data-ttu-id="ff6bc-124">short int</span><span class="sxs-lookup"><span data-stu-id="ff6bc-124">short int</span></span>  <br/> |
|<span data-ttu-id="ff6bc-125">PT_I4 oder PT_LONG (signiert)</span><span class="sxs-lookup"><span data-stu-id="ff6bc-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="ff6bc-126">**l**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-126">**l**</span></span> <br/> |<span data-ttu-id="ff6bc-127">LONG</span><span class="sxs-lookup"><span data-stu-id="ff6bc-127">LONG</span></span>  <br/> |
|<span data-ttu-id="ff6bc-128">PT_I4 oder PT_LONG (unsigned)</span><span class="sxs-lookup"><span data-stu-id="ff6bc-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="ff6bc-129">**UL**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-129">**ul**</span></span> <br/> |<span data-ttu-id="ff6bc-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="ff6bc-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="ff6bc-131">PT_R4 oder PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="ff6bc-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="ff6bc-132">**FLT**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-132">**flt**</span></span> <br/> |<span data-ttu-id="ff6bc-133">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="ff6bc-133">float</span></span>  <br/> |
|<span data-ttu-id="ff6bc-134">PT_R8 oder PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="ff6bc-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="ff6bc-135">**Doppel**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-135">**dbl**</span></span> <br/> |<span data-ttu-id="ff6bc-136">double</span><span class="sxs-lookup"><span data-stu-id="ff6bc-136">double</span></span>  <br/> |
|<span data-ttu-id="ff6bc-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ff6bc-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="ff6bc-138">**b**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-138">**b**</span></span> <br/> |<span data-ttu-id="ff6bc-139">unsigned short int</span><span class="sxs-lookup"><span data-stu-id="ff6bc-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="ff6bc-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="ff6bc-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="ff6bc-141">**cur**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-141">**cur**</span></span> <br/> |[<span data-ttu-id="ff6bc-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="ff6bc-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="ff6bc-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="ff6bc-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="ff6bc-144">**auf**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-144">**at**</span></span> <br/> |<span data-ttu-id="ff6bc-145">double</span><span class="sxs-lookup"><span data-stu-id="ff6bc-145">double</span></span>  <br/> |
|<span data-ttu-id="ff6bc-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ff6bc-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="ff6bc-147">**FT**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-147">**ft**</span></span> <br/> |[<span data-ttu-id="ff6bc-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="ff6bc-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="ff6bc-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="ff6bc-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="ff6bc-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-150">**lpszA**</span></span> <br/> |<span data-ttu-id="ff6bc-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="ff6bc-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="ff6bc-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ff6bc-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="ff6bc-153">**bin**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-153">**bin**</span></span> <br/> |<span data-ttu-id="ff6bc-154">BYTE [Array]</span><span class="sxs-lookup"><span data-stu-id="ff6bc-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="ff6bc-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ff6bc-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="ff6bc-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-156">**lpszW**</span></span> <br/> |<span data-ttu-id="ff6bc-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ff6bc-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="ff6bc-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="ff6bc-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="ff6bc-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-159">**lpguid**</span></span> <br/> |<span data-ttu-id="ff6bc-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="ff6bc-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="ff6bc-161">PT_I8 oder PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="ff6bc-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="ff6bc-162">**Li**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-162">**li**</span></span> <br/> |<span data-ttu-id="ff6bc-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="ff6bc-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="ff6bc-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="ff6bc-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-165">**MVi**</span></span> <br/> |[<span data-ttu-id="ff6bc-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="ff6bc-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="ff6bc-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="ff6bc-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="ff6bc-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-168">**MVI**</span></span> <br/> |[<span data-ttu-id="ff6bc-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="ff6bc-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="ff6bc-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="ff6bc-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="ff6bc-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="ff6bc-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="ff6bc-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="ff6bc-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="ff6bc-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="ff6bc-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="ff6bc-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="ff6bc-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="ff6bc-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="ff6bc-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="ff6bc-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="ff6bc-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="ff6bc-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="ff6bc-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="ff6bc-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="ff6bc-180">**MVbei**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-180">**MVat**</span></span> <br/> |[<span data-ttu-id="ff6bc-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="ff6bc-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="ff6bc-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ff6bc-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="ff6bc-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-183">**MVft**</span></span> <br/> |[<span data-ttu-id="ff6bc-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="ff6bc-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="ff6bc-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="ff6bc-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="ff6bc-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="ff6bc-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="ff6bc-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="ff6bc-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="ff6bc-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="ff6bc-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="ff6bc-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="ff6bc-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="ff6bc-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ff6bc-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="ff6bc-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="ff6bc-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="ff6bc-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="ff6bc-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="ff6bc-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="ff6bc-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="ff6bc-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="ff6bc-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="ff6bc-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="ff6bc-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="ff6bc-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-198">**MVli**</span></span> <br/> |[<span data-ttu-id="ff6bc-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="ff6bc-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="ff6bc-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="ff6bc-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="ff6bc-201">**err**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-201">**err**</span></span> <br/> |[<span data-ttu-id="ff6bc-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="ff6bc-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="ff6bc-203">PT_NULL oder PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="ff6bc-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="ff6bc-204">**x**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-204">**x**</span></span> <br/> |<span data-ttu-id="ff6bc-205">LONG</span><span class="sxs-lookup"><span data-stu-id="ff6bc-205">LONG</span></span>  <br/> |
|<span data-ttu-id="ff6bc-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="ff6bc-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="ff6bc-207">**LPV**</span><span class="sxs-lookup"><span data-stu-id="ff6bc-207">**lpv**</span></span> <br/> |<span data-ttu-id="ff6bc-208">VOID\*</span><span class="sxs-lookup"><span data-stu-id="ff6bc-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff6bc-209">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff6bc-209">Remarks</span></span>

<span data-ttu-id="ff6bc-210">Das **ulPropTag** -Element besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="ff6bc-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="ff6bc-211">Ein Bezeichner in den hochwertigen 16 Bits.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="ff6bc-212">Ein Typ in den niederwertigen 16 Bits.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="ff6bc-213">Der Bezeichner ist ein numerischer Wert in einem bestimmten Bereich.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="ff6bc-214">MAPI definiert Bereiche für Bezeichner, um zu beschreiben, wofür die Eigenschaft verwendet wird und wer für deren Verwaltung zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="ff6bc-215">MAPI definiert Einschränkungen für die einzelnen Eigenschaftentags, die in der Headerdatei Mapitags. h unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="ff6bc-216">Der Typ gibt das Format für den Wert der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="ff6bc-217">MAPI definiert Konstanten für alle Eigenschaftentypen, die in der Headerdatei Mapidefs. h unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="ff6bc-218">Eine vollständige Liste der gültigen Eigenschaftsbereiche für Bezeichner und Eigenschaftentypen finden Sie unter der [Eigenschaftsbezeichner und-Typen](property-identifiers-and-types.md) .</span><span class="sxs-lookup"><span data-stu-id="ff6bc-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="ff6bc-219">Das **dwAlignPad** -Element wird als Textabstand verwendet, um eine ordnungsgemäße Ausrichtung auf Computern sicherzustellen, die eine 8-Byte-Ausrichtung für 8-Byte-Werte erfordern.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="ff6bc-220">Entwickler, die Code auf solchen Computern schreiben, sollten Speicher Zuordnungs Routinen verwenden, die die **SPropValue** -Arrays an 8-Byte-Begrenzungen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="ff6bc-221">Weitere Informationen finden Sie unter [Übersicht über MAPI-Eigenschaftentypen](mapi-property-type-overview.md) und [Aktualisieren von MAPI-Eigenschaften](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ff6bc-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ff6bc-222">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff6bc-222">See also</span></span>



[<span data-ttu-id="ff6bc-223">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ff6bc-223">MAPI Structures</span></span>](mapi-structures.md)

