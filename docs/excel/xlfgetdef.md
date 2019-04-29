---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 014db553156849d84bd07e0e416f8cb3fefb4e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421998"
---
# <a name="xlfgetdef"></a><span data-ttu-id="ee4ed-104">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="ee4ed-104">xlfGetDef</span></span>

<span data-ttu-id="ee4ed-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ee4ed-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ee4ed-106">Gibt den Namen als Text zurück, der für einen bestimmten Bereich, Wert oder eine Formel in einer Arbeitsmappe definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-106">Returns the name, as text, that is defined for a particular area, value, or formula in a workbook.</span></span> <span data-ttu-id="ee4ed-107">In Excel wird dieser Wert in der Spalte **Name** des Dialogfelds **Name Manager** angezeigt, das angezeigt wird, wenn Sie auf der Registerkarte **Formeln** im Abschnitt **definierte Namen** auf **Name Manager** klicken. verwenden Sie **xlfGetDef** , um die Name, der einer Definition entspricht.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-107">In Excel, this value is displayed in the **Name** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. Use **xlfGetDef** to get the name that corresponds to a definition.</span></span> <span data-ttu-id="ee4ed-108">Verwenden Sie [xlfGetName](xlfgetname.md), um die Definition eines Namens abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-108">To get the definition of a name, use [xlfGetName](xlfgetname.md).</span></span>
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a><span data-ttu-id="ee4ed-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee4ed-109">Parameters</span></span>

<span data-ttu-id="ee4ed-110">_pxDefText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="ee4ed-110">_pxDefText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="ee4ed-111">Kann alles sein, auf das Sie einen Namen definieren können, auf den verwiesen werden kann, einschließlich eines Verweises, eines Werts, eines Objekts oder einer Formel.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-111">Can be anything you can define a name to refer to, including a reference, a value, an object, or a formula.</span></span>
  
<span data-ttu-id="ee4ed-112">Verweise müssen im Z1S1-Format angegeben werden, Beispiels `"R3C5"`Weise.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-112">References must be given in R1C1 style, such as  `"R3C5"`.</span></span> <span data-ttu-id="ee4ed-113">Wenn _pxDefText_ ein Wert oder eine Formel ist, ist es nicht erforderlich, das Gleichheitszeichen einzuschließen, das \*\*\*\* in der Spalte bezieht sich im Dialogfeld **Name Manager** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-113">If  _pxDefText_ is a value or formula, it is not necessary to include the equal sign that is displayed in the **Refers To** column in the **Name Manager** dialog box.</span></span> <span data-ttu-id="ee4ed-114">Wenn mehrere Namen für _pxDefText_vorhanden sind, gibt **xlfGetDef** den Vornamen zurück.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-114">If there is more than one name for  _pxDefText_, **xlfGetDef** returns the first name.</span></span> <span data-ttu-id="ee4ed-115">Wenn kein Name mit _pxDefText_überein \*\*\*\* stimmt, gibt `#NAME?` xlfGetDef den Fehlerwert zurück.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-115">If no name matches  _pxDefText_, **xlfGetDef** returns the  `#NAME?` error value.</span></span> 
  
<span data-ttu-id="ee4ed-116">_pxDocumentText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="ee4ed-116">_pxDocumentText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="ee4ed-117">Gibt das Blatt an, in dem sich _pxDefText_ befindet.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-117">Specifies the sheet that  _pxDefText_ is on.</span></span> <span data-ttu-id="ee4ed-118">Wenn _pxDocumentText_ ausgelassen wird, wird davon ausgegangen, dass es sich um das aktive Blatt handelt.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-118">If  _pxDocumentText_ is omitted, it is assumed to be the active sheet.</span></span> 
  
<span data-ttu-id="ee4ed-119">_pxTypeNum_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="ee4ed-119">_pxTypeNum_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="ee4ed-120">Eine Zahl zwischen 1 und 3, die angibt, welche Typen von Namen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-120">A number from 1 to 3 specifying which types of names are returned.</span></span>
  
