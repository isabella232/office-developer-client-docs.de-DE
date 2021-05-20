---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436629"
---
# <a name="xlfgetname"></a><span data-ttu-id="9be3c-104">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="9be3c-104">xlfGetName</span></span>

<span data-ttu-id="9be3c-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9be3c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9be3c-106">Gibt die Definition eines Namens zurück, wie sie in der Spalte **Verweist** auf des Dialogfelds  **Name Manager** angezeigt wird, die angezeigt wird, wenn Sie im Abschnitt Definierte Namen auf der Registerkarte **Formeln** auf **Name Manager** klicken. Wenn die Definition Verweise enthält, werden sie als R1C1-Verweise angegeben.</span><span class="sxs-lookup"><span data-stu-id="9be3c-106">Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references.</span></span> <span data-ttu-id="9be3c-107">Verwenden **Sie xlfGetName,** um den durch einen Namen definierten Wert zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9be3c-107">Use **xlfGetName** to check the value defined by a name.</span></span> <span data-ttu-id="9be3c-108">Verwenden Sie [xlfGetDef,](xlfgetdef.md)um den Namen zu erhalten, der einer Definition entspricht.</span><span class="sxs-lookup"><span data-stu-id="9be3c-108">To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).</span></span>
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a><span data-ttu-id="9be3c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9be3c-109">Parameters</span></span>

<span data-ttu-id="9be3c-110">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="9be3c-110">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="9be3c-111">Kann ein auf dem Blatt definierter Name sein. ein externer Verweis auf einen namen, der in der aktiven Arbeitsmappe definiert ist, z. B. ; oder ein externer Verweis auf einen Namen, der für eine bestimmte geöffnete Arbeitsmappe definiert ist, z. B.  `"!Sales"`  `"[Book1]SHEET1!Sales"` .</span><span class="sxs-lookup"><span data-stu-id="9be3c-111">Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.</span></span>  <span data-ttu-id="9be3c-112">_pxNameText_ kann auch ein ausgeblendeter Name sein.</span><span class="sxs-lookup"><span data-stu-id="9be3c-112">_pxNameText_ can also be a hidden name.</span></span> 
  
<span data-ttu-id="9be3c-113">_pxInfoType_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="9be3c-113">_pxInfoType_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="9be3c-114">Gibt den Typ der Informationen an, die über den Namen zurückgeben werden.</span><span class="sxs-lookup"><span data-stu-id="9be3c-114">Specifies the type of information to return about the name.</span></span> <span data-ttu-id="9be3c-115">Wenn **FALSE** oder nicht angegeben wird, wird die Definition zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9be3c-115">If **FALSE** or omitted, the definition is returned.</span></span> <span data-ttu-id="9be3c-116">Wenn **TRUE**, gibt **TRUE zurück,** wenn der Name nur für das Blatt definiert ist, **FALSE,** wenn der Name für die gesamte Arbeitsmappe definiert ist.</span><span class="sxs-lookup"><span data-stu-id="9be3c-116">If **TRUE**, returns **TRUE** if the name is defined for just the sheet, **FALSE** if the name is defined for the entire workbook.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9be3c-117">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9be3c-117">Property value/Return value</span></span>

