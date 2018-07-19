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
ms.openlocfilehash: 030c4e501e8a9eb4b6ce29d7fe0e171324b50b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790615"
---
# <a name="xlfgetdef"></a><span data-ttu-id="50e40-104">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="50e40-104">xlfGetDef</span></span>

<span data-ttu-id="50e40-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="50e40-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="50e40-106">Gibt den Namen als Text, der für einen bestimmten Bereich, Wert oder eine Formel in einer Arbeitsmappe definiert ist.</span><span class="sxs-lookup"><span data-stu-id="50e40-106">Returns the name, as text, that is defined for a particular area, value, or formula in a workbook.</span></span> <span data-ttu-id="50e40-107">In Excel-dieser Wert wird angezeigt, in der Spalte **Name** des Dialogfelds **Namens-Manager** angezeigt wird, wenn Sie im Abschnitt **Definierte Namen** auf der Registerkarte **Formeln** verwenden **XlfGetDef** **Namens-Manager** zum Abrufen klicken Sie auf der Namen, die eine Definition entspricht.</span><span class="sxs-lookup"><span data-stu-id="50e40-107">In Excel, this value is displayed in the **Name** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. Use **xlfGetDef** to get the name that corresponds to a definition.</span></span> <span data-ttu-id="50e40-108">Wenn Sie die Definition eines Namens erhalten möchten, verwenden Sie [XlfGetName](xlfgetname.md).</span><span class="sxs-lookup"><span data-stu-id="50e40-108">To get the definition of a name, use [xlfGetName](xlfgetname.md).</span></span>
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a><span data-ttu-id="50e40-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="50e40-109">Parameters</span></span>