|<span data-ttu-id="ee4ed-121">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="ee4ed-121">**_pxTypeNum_**</span></span>|<span data-ttu-id="ee4ed-122">**gibt zurück**</span><span class="sxs-lookup"><span data-stu-id="ee4ed-122">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ee4ed-123">1 (oder Auslassung)</span><span class="sxs-lookup"><span data-stu-id="ee4ed-123">1 or omitted</span></span>  <br/> |<span data-ttu-id="ee4ed-124">Nur normale Namen.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-124">Normal names only.</span></span>  <br/> |
|<span data-ttu-id="ee4ed-125">2</span><span class="sxs-lookup"><span data-stu-id="ee4ed-125">2</span></span>  <br/> |<span data-ttu-id="ee4ed-126">Nur versteckte Namen.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-126">Hidden names only.</span></span>  <br/> |
|<span data-ttu-id="ee4ed-127">3</span><span class="sxs-lookup"><span data-stu-id="ee4ed-127">3</span></span>  <br/> |<span data-ttu-id="ee4ed-128">Alle Namen.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-128">All names.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="ee4ed-129">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee4ed-129">Property value/Return value</span></span>

 <span data-ttu-id="ee4ed-130">_pxRes_ (**xltypeStr** oder **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="ee4ed-130">_pxRes_ (**xltypeStr** or **xltypeErr**)</span></span>
  
<span data-ttu-id="ee4ed-131">Gibt den Namen zurück, der der angegebenen Definition zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-131">Returns the name associated with the specified definition.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ee4ed-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee4ed-132">Remarks</span></span>

<span data-ttu-id="ee4ed-133">Die folgende Tabelle enthält vier Beispiele für die Werte, die von einem Aufruf von **xlfGetDef** mit den angegebenen Argumenten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-133">The following table lists four examples of the values returned by a call to **xlfGetDef** with the specified arguments.</span></span> 
  
|<span data-ttu-id="ee4ed-134">**In Excel definierter Name**</span><span class="sxs-lookup"><span data-stu-id="ee4ed-134">**Name defined in Excel**</span></span>|<span data-ttu-id="ee4ed-135">**_pxDefText_**</span><span class="sxs-lookup"><span data-stu-id="ee4ed-135">**_pxDefText_**</span></span>|<span data-ttu-id="ee4ed-136">**_pxDocumentText_**</span><span class="sxs-lookup"><span data-stu-id="ee4ed-136">**_pxDocumentText_**</span></span>|<span data-ttu-id="ee4ed-137">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="ee4ed-137">**_pxTypeNum_**</span></span>|<span data-ttu-id="ee4ed-138">**ZurückgeGebener Wert**</span><span class="sxs-lookup"><span data-stu-id="ee4ed-138">**Value Returned**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ee4ed-139">Der angegebene Bereich in Sheet4 heißt Sales.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-139">The specified range in Sheet4 is named Sales.</span></span>  <br/> |<span data-ttu-id="ee4ed-140">"R2C2: R9C6"</span><span class="sxs-lookup"><span data-stu-id="ee4ed-140">"R2C2:R9C6"</span></span>  <br/> |<span data-ttu-id="ee4ed-141">Sheet4</span><span class="sxs-lookup"><span data-stu-id="ee4ed-141">"Sheet4"</span></span>  <br/> |<span data-ttu-id="ee4ed-142">\<weggelassen\></span><span class="sxs-lookup"><span data-stu-id="ee4ed-142">\<omitted\></span></span>  <br/> |<span data-ttu-id="ee4ed-143">Sales</span><span class="sxs-lookup"><span data-stu-id="ee4ed-143">"Sales"</span></span>  <br/> |
|<span data-ttu-id="ee4ed-144">Der Wert 100 in Sheet4 ist als Konstante definiert.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-144">The value 100 in Sheet4 is defined as Constant.</span></span>  <br/> |<span data-ttu-id="ee4ed-145">"100"</span><span class="sxs-lookup"><span data-stu-id="ee4ed-145">"100"</span></span>  <br/> |<span data-ttu-id="ee4ed-146">Sheet4</span><span class="sxs-lookup"><span data-stu-id="ee4ed-146">"Sheet4"</span></span>  <br/> |<span data-ttu-id="ee4ed-147">\<weggelassen\></span><span class="sxs-lookup"><span data-stu-id="ee4ed-147">\<omitted\></span></span>  <br/> |<span data-ttu-id="ee4ed-148">Konstante</span><span class="sxs-lookup"><span data-stu-id="ee4ed-148">"Constant"</span></span>  <br/> |
|<span data-ttu-id="ee4ed-149">Die angegebene Formel in Sheet4 hat den Namen SumTotal.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-149">The specified formula in Sheet4 is named SumTotal.</span></span>  <br/> |<span data-ttu-id="ee4ed-150">"SUM (Z1S1: R10C1)"</span><span class="sxs-lookup"><span data-stu-id="ee4ed-150">"SUM(R1C1:R10C1)"</span></span>  <br/> |<span data-ttu-id="ee4ed-151">Sheet4</span><span class="sxs-lookup"><span data-stu-id="ee4ed-151">"Sheet4"</span></span>  <br/> |<span data-ttu-id="ee4ed-152">\<weggelassen\></span><span class="sxs-lookup"><span data-stu-id="ee4ed-152">\<omitted\></span></span>  <br/> |<span data-ttu-id="ee4ed-153">SumTotal</span><span class="sxs-lookup"><span data-stu-id="ee4ed-153">"SumTotal"</span></span>  <br/> |
|<span data-ttu-id="ee4ed-154">3 wird als ausgeblendeter namens Zähler im aktiven Blatt definiert.</span><span class="sxs-lookup"><span data-stu-id="ee4ed-154">3 is defined as the hidden name Counter on the active sheet.</span></span>  <br/> |<span data-ttu-id="ee4ed-155">3</span><span class="sxs-lookup"><span data-stu-id="ee4ed-155">"3"</span></span>  <br/> |<span data-ttu-id="ee4ed-156">\<weggelassen\></span><span class="sxs-lookup"><span data-stu-id="ee4ed-156">\<omitted\></span></span>  <br/> |<span data-ttu-id="ee4ed-157">2</span><span class="sxs-lookup"><span data-stu-id="ee4ed-157">2</span></span>  <br/> |<span data-ttu-id="ee4ed-158">Zähler</span><span class="sxs-lookup"><span data-stu-id="ee4ed-158">"Counter"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee4ed-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee4ed-159">See also</span></span>

- [<span data-ttu-id="ee4ed-160">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="ee4ed-160">xlfGetName</span></span>](xlfgetname.md)
- [<span data-ttu-id="ee4ed-161">Wichtige und nützliche C-API-XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ee4ed-161">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