<span data-ttu-id="9be3c-118">_pxRes_ (**xltypeStr**, **xltypeBool** oder **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="9be3c-118">_pxRes_ (**xltypeStr**, **xltypeBool**, or **xltypeErr**)</span></span>
  
<span data-ttu-id="9be3c-119">Gibt abhängig vom für  _pxInfoType_ übergebenen Wert die Definition des angegebenen Namens (**xltypeStr**) oder **TRUE** oder **FALSE** (**xltypeBool**) zurück.</span><span class="sxs-lookup"><span data-stu-id="9be3c-119">Depending on the value passed for  _pxInfoType_, returns the definition of the specified name (**xltypeStr**), or **TRUE** or **FALSE** (**xltypeBool**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9be3c-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9be3c-120">Remarks</span></span>

<span data-ttu-id="9be3c-121">Wenn das **Kontrollkästchen Arbeitsblatt und** Inhalt gesperrter  Zellen schützen im Dialogfeld Blatt schützen aktiviert wurde, um die Arbeitsmappe zu schützen, die den Namen enthält, gibt **xlfGetName** den `#N/A` Fehlerwert zurück.</span><span class="sxs-lookup"><span data-stu-id="9be3c-121">If the **Protect worksheet and contents of locked cells** check box has been selected in the **Protect Sheet** dialog box to protect the workbook containing the name, **xlfGetName** returns the  `#N/A` error value.</span></span> <span data-ttu-id="9be3c-122">Klicken Sie im Abschnitt Änderungen  **auf** der  Registerkarte Überprüfen auf Blatt schützen, um das Dialogfeld Blatt schützen **anzuzeigen.**</span><span class="sxs-lookup"><span data-stu-id="9be3c-122">To see the **Protect Sheet** dialog box, click **Protect Sheet** in the **Changes** section of the **Review** tab.</span></span> 
  
<span data-ttu-id="9be3c-123">In der folgenden Tabelle sind drei Beispiele für die Werte aufgeführt, die von einem Aufruf von **xlfGetDef** mit dem angegebenen  _Argument pxNameText zurückgegeben_ werden.</span><span class="sxs-lookup"><span data-stu-id="9be3c-123">The following table lists three examples of the values returned by a call to **xlfGetDef** with the specified  _pxNameText_ argument.</span></span> 
  
|<span data-ttu-id="9be3c-124">**Definition in Excel**</span><span class="sxs-lookup"><span data-stu-id="9be3c-124">**Definition in Excel**</span></span>|<span data-ttu-id="9be3c-125">**_pxNameText_**</span><span class="sxs-lookup"><span data-stu-id="9be3c-125">**_pxNameText_**</span></span>|<span data-ttu-id="9be3c-126">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="9be3c-126">**Value Returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9be3c-127">Der Name Sales auf einem Blatt wird als die Zahl 523 definiert.</span><span class="sxs-lookup"><span data-stu-id="9be3c-127">The name Sales on a sheet is defined as the number 523.</span></span>  <br/> |<span data-ttu-id="9be3c-128">"Sales"</span><span class="sxs-lookup"><span data-stu-id="9be3c-128">"Sales"</span></span>  <br/> |<span data-ttu-id="9be3c-129">"=523"</span><span class="sxs-lookup"><span data-stu-id="9be3c-129">"=523"</span></span>  <br/> |
|<span data-ttu-id="9be3c-130">Der Name Profit im aktiven Blatt wird als Formel =Sales-Costs definiert.</span><span class="sxs-lookup"><span data-stu-id="9be3c-130">The name Profit on the active sheet is defined as the formula =Sales-Costs.</span></span>  <br/> |<span data-ttu-id="9be3c-131">"! Profit"</span><span class="sxs-lookup"><span data-stu-id="9be3c-131">"!Profit"</span></span>  <br/> |<span data-ttu-id="9be3c-132">"=Sales-Costs"</span><span class="sxs-lookup"><span data-stu-id="9be3c-132">"=Sales-Costs"</span></span>  <br/> |
|<span data-ttu-id="9be3c-133">Der Name Database auf dem aktiven Blatt wird als Bereich A1:F500 definiert.</span><span class="sxs-lookup"><span data-stu-id="9be3c-133">The name Database on the active sheet is defined as the range A1:F500.</span></span>  <br/> |<span data-ttu-id="9be3c-134">"! Database"</span><span class="sxs-lookup"><span data-stu-id="9be3c-134">"!Database"</span></span>  <br/> |<span data-ttu-id="9be3c-135">"=R1C1:R500C6"</span><span class="sxs-lookup"><span data-stu-id="9be3c-135">"=R1C1:R500C6"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9be3c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9be3c-136">See also</span></span>

- [<span data-ttu-id="9be3c-137">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="9be3c-137">xlfGetDef</span></span>](xlfgetdef.md)
- [<span data-ttu-id="9be3c-138">Wichtige und nützliche C-API-XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9be3c-138">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

