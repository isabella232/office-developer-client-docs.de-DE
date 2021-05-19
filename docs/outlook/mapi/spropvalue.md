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
# <a name="spropvalue"></a><span data-ttu-id="aca9e-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="aca9e-103">SPropValue</span></span>

  
  
<span data-ttu-id="aca9e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aca9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aca9e-105">Beschreibt eine MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="aca9e-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aca9e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="aca9e-106">Header file:</span></span>  <br/> |<span data-ttu-id="aca9e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aca9e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="aca9e-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="aca9e-108">Related macros:</span></span>  <br/> |<span data-ttu-id="aca9e-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="aca9e-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="aca9e-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="aca9e-110">Members</span></span>

 <span data-ttu-id="aca9e-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="aca9e-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="aca9e-112">Eigenschaftstag für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="aca9e-112">Property tag for the property.</span></span> <span data-ttu-id="aca9e-113">Eigenschaftstags sind 32-Bit-ganzzahlige, nicht signierte Ganzzahlen, die aus dem eindeutigen Bezeichner der Eigenschaft in der hohen Reihenfolge von 16 Bit und dem Typ der Eigenschaft in der niedrigen Reihenfolge von 16 Bit bestehen.</span><span class="sxs-lookup"><span data-stu-id="aca9e-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="aca9e-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="aca9e-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="aca9e-115">Reserviert für MAPI; nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="aca9e-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="aca9e-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="aca9e-116">**Value**</span></span>
  
