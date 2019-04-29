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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433528"
---
# <a name="spropvalue"></a><span data-ttu-id="2a4a4-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2a4a4-103">SPropValue</span></span>

  
  
<span data-ttu-id="2a4a4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a4a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a4a4-105">Beschreibt eine MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a4a4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2a4a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="2a4a4-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2a4a4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2a4a4-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="2a4a4-108">Related macros:</span></span>  <br/> |<span data-ttu-id="2a4a4-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="2a4a4-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="2a4a4-110">Members</span><span class="sxs-lookup"><span data-stu-id="2a4a4-110">Members</span></span>

 <span data-ttu-id="2a4a4-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="2a4a4-112">Property-Tag für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-112">Property tag for the property.</span></span> <span data-ttu-id="2a4a4-113">Eigenschaftstags sind 32-Bit-Ganzzahlen ohne Vorzeichen, bestehend aus dem eindeutigen Bezeichner der Eigenschaft in den hochwertigen 16 Bits und dem Typ der Eigenschaft in den niedrigwertigen 16 Bits.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="2a4a4-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="2a4a4-115">Reserviert für MAPI; nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="2a4a4-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-116">**Value**</span></span>
  
> <span data-ttu-id="2a4a4-117">Vereinigung von Datenwerten, der spezifische Wert, der vom Eigenschaftentyp diktiert wird.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="2a4a4-118">In der folgenden Tabelle werden die einzelnen Eigenschaftentypen, das zu verwendende Mitglied der Union und der zugehörige Datentyp aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="2a4a4-119">**Eigenschaftentyp**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-119">**Property type**</span></span>|<span data-ttu-id="2a4a4-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-120">**Value**</span></span>|<span data-ttu-id="2a4a4-121">**Datentyp des Werts**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2a4a4-122">PT_I2 oder PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="2a4a4-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="2a4a4-123">**i**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-123">**i**</span></span> <br/> |<span data-ttu-id="2a4a4-124">short int</span><span class="sxs-lookup"><span data-stu-id="2a4a4-124">short int</span></span>  <br/> |
|<span data-ttu-id="2a4a4-125">PT_I4 oder PT_LONG (signiert)</span><span class="sxs-lookup"><span data-stu-id="2a4a4-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="2a4a4-126">**l**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-126">**l**</span></span> <br/> |<span data-ttu-id="2a4a4-127">LONG</span><span class="sxs-lookup"><span data-stu-id="2a4a4-127">LONG</span></span>  <br/> |
|<span data-ttu-id="2a4a4-128">PT_I4 oder PT_LONG (unsigned)</span><span class="sxs-lookup"><span data-stu-id="2a4a4-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="2a4a4-129">**UL**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-129">**ul**</span></span> <br/> |<span data-ttu-id="2a4a4-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="2a4a4-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="2a4a4-131">PT_R4 oder PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="2a4a4-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="2a4a4-132">**FLT**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-132">**flt**</span></span> <br/> |<span data-ttu-id="2a4a4-133">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="2a4a4-133">float</span></span>  <br/> |
|<span data-ttu-id="2a4a4-134">PT_R8 oder PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="2a4a4-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="2a4a4-135">**Doppel**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-135">**dbl**</span></span> <br/> |<span data-ttu-id="2a4a4-136">double</span><span class="sxs-lookup"><span data-stu-id="2a4a4-136">double</span></span>  <br/> |
|<span data-ttu-id="2a4a4-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2a4a4-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="2a4a4-138">**b**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-138">**b**</span></span> <br/> |<span data-ttu-id="2a4a4-139">unsigned short int</span><span class="sxs-lookup"><span data-stu-id="2a4a4-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="2a4a4-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="2a4a4-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="2a4a4-141">**cur**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-141">**cur**</span></span> <br/> |[<span data-ttu-id="2a4a4-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="2a4a4-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="2a4a4-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="2a4a4-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="2a4a4-144">**auf**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-144">**at**</span></span> <br/> |<span data-ttu-id="2a4a4-145">double</span><span class="sxs-lookup"><span data-stu-id="2a4a4-145">double</span></span>  <br/> |
|<span data-ttu-id="2a4a4-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="2a4a4-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="2a4a4-147">**FT**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-147">**ft**</span></span> <br/> |[<span data-ttu-id="2a4a4-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="2a4a4-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="2a4a4-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="2a4a4-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="2a4a4-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-150">**lpszA**</span></span> <br/> |<span data-ttu-id="2a4a4-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="2a4a4-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="2a4a4-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2a4a4-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="2a4a4-153">**bin**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-153">**bin**</span></span> <br/> |<span data-ttu-id="2a4a4-154">BYTE [Array]</span><span class="sxs-lookup"><span data-stu-id="2a4a4-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="2a4a4-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2a4a4-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="2a4a4-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-156">**lpszW**</span></span> <br/> |<span data-ttu-id="2a4a4-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="2a4a4-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="2a4a4-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="2a4a4-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="2a4a4-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-159">**lpguid**</span></span> <br/> |<span data-ttu-id="2a4a4-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="2a4a4-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="2a4a4-161">PT_I8 oder PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="2a4a4-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="2a4a4-162">**Li**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-162">**li**</span></span> <br/> |<span data-ttu-id="2a4a4-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="2a4a4-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="2a4a4-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="2a4a4-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-165">**MVi**</span></span> <br/> |[<span data-ttu-id="2a4a4-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="2a4a4-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="2a4a4-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="2a4a4-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="2a4a4-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-168">**MVI**</span></span> <br/> |[<span data-ttu-id="2a4a4-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="2a4a4-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="2a4a4-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="2a4a4-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="2a4a4-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="2a4a4-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="2a4a4-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="2a4a4-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="2a4a4-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="2a4a4-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="2a4a4-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="2a4a4-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="2a4a4-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="2a4a4-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="2a4a4-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="2a4a4-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="2a4a4-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="2a4a4-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="2a4a4-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="2a4a4-180">**MVbei**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-180">**MVat**</span></span> <br/> |[<span data-ttu-id="2a4a4-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="2a4a4-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="2a4a4-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="2a4a4-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="2a4a4-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-183">**MVft**</span></span> <br/> |[<span data-ttu-id="2a4a4-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="2a4a4-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="2a4a4-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="2a4a4-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="2a4a4-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="2a4a4-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="2a4a4-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="2a4a4-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="2a4a4-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="2a4a4-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="2a4a4-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="2a4a4-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="2a4a4-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2a4a4-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="2a4a4-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="2a4a4-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="2a4a4-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="2a4a4-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="2a4a4-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="2a4a4-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="2a4a4-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="2a4a4-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="2a4a4-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="2a4a4-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="2a4a4-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-198">**MVli**</span></span> <br/> |[<span data-ttu-id="2a4a4-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="2a4a4-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="2a4a4-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="2a4a4-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="2a4a4-201">**err**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-201">**err**</span></span> <br/> |[<span data-ttu-id="2a4a4-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="2a4a4-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="2a4a4-203">PT_NULL oder PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="2a4a4-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="2a4a4-204">**x**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-204">**x**</span></span> <br/> |<span data-ttu-id="2a4a4-205">LONG</span><span class="sxs-lookup"><span data-stu-id="2a4a4-205">LONG</span></span>  <br/> |
|<span data-ttu-id="2a4a4-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="2a4a4-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="2a4a4-207">**LPV**</span><span class="sxs-lookup"><span data-stu-id="2a4a4-207">**lpv**</span></span> <br/> |<span data-ttu-id="2a4a4-208">VOID\*</span><span class="sxs-lookup"><span data-stu-id="2a4a4-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a4a4-209">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a4a4-209">Remarks</span></span>

<span data-ttu-id="2a4a4-210">Das **ulPropTag** -Element besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="2a4a4-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="2a4a4-211">Ein Bezeichner in den hochwertigen 16 Bits.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="2a4a4-212">Ein Typ in den niederwertigen 16 Bits.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="2a4a4-213">Der Bezeichner ist ein numerischer Wert in einem bestimmten Bereich.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="2a4a4-214">MAPI definiert Bereiche für Bezeichner, um zu beschreiben, wofür die Eigenschaft verwendet wird und wer für deren Verwaltung zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="2a4a4-215">MAPI definiert Einschränkungen für die einzelnen Eigenschaftentags, die in der Headerdatei Mapitags. h unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="2a4a4-216">Der Typ gibt das Format für den Wert der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="2a4a4-217">MAPI definiert Konstanten für alle Eigenschaftentypen, die in der Headerdatei Mapidefs. h unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="2a4a4-218">Eine vollständige Liste der gültigen Eigenschaftsbereiche für Bezeichner und Eigenschaftentypen finden Sie unter der [Eigenschaftsbezeichner und-Typen](property-identifiers-and-types.md) .</span><span class="sxs-lookup"><span data-stu-id="2a4a4-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="2a4a4-219">Das **dwAlignPad** -Element wird als Textabstand verwendet, um eine ordnungsgemäße Ausrichtung auf Computern sicherzustellen, die eine 8-Byte-Ausrichtung für 8-Byte-Werte erfordern.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="2a4a4-220">Entwickler, die Code auf solchen Computern schreiben, sollten Speicher Zuordnungs Routinen verwenden, die die **SPropValue** -Arrays an 8-Byte-Begrenzungen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="2a4a4-221">Weitere Informationen finden Sie unter [Übersicht über MAPI-Eigenschaftentypen](mapi-property-type-overview.md) und [Aktualisieren von MAPI-Eigenschaften](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="2a4a4-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2a4a4-222">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a4a4-222">See also</span></span>



[<span data-ttu-id="2a4a4-223">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2a4a4-223">MAPI Structures</span></span>](mapi-structures.md)