<span data-ttu-id="50e40-110">_pxDefText_ (**XltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="50e40-110">_pxDefText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="50e40-111">Kann sein Suchzeichenfolge Sie verweisen auf, einen Namen definieren können, einschließlich einen Verweis, einen Wert, ein Objekt oder eine Formel.</span><span class="sxs-lookup"><span data-stu-id="50e40-111">Can be anything you can define a name to refer to, including a reference, a value, an object, or a formula.</span></span>
  
<span data-ttu-id="50e40-112">Verweise müssen wie in Z1S1-Bezugsart angegeben werden `"R3C5"`.</span><span class="sxs-lookup"><span data-stu-id="50e40-112">References must be given in R1C1 style, such as  `"R3C5"`.</span></span> <span data-ttu-id="50e40-113">Wenn _PxDefText_ einen Wert oder eine Formel ist, ist es nicht erforderlich, Gleichheitszeichen enthalten, das in der Spalte **Bezieht sich auf** das Dialogfeld **Namens-Manager** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="50e40-113">If  _pxDefText_ is a value or formula, it is not necessary to include the equal sign that is displayed in the **Refers To** column in the **Name Manager** dialog box.</span></span> <span data-ttu-id="50e40-114">Wenn mehr als einen Namen für die _PxDefText_vorhanden ist, gibt **XlfGetDef** den Vornamen zurück.</span><span class="sxs-lookup"><span data-stu-id="50e40-114">If there is more than one name for  _pxDefText_, **xlfGetDef** returns the first name.</span></span> <span data-ttu-id="50e40-115">Wenn kein Name eines _PxDefText_entspricht, gibt **XlfGetDef** die `#NAME?` Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="50e40-115">If no name matches  _pxDefText_, **xlfGetDef** returns the  `#NAME?` error value.</span></span> 
  
<span data-ttu-id="50e40-116">_pxDocumentText_ (**XltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="50e40-116">_pxDocumentText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="50e40-117">Gibt das Blatt an diesem _PxDefText_ ist auf.</span><span class="sxs-lookup"><span data-stu-id="50e40-117">Specifies the sheet that  _pxDefText_ is on.</span></span> <span data-ttu-id="50e40-118">Wenn _PxDocumentText_ ausgelassen wird, wird angenommen, dass das aktive Blatt sein.</span><span class="sxs-lookup"><span data-stu-id="50e40-118">If  _pxDocumentText_ is omitted, it is assumed to be the active sheet.</span></span> 
  
<span data-ttu-id="50e40-119">_pxTypeNum_ (**XltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="50e40-119">_pxTypeNum_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="50e40-120">Eine Zahl zwischen 1 und 3 angeben, welche Arten von Namen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="50e40-120">A number from 1 to 3 specifying which types of names are returned.</span></span>
  
|<span data-ttu-id="50e40-121">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="50e40-121">**_pxTypeNum_**</span></span>|<span data-ttu-id="50e40-122">**gibt zurück**</span><span class="sxs-lookup"><span data-stu-id="50e40-122">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="50e40-123">1 (oder Auslassung)</span><span class="sxs-lookup"><span data-stu-id="50e40-123">1 or omitted</span></span>  <br/> |<span data-ttu-id="50e40-124">Normale Namen.</span><span class="sxs-lookup"><span data-stu-id="50e40-124">Normal names only.</span></span>  <br/> |
|<span data-ttu-id="50e40-125">2</span><span class="sxs-lookup"><span data-stu-id="50e40-125">2</span></span>  <br/> |<span data-ttu-id="50e40-126">Ausgeblendete Namen.</span><span class="sxs-lookup"><span data-stu-id="50e40-126">Hidden names only.</span></span>  <br/> |
|<span data-ttu-id="50e40-127">3</span><span class="sxs-lookup"><span data-stu-id="50e40-127">3</span></span>  <br/> |<span data-ttu-id="50e40-128">Alle Namen.</span><span class="sxs-lookup"><span data-stu-id="50e40-128">All names.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="50e40-129">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50e40-129">Property value/Return value</span></span>

 <span data-ttu-id="50e40-130">_pxRes_ (**XltypeStr** oder **XltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="50e40-130">_pxRes_ (**xltypeStr** or **xltypeErr**)</span></span>
  
<span data-ttu-id="50e40-131">Gibt den Namen der angegebenen Rollendefinition zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="50e40-131">Returns the name associated with the specified definition.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50e40-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50e40-132">Remarks</span></span>

<span data-ttu-id="50e40-133">Die folgende Tabelle enthält Beispiele für vier durch einen Aufruf von **XlfGetDef** mit den angegebenen Argumenten zurückgegebenen Werte sind.</span><span class="sxs-lookup"><span data-stu-id="50e40-133">The following table lists four examples of the values returned by a call to **xlfGetDef** with the specified arguments.</span></span> 
  
|<span data-ttu-id="50e40-134">**In Excel definierten Namen**</span><span class="sxs-lookup"><span data-stu-id="50e40-134">**Name defined in Excel**</span></span>|<span data-ttu-id="50e40-135">**_pxDefText_**</span><span class="sxs-lookup"><span data-stu-id="50e40-135">**_pxDefText_**</span></span>|<span data-ttu-id="50e40-136">**_pxDocumentText_**</span><span class="sxs-lookup"><span data-stu-id="50e40-136">**_pxDocumentText_**</span></span>|<span data-ttu-id="50e40-137">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="50e40-137">**_pxTypeNum_**</span></span>|<span data-ttu-id="50e40-138">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="50e40-138">**Value Returned**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="50e40-139">Im angegebene Bereich Tabelle4 heißt Sales.</span><span class="sxs-lookup"><span data-stu-id="50e40-139">The specified range in Sheet4 is named Sales.</span></span>  <br/> |<span data-ttu-id="50e40-140">"R2C2:R9C6"</span><span class="sxs-lookup"><span data-stu-id="50e40-140">"R2C2:R9C6"</span></span>  <br/> |<span data-ttu-id="50e40-141">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="50e40-141">"Sheet4"</span></span>  <br/> |<span data-ttu-id="50e40-142">\<ausgelassen\></span><span class="sxs-lookup"><span data-stu-id="50e40-142">\<omitted\></span></span>  <br/> |<span data-ttu-id="50e40-143">"Sales"</span><span class="sxs-lookup"><span data-stu-id="50e40-143">"Sales"</span></span>  <br/> |
|<span data-ttu-id="50e40-144">Der Wert 100 in Tabelle4 wird als Konstante definiert.</span><span class="sxs-lookup"><span data-stu-id="50e40-144">The value 100 in Sheet4 is defined as Constant.</span></span>  <br/> |<span data-ttu-id="50e40-145">"100"</span><span class="sxs-lookup"><span data-stu-id="50e40-145">"100"</span></span>  <br/> |<span data-ttu-id="50e40-146">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="50e40-146">"Sheet4"</span></span>  <br/> |<span data-ttu-id="50e40-147">\<ausgelassen\></span><span class="sxs-lookup"><span data-stu-id="50e40-147">\<omitted\></span></span>  <br/> |<span data-ttu-id="50e40-148">"Constant"</span><span class="sxs-lookup"><span data-stu-id="50e40-148">"Constant"</span></span>  <br/> |
|<span data-ttu-id="50e40-149">Die angegebene Formel in Tabelle4 heißt SumTotal.</span><span class="sxs-lookup"><span data-stu-id="50e40-149">The specified formula in Sheet4 is named SumTotal.</span></span>  <br/> |<span data-ttu-id="50e40-150">"SUM(R1C1:R10C1)"</span><span class="sxs-lookup"><span data-stu-id="50e40-150">"SUM(R1C1:R10C1)"</span></span>  <br/> |<span data-ttu-id="50e40-151">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="50e40-151">"Sheet4"</span></span>  <br/> |<span data-ttu-id="50e40-152">\<ausgelassen\></span><span class="sxs-lookup"><span data-stu-id="50e40-152">\<omitted\></span></span>  <br/> |<span data-ttu-id="50e40-153">"SumTotal"</span><span class="sxs-lookup"><span data-stu-id="50e40-153">"SumTotal"</span></span>  <br/> |
|<span data-ttu-id="50e40-154">3 ist definiert als die ausgeblendeten Namen Leistungsindikator im aktiven Blatt.</span><span class="sxs-lookup"><span data-stu-id="50e40-154">3 is defined as the hidden name Counter on the active sheet.</span></span>  <br/> |<span data-ttu-id="50e40-155">"3"</span><span class="sxs-lookup"><span data-stu-id="50e40-155">"3"</span></span>  <br/> |<span data-ttu-id="50e40-156">\<ausgelassen\></span><span class="sxs-lookup"><span data-stu-id="50e40-156">\<omitted\></span></span>  <br/> |<span data-ttu-id="50e40-157">2</span><span class="sxs-lookup"><span data-stu-id="50e40-157">2</span></span>  <br/> |<span data-ttu-id="50e40-158">"Counter"</span><span class="sxs-lookup"><span data-stu-id="50e40-158">"Counter"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50e40-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50e40-159">See also</span></span>

- [<span data-ttu-id="50e40-160">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="50e40-160">xlfGetName</span></span>](xlfgetname.md)
- [<span data-ttu-id="50e40-161">Wichtige und n�tzliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="50e40-161">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

