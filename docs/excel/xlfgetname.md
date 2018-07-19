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
ms.openlocfilehash: 63bfc6e94950a621c2367b2d35d25e3de48b344f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790594"
---
# <a name="xlfgetname"></a><span data-ttu-id="702bc-104">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="702bc-104">xlfGetName</span></span>

<span data-ttu-id="702bc-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="702bc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="702bc-106">Gibt die Definition eines Namens zurück, wie er in der Spalte **bezieht sich auf** das Dialogfeld **Namens-Manager** angezeigt, die angezeigt wird wird, wenn Sie **Namens-Manager** im Abschnitt **Definierte Namen** auf der Registerkarte **Formeln** klicken. Wenn die Definition Verweise enthält, werden sie als Z1S1-Bezügen angegeben.</span><span class="sxs-lookup"><span data-stu-id="702bc-106">Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references.</span></span> <span data-ttu-id="702bc-107">Verwenden Sie **XlfGetName** , überprüfen Sie den Wert durch einen Namen definiert.</span><span class="sxs-lookup"><span data-stu-id="702bc-107">Use **xlfGetName** to check the value defined by a name.</span></span> <span data-ttu-id="702bc-108">Verwenden Sie zum Abrufen des Namens, die eine Definition entspricht, [XlfGetDef](xlfgetdef.md).</span><span class="sxs-lookup"><span data-stu-id="702bc-108">To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).</span></span>
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a><span data-ttu-id="702bc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="702bc-109">Parameters</span></span>

