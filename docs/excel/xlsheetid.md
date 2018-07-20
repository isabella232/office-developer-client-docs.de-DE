---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- Xlsheetid-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e4e184d4e456ffe26292fe31b1b41463834216f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790612"
---
# <a name="xlsheetid"></a><span data-ttu-id="aa221-104">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="aa221-104">xlSheetId</span></span>

<span data-ttu-id="aa221-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="aa221-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="aa221-106">Sucht nach der Blatt-ID eines benannten Blatts, um externe Verweise zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aa221-106">Finds the sheet ID of a named sheet in order to construct external references.</span></span>
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a><span data-ttu-id="aa221-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa221-107">Parameters</span></span>

<span data-ttu-id="aa221-108">_pxSheetName_ (**XltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="aa221-108">_pxSheetName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="aa221-109">(Optional).</span><span class="sxs-lookup"><span data-stu-id="aa221-109">(Optional).</span></span> <span data-ttu-id="aa221-110">Der Name des Adressbuchs und Blatt, das Sie informieren möchten.</span><span class="sxs-lookup"><span data-stu-id="aa221-110">The name of the book and sheet you want to find out about.</span></span> <span data-ttu-id="aa221-111">Wenn Length angegeben, gibt die Funktion **XlSheetId** Blatt-ID des Blatts aktiv (vorne) zurück.</span><span class="sxs-lookup"><span data-stu-id="aa221-111">If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="aa221-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa221-112">Return value</span></span>

<span data-ttu-id="aa221-113">Gibt die Blatt-ID im _PxRes -\>val.mref.idSheet_.</span><span class="sxs-lookup"><span data-stu-id="aa221-113">Returns the sheet ID in  _pxRes-\>val.mref.idSheet_.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="aa221-114">Die _PxRes -\>val.mref.lpmref_ Array Zeiger ist auf NULL festgelegt wurde nach diesem Aufruf, damit besteht keine Notwendigkeit Aufrufen **XlFree** , um den Arbeitsspeicher, die normalerweise dieses Typs enthält, freizugeben, obwohl es dazu vollständig sicher ist.</span><span class="sxs-lookup"><span data-stu-id="aa221-114">The  _pxRes-\>val.mref.lpmref_ array pointer is set to NULL after this call so that there is no need to call **xlFree** to release the memory that this type normally contains, although it is completely safe to do so.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="aa221-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aa221-115">Remarks</span></span>

<span data-ttu-id="aa221-116">Die Arbeitsmappe mit dem angegebenen Blatt muss diese Funktion geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="aa221-116">The workbook containing the specified sheet must be open to use this function.</span></span> <span data-ttu-id="aa221-117">Es ist nicht möglich, einen Verweis auf eine nicht geöffneten Arbeitsmappe aus einer DLL zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aa221-117">There is no way to construct a reference to an unopened workbook from a DLL.</span></span> <span data-ttu-id="aa221-118">Weitere Informationen zur Verwendung von **XlSheetId** zum Referenzen zu erzeugen finden Sie unter [Speicherverwaltung in Excel](memory-management-in-excel.md) Beispiele für **XltypeRef** zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="aa221-118">For more information about using **xlSheetId** to construct references, see [Memory Management in Excel](memory-management-in-excel.md) for examples of **xltypeRef** construction.</span></span> 
  
## <a name="example"></a><span data-ttu-id="aa221-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="aa221-119">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="aa221-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa221-120">See also</span></span>

- [<span data-ttu-id="aa221-121">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="aa221-121">xlSheetNm</span></span>](xlsheetnm.md)
- [<span data-ttu-id="aa221-122">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="aa221-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

