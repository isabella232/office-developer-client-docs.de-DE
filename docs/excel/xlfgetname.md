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
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303885"
---
# <a name="xlfgetname"></a><span data-ttu-id="0c5f1-104">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="0c5f1-104">xlfGetName</span></span>

<span data-ttu-id="0c5f1-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0c5f1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0c5f1-106">Gibt die Definition eines Namens zurück, wie er in der **Spalte bezieht sich** des Dialogfelds **Name Manager** angezeigt wird, das angezeigt wird, wenn Sie auf der Registerkarte **Formeln** im Abschnitt **definierte Namen** auf **Name Manager** klicken. Wenn die Definition Verweise enthält, werden diese als Z1S1-Verweise angegeben.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-106">Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references.</span></span> <span data-ttu-id="0c5f1-107">Verwenden Sie **xlfGetName** , um den durch einen Namen definierten Wert zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-107">Use **xlfGetName** to check the value defined by a name.</span></span> <span data-ttu-id="0c5f1-108">Verwenden Sie [xlfGetDef](xlfgetdef.md), um den Namen abzurufen, der einer Definition entspricht.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-108">To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).</span></span>
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a><span data-ttu-id="0c5f1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c5f1-109">Parameters</span></span>

<span data-ttu-id="0c5f1-110">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="0c5f1-110">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="0c5f1-111">Kann ein auf dem Blatt definierter Name sein. ein externer Verweis auf einen Namen, der in der aktiven Arbeitsmappe definiert ist `"!Sales"`, beispielsweise; oder einen externen Verweis auf einen Namen, der für eine bestimmte geöffnete Arbeitsmappe definiert `"[Book1]SHEET1!Sales"`ist, beispielsweise.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-111">Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.</span></span>  <span data-ttu-id="0c5f1-112">_pxNameText_ kann auch ein ausgeblendeter Name sein.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-112">_pxNameText_ can also be a hidden name.</span></span> 
  
<span data-ttu-id="0c5f1-113">_pxInfoType_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="0c5f1-113">_pxInfoType_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="0c5f1-114">Gibt den Typ der Informationen an, die über den Namen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-114">Specifies the type of information to return about the name.</span></span> <span data-ttu-id="0c5f1-115">Wenn **false** oder nicht angegeben, wird die Definition zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-115">If **FALSE** or omitted, the definition is returned.</span></span> <span data-ttu-id="0c5f1-116">Wenn **true**, gibt **true** zurück, wenn der Name nur für das Blatt definiert ist, **false** , wenn der Name für die gesamte Arbeitsmappe definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-116">If **TRUE**, returns **TRUE** if the name is defined for just the sheet, **FALSE** if the name is defined for the entire workbook.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0c5f1-117">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c5f1-117">Property value/Return value</span></span>

<span data-ttu-id="0c5f1-118">_pxRes_ (**xltypeStr**, **xltypeBool**oder **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="0c5f1-118">_pxRes_ (**xltypeStr**, **xltypeBool**, or **xltypeErr**)</span></span>
  
<span data-ttu-id="0c5f1-119">Gibt in Abhängigkeit vom für _pxInfoType_übergebenen Wert die Definition des angegebenen Namens (**XltypeStr**) oder **true** oder **false** (**xltypeBool**) zurück.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-119">Depending on the value passed for  _pxInfoType_, returns the definition of the specified name (**xltypeStr**), or **TRUE** or **FALSE** (**xltypeBool**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0c5f1-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c5f1-120">Remarks</span></span>

<span data-ttu-id="0c5f1-121">Wenn das Kontrollkästchen **Arbeitsblatt und Inhalt gesperrter Zellen schützen** im Dialogfeld **Blatt schützen** ausgewählt wurde, um die Arbeitsmappe mit dem Namen zu schützen, gibt `#N/A` **xlfGetName** den Fehlerwert zurück.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-121">If the **Protect worksheet and contents of locked cells** check box has been selected in the **Protect Sheet** dialog box to protect the workbook containing the name, **xlfGetName** returns the  `#N/A` error value.</span></span> <span data-ttu-id="0c5f1-122">Klicken Sie im Abschnitt **Änderungen** der Registerkarte **überprüfen** auf **Blatt schützen** , um das Dialogfeld **Blatt schützen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-122">To see the **Protect Sheet** dialog box, click **Protect Sheet** in the **Changes** section of the **Review** tab.</span></span> 
  
<span data-ttu-id="0c5f1-123">In der folgenden Tabelle sind drei Beispiele für die Werte aufgeführt, die von einem Aufruf von **xlfGetDef** mit dem angegebenen _pxNameText_ -Argument zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-123">The following table lists three examples of the values returned by a call to **xlfGetDef** with the specified  _pxNameText_ argument.</span></span> 
  
|<span data-ttu-id="0c5f1-124">**Definition in Excel**</span><span class="sxs-lookup"><span data-stu-id="0c5f1-124">**Definition in Excel**</span></span>|<span data-ttu-id="0c5f1-125">**_pxNameText_**</span><span class="sxs-lookup"><span data-stu-id="0c5f1-125">**_pxNameText_**</span></span>|<span data-ttu-id="0c5f1-126">**ZurückgeGebener Wert**</span><span class="sxs-lookup"><span data-stu-id="0c5f1-126">**Value Returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0c5f1-127">Der Name Verkäufe auf einem Blatt ist als Nummer 523 definiert.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-127">The name Sales on a sheet is defined as the number 523.</span></span>  <br/> |<span data-ttu-id="0c5f1-128">Sales</span><span class="sxs-lookup"><span data-stu-id="0c5f1-128">"Sales"</span></span>  <br/> |<span data-ttu-id="0c5f1-129">"= 523"</span><span class="sxs-lookup"><span data-stu-id="0c5f1-129">"=523"</span></span>  <br/> |
|<span data-ttu-id="0c5f1-130">Der Name Profit des aktiven Blatts ist definiert als Formel = Sales-costs.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-130">The name Profit on the active sheet is defined as the formula =Sales-Costs.</span></span>  <br/> |<span data-ttu-id="0c5f1-131">"! Gewinn</span><span class="sxs-lookup"><span data-stu-id="0c5f1-131">"!Profit"</span></span>  <br/> |<span data-ttu-id="0c5f1-132">"= Verkaufskosten"</span><span class="sxs-lookup"><span data-stu-id="0c5f1-132">"=Sales-Costs"</span></span>  <br/> |
|<span data-ttu-id="0c5f1-133">Die Name-Datenbank im aktiven Blatt ist als Range a1: F500 definiert.</span><span class="sxs-lookup"><span data-stu-id="0c5f1-133">The name Database on the active sheet is defined as the range A1:F500.</span></span>  <br/> |<span data-ttu-id="0c5f1-134">"! Datenbank</span><span class="sxs-lookup"><span data-stu-id="0c5f1-134">"!Database"</span></span>  <br/> |<span data-ttu-id="0c5f1-135">"= Z1S1: R500C6"</span><span class="sxs-lookup"><span data-stu-id="0c5f1-135">"=R1C1:R500C6"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c5f1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c5f1-136">See also</span></span>

- [<span data-ttu-id="0c5f1-137">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="0c5f1-137">xlfGetDef</span></span>](xlfgetdef.md)
- [<span data-ttu-id="0c5f1-138">Wichtige und n�tzliche C-API XLM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="0c5f1-138">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