<span data-ttu-id="702bc-110">_pxNameText_ (**XltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="702bc-110">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="702bc-111">Ein Namen kann für das Blatt definiert werden; ein externer Verweis auf einen Namen in der aktiven Arbeitsmappe definiert `"!Sales"`; oder ein externer Verweis auf einen Namen für einen bestimmten geöffnete Arbeitsmappe, beispielsweise definierte `"[Book1]SHEET1!Sales"`.</span><span class="sxs-lookup"><span data-stu-id="702bc-111">Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.</span></span>  <span data-ttu-id="702bc-112">_PxNameText_ kann auch ausgeblendeter Name sein.</span><span class="sxs-lookup"><span data-stu-id="702bc-112">_pxNameText_ can also be a hidden name.</span></span> 
  
<span data-ttu-id="702bc-113">_pxInfoType_ (**XltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="702bc-113">_pxInfoType_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="702bc-114">Gibt den Typ der Informationen, die über den Namen des zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="702bc-114">Specifies the type of information to return about the name.</span></span> <span data-ttu-id="702bc-115">Wenn **FALSE** oder weggelassen wird, wird die Definition zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="702bc-115">If **FALSE** or omitted, the definition is returned.</span></span> <span data-ttu-id="702bc-116">Wenn **TRUE**, gibt **TRUE** zurück, wenn der Name für lediglich das Arbeitsblatt, **FALSE** definiert ist, wenn der Name für die gesamte Arbeitsmappe definiert ist.</span><span class="sxs-lookup"><span data-stu-id="702bc-116">If **TRUE**, returns **TRUE** if the name is defined for just the sheet, **FALSE** if the name is defined for the entire workbook.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="702bc-117">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="702bc-117">Property value/Return value</span></span>

<span data-ttu-id="702bc-118">_pxRes_ (**XltypeStr**, **XltypeBool**oder **XltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="702bc-118">_pxRes_ (**xltypeStr**, **xltypeBool**, or **xltypeErr**)</span></span>
  
<span data-ttu-id="702bc-119">Abhängig vom Wert für _PxInfoType_übergeben gibt die Definition des angegebenen Namen (**XltypeStr**) oder **TRUE** oder **FALSE** (**XltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="702bc-119">Depending on the value passed for  _pxInfoType_, returns the definition of the specified name (**xltypeStr**), or **TRUE** or **FALSE** (**xltypeBool**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="702bc-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="702bc-120">Remarks</span></span>

<span data-ttu-id="702bc-121">Wenn das Kontrollkästchen **Arbeitsblatt und Inhalt gesperrter Zellen schützen** im Dialogfeld **Blatt schützen** ausgewählt wurde um die Arbeitsmappe mit dem Namen zu schützen, **XlfGetName** gibt die `#N/A` Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="702bc-121">If the **Protect worksheet and contents of locked cells** check box has been selected in the **Protect Sheet** dialog box to protect the workbook containing the name, **xlfGetName** returns the  `#N/A` error value.</span></span> <span data-ttu-id="702bc-122">Um das Dialogfeld **Blatt schützen** angezeigt wird, klicken Sie auf **Blatt schützen** im Abschnitt **Änderungen** von der Registerkarte **Überprüfen** .</span><span class="sxs-lookup"><span data-stu-id="702bc-122">To see the **Protect Sheet** dialog box, click **Protect Sheet** in the **Changes** section of the **Review** tab.</span></span> 
  
<span data-ttu-id="702bc-123">Die folgende Tabelle enthält drei Beispiele für die Werte durch einen Aufruf von **XlfGetDef** mit dem Argument angegebenen _PxNameText_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="702bc-123">The following table lists three examples of the values returned by a call to **xlfGetDef** with the specified  _pxNameText_ argument.</span></span> 
  
|<span data-ttu-id="702bc-124">**Definition in Excel**</span><span class="sxs-lookup"><span data-stu-id="702bc-124">**Definition in Excel**</span></span>|<span data-ttu-id="702bc-125">**_pxNameText_**</span><span class="sxs-lookup"><span data-stu-id="702bc-125">**_pxNameText_**</span></span>|<span data-ttu-id="702bc-126">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="702bc-126">**Value Returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="702bc-127">Den Namen Umsatz auf einem Blatt ist als die Anzahl 523 definiert.</span><span class="sxs-lookup"><span data-stu-id="702bc-127">The name Sales on a sheet is defined as the number 523.</span></span>  <br/> |<span data-ttu-id="702bc-128">"Sales"</span><span class="sxs-lookup"><span data-stu-id="702bc-128">"Sales"</span></span>  <br/> |<span data-ttu-id="702bc-129">"= 523"</span><span class="sxs-lookup"><span data-stu-id="702bc-129">"=523"</span></span>  <br/> |
|<span data-ttu-id="702bc-130">Der Name der Gewinn im aktiven Blatt festgelegt wie die Formel = Sales-Kosten.</span><span class="sxs-lookup"><span data-stu-id="702bc-130">The name Profit on the active sheet is defined as the formula =Sales-Costs.</span></span>  <br/> |<span data-ttu-id="702bc-131">"! Gewinn"</span><span class="sxs-lookup"><span data-stu-id="702bc-131">"!Profit"</span></span>  <br/> |<span data-ttu-id="702bc-132">"Sales-Kosten ="</span><span class="sxs-lookup"><span data-stu-id="702bc-132">"=Sales-Costs"</span></span>  <br/> |
|<span data-ttu-id="702bc-133">Der Name-Datenbank auf dem aktiven Blatt ist wie der Bereich A1:F500 definiert.</span><span class="sxs-lookup"><span data-stu-id="702bc-133">The name Database on the active sheet is defined as the range A1:F500.</span></span>  <br/> |<span data-ttu-id="702bc-134">"! Datenbank"</span><span class="sxs-lookup"><span data-stu-id="702bc-134">"!Database"</span></span>  <br/> |<span data-ttu-id="702bc-135">"R1C1:R500C6 ="</span><span class="sxs-lookup"><span data-stu-id="702bc-135">"=R1C1:R500C6"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="702bc-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="702bc-136">See also</span></span>

- [<span data-ttu-id="702bc-137">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="702bc-137">xlfGetDef</span></span>](xlfgetdef.md)
- [<span data-ttu-id="702bc-138">Wichtige und n�tzliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="702bc-138">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

