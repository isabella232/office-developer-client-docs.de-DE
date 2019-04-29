---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- xlsheetid-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428431"
---
# <a name="xlsheetid"></a><span data-ttu-id="c0ddb-104">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="c0ddb-104">xlSheetId</span></span>

<span data-ttu-id="c0ddb-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c0ddb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c0ddb-106">Sucht die Blatt-ID eines benannten Blatts, um externe Verweise zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c0ddb-106">Finds the sheet ID of a named sheet in order to construct external references.</span></span>
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a><span data-ttu-id="c0ddb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0ddb-107">Parameters</span></span>

<span data-ttu-id="c0ddb-108">_pxSheetName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="c0ddb-108">_pxSheetName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="c0ddb-109">(Optional).</span><span class="sxs-lookup"><span data-stu-id="c0ddb-109">(Optional).</span></span> <span data-ttu-id="c0ddb-110">Der Name des Buches und des Blatts, über das Sie sich informieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c0ddb-110">The name of the book and sheet you want to find out about.</span></span> <span data-ttu-id="c0ddb-111">Wenn kein Wert angegeben wird, gibt die **XLSHEETID** -Funktion die Blatt-ID des aktiven (Front-) Blatts zurück.</span><span class="sxs-lookup"><span data-stu-id="c0ddb-111">If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="c0ddb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0ddb-112">Return value</span></span>

<span data-ttu-id="c0ddb-113">Gibt die Blatt-ID in _pxRes\>-Val. mref. idSheet_zurück.</span><span class="sxs-lookup"><span data-stu-id="c0ddb-113">Returns the sheet ID in  _pxRes-\>val.mref.idSheet_.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c0ddb-114">Der _pxRes-\>Val. mref. lpmref-_ Array Zeiger wird nach diesem Aufruf auf NULL festgelegt, sodass es nicht erforderlich ist, **xlFree** aufzurufen, um den von diesem Typ normalerweise enthaltenen Speicher freizugeben, obwohl dies vollständig sicher ist.</span><span class="sxs-lookup"><span data-stu-id="c0ddb-114">The  _pxRes-\>val.mref.lpmref_ array pointer is set to NULL after this call so that there is no need to call **xlFree** to release the memory that this type normally contains, although it is completely safe to do so.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c0ddb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0ddb-115">Remarks</span></span>

<span data-ttu-id="c0ddb-116">Die Arbeitsmappe mit dem angegebenen Blatt muss geöffnet sein, um diese Funktion verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="c0ddb-116">The workbook containing the specified sheet must be open to use this function.</span></span> <span data-ttu-id="c0ddb-117">Es gibt keine Möglichkeit, einen Verweis auf eine nicht geöffnete Arbeitsmappe aus einer DLL zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c0ddb-117">There is no way to construct a reference to an unopened workbook from a DLL.</span></span> <span data-ttu-id="c0ddb-118">Weitere Informationen zur Verwendung von **xlSheetId** zum Erstellen von Verweisen finden Sie unter [Memory Management in Excel](memory-management-in-excel.md) for examples of **externen xltypeRef** Construction.</span><span class="sxs-lookup"><span data-stu-id="c0ddb-118">For more information about using **xlSheetId** to construct references, see [Memory Management in Excel](memory-management-in-excel.md) for examples of **xltypeRef** construction.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c0ddb-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c0ddb-119">Example</span></span>

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="c0ddb-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0ddb-120">See also</span></span>

- [<span data-ttu-id="c0ddb-121">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="c0ddb-121">xlSheetNm</span></span>](xlsheetnm.md)
- [<span data-ttu-id="c0ddb-122">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="c0ddb-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