> <span data-ttu-id="aca9e-117">Union der Datenwerte, der vom Eigenschaftentyp diktierte spezifische Wert.</span><span class="sxs-lookup"><span data-stu-id="aca9e-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="aca9e-118">In der folgenden Tabelle sind die einzelnen Eigenschaftentypen, das Zu verwendende Mitglied der Union und der zugehörige Datentyp aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="aca9e-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="aca9e-119">**Eigenschaftentyp**</span><span class="sxs-lookup"><span data-stu-id="aca9e-119">**Property type**</span></span>|<span data-ttu-id="aca9e-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="aca9e-120">**Value**</span></span>|<span data-ttu-id="aca9e-121">**Datentyp value**</span><span class="sxs-lookup"><span data-stu-id="aca9e-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aca9e-122">PT_I2 oder PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="aca9e-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="aca9e-123">**i**</span><span class="sxs-lookup"><span data-stu-id="aca9e-123">**i**</span></span> <br/> |<span data-ttu-id="aca9e-124">short int</span><span class="sxs-lookup"><span data-stu-id="aca9e-124">short int</span></span>  <br/> |
|<span data-ttu-id="aca9e-125">PT_I4 oder PT_LONG (signiert)</span><span class="sxs-lookup"><span data-stu-id="aca9e-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="aca9e-126">**l**</span><span class="sxs-lookup"><span data-stu-id="aca9e-126">**l**</span></span> <br/> |<span data-ttu-id="aca9e-127">LONG</span><span class="sxs-lookup"><span data-stu-id="aca9e-127">LONG</span></span>  <br/> |
|<span data-ttu-id="aca9e-128">PT_I4 oder PT_LONG (nicht signiert)</span><span class="sxs-lookup"><span data-stu-id="aca9e-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="aca9e-129">**ul**</span><span class="sxs-lookup"><span data-stu-id="aca9e-129">**ul**</span></span> <br/> |<span data-ttu-id="aca9e-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="aca9e-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="aca9e-131">PT_R4 oder PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="aca9e-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="aca9e-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="aca9e-132">**flt**</span></span> <br/> |<span data-ttu-id="aca9e-133">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="aca9e-133">float</span></span>  <br/> |
|<span data-ttu-id="aca9e-134">PT_R8 oder PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="aca9e-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="aca9e-135">**dbl**</span><span class="sxs-lookup"><span data-stu-id="aca9e-135">**dbl**</span></span> <br/> |<span data-ttu-id="aca9e-136">double</span><span class="sxs-lookup"><span data-stu-id="aca9e-136">double</span></span>  <br/> |
|<span data-ttu-id="aca9e-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="aca9e-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="aca9e-138">**b**</span><span class="sxs-lookup"><span data-stu-id="aca9e-138">**b**</span></span> <br/> |<span data-ttu-id="aca9e-139">unsigned short int</span><span class="sxs-lookup"><span data-stu-id="aca9e-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="aca9e-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="aca9e-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="aca9e-141">**cur**</span><span class="sxs-lookup"><span data-stu-id="aca9e-141">**cur**</span></span> <br/> |[<span data-ttu-id="aca9e-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="aca9e-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="aca9e-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="aca9e-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="aca9e-144">**at**</span><span class="sxs-lookup"><span data-stu-id="aca9e-144">**at**</span></span> <br/> |<span data-ttu-id="aca9e-145">double</span><span class="sxs-lookup"><span data-stu-id="aca9e-145">double</span></span>  <br/> |
|<span data-ttu-id="aca9e-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="aca9e-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="aca9e-147">**ft**</span><span class="sxs-lookup"><span data-stu-id="aca9e-147">**ft**</span></span> <br/> |[<span data-ttu-id="aca9e-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="aca9e-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="aca9e-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="aca9e-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="aca9e-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="aca9e-150">**lpszA**</span></span> <br/> |<span data-ttu-id="aca9e-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="aca9e-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="aca9e-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="aca9e-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="aca9e-153">**bin**</span><span class="sxs-lookup"><span data-stu-id="aca9e-153">**bin**</span></span> <br/> |<span data-ttu-id="aca9e-154">BYTE [array]</span><span class="sxs-lookup"><span data-stu-id="aca9e-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="aca9e-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aca9e-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="aca9e-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="aca9e-156">**lpszW**</span></span> <br/> |<span data-ttu-id="aca9e-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="aca9e-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="aca9e-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="aca9e-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="aca9e-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="aca9e-159">**lpguid**</span></span> <br/> |<span data-ttu-id="aca9e-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="aca9e-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="aca9e-161">PT_I8 oder PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="aca9e-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="aca9e-162">**li**</span><span class="sxs-lookup"><span data-stu-id="aca9e-162">**li**</span></span> <br/> |<span data-ttu-id="aca9e-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="aca9e-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="aca9e-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="aca9e-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="aca9e-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="aca9e-165">**MVi**</span></span> <br/> |[<span data-ttu-id="aca9e-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="aca9e-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="aca9e-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="aca9e-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="aca9e-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="aca9e-168">**MVI**</span></span> <br/> |[<span data-ttu-id="aca9e-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="aca9e-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="aca9e-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="aca9e-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="aca9e-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="aca9e-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="aca9e-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="aca9e-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="aca9e-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="aca9e-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="aca9e-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="aca9e-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="aca9e-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="aca9e-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="aca9e-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="aca9e-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="aca9e-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="aca9e-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="aca9e-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="aca9e-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="aca9e-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="aca9e-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="aca9e-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="aca9e-180">**MVat**</span></span> <br/> |[<span data-ttu-id="aca9e-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="aca9e-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="aca9e-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="aca9e-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="aca9e-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="aca9e-183">**MVft**</span></span> <br/> |[<span data-ttu-id="aca9e-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="aca9e-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="aca9e-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="aca9e-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="aca9e-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="aca9e-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="aca9e-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="aca9e-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="aca9e-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="aca9e-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="aca9e-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="aca9e-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="aca9e-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="aca9e-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="aca9e-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aca9e-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="aca9e-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="aca9e-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="aca9e-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="aca9e-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="aca9e-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="aca9e-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="aca9e-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="aca9e-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="aca9e-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="aca9e-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="aca9e-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="aca9e-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="aca9e-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="aca9e-198">**MVli**</span></span> <br/> |[<span data-ttu-id="aca9e-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="aca9e-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="aca9e-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="aca9e-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="aca9e-201">**err**</span><span class="sxs-lookup"><span data-stu-id="aca9e-201">**err**</span></span> <br/> |[<span data-ttu-id="aca9e-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="aca9e-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="aca9e-203">PT_NULL oder PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="aca9e-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="aca9e-204">**x**</span><span class="sxs-lookup"><span data-stu-id="aca9e-204">**x**</span></span> <br/> |<span data-ttu-id="aca9e-205">LONG</span><span class="sxs-lookup"><span data-stu-id="aca9e-205">LONG</span></span>  <br/> |
|<span data-ttu-id="aca9e-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="aca9e-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="aca9e-207">**lpv**</span><span class="sxs-lookup"><span data-stu-id="aca9e-207">**lpv**</span></span> <br/> |<span data-ttu-id="aca9e-208">VOID \*</span><span class="sxs-lookup"><span data-stu-id="aca9e-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aca9e-209">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aca9e-209">Remarks</span></span>

<span data-ttu-id="aca9e-210">Das **ulPropTag-Element** besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="aca9e-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="aca9e-211">Ein Bezeichner in der hohen Reihenfolge von 16 Bit.</span><span class="sxs-lookup"><span data-stu-id="aca9e-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="aca9e-212">Ein Typ in niedriger Reihenfolge von 16 Bit.</span><span class="sxs-lookup"><span data-stu-id="aca9e-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="aca9e-213">Der Bezeichner ist ein numerischer Wert innerhalb eines bestimmten Bereichs.</span><span class="sxs-lookup"><span data-stu-id="aca9e-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="aca9e-214">MAPI definiert Bereiche für Bezeichner, um zu beschreiben, wofür die Eigenschaft verwendet wird und wer für die Verwaltung verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="aca9e-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="aca9e-215">MAPI definiert Einschränkungen für jedes der Eigenschaftentags, die es in der Mapitags.h-Headerdatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aca9e-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="aca9e-216">Der Typ gibt das Format für den Wert der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="aca9e-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="aca9e-217">MAPI definiert Konstanten für jeden der Eigenschaftentypen, die in der Mapidefs.h-Headerdatei unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="aca9e-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="aca9e-218">Eine vollständige Liste der gültigen Eigenschaftsbereiche für Bezeichner und Eigenschaftstypen finden Sie im Anhang [Property Identifiers and Types.](property-identifiers-and-types.md)</span><span class="sxs-lookup"><span data-stu-id="aca9e-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="aca9e-219">Das **dwAlignPad-Element** wird als Abstand verwendet, um die ordnungsgemäße Ausrichtung auf Computern sicherzustellen, für die eine 8-Byte-Ausrichtung für 8-Byte-Werte erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="aca9e-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="aca9e-220">Entwickler, die Code auf solchen Computern schreiben, sollten Speicherzuweisungsroutinen verwenden, die **die SPropValue-Arrays** an 8-Byte-Grenzen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="aca9e-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="aca9e-221">Weitere Informationen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="aca9e-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aca9e-222">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aca9e-222">See also</span></span>



[<span data-ttu-id="aca9e-223">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="aca9e-223">MAPI Structures</span></span>](mapi-structures.md)

