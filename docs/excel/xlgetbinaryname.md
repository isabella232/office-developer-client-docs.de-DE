---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- xlgetbinaryname-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6d063213e3f83451e8a072e71f0878174214f73e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412464"
---
# <a name="xlgetbinaryname"></a><span data-ttu-id="b5937-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="b5937-104">xlGetBinaryName</span></span>

<span data-ttu-id="b5937-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b5937-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b5937-106">Wird verwendet, um ein Handle für von der [xlDefineBinaryName-Funktion](xldefinebinaryname.md)gespeicherte Daten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="b5937-106">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md).</span></span> <span data-ttu-id="b5937-107">Daten mit einem definierten binären Namen werden mit der Arbeitsmappe gespeichert und können jederzeit über den Namen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b5937-107">Data with a defined binary name is saved with the workbook and can be accessed by name at any time.</span></span> <span data-ttu-id="b5937-108">Weitere Informationen finden Sie unter "Beschränkung des binären Namensbereichs" in [bekannte Probleme in Excel XLL Development](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="b5937-108">For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="b5937-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5937-109">Parameters</span></span>

<span data-ttu-id="b5937-110">_pxRes_ (**xltypeBigData** oder **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="b5937-110">_pxRes_ (**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="b5937-111">Eine Struktur, die die abgerufenen Daten angibt, oder ein Fehler ist, dass die Daten nicht abgerufen oder der Name nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b5937-111">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined.</span></span> <span data-ttu-id="b5937-112">Wenn die Funktion zurückgibt, enthält das **hdata** -Element des **XLOPER**/ -**XLOPER12** ein Handle für die benannten Daten.</span><span class="sxs-lookup"><span data-stu-id="b5937-112">When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.</span></span>  <span data-ttu-id="b5937-113">_pxRes_ sollte bei einem Aufruf von **xlFree** freigegeben werden, wenn Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="b5937-113">_pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="b5937-114">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="b5937-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="b5937-115">Eine Zeichenfolge, die den Namen der Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="b5937-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5937-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5937-116">Remarks</span></span>

<span data-ttu-id="b5937-117">Microsoft Excel besitzt das in **hdata**zurückgegebene Speicherhandle.</span><span class="sxs-lookup"><span data-stu-id="b5937-117">Microsoft Excel owns the memory handle returned in **hdata**.</span></span> <span data-ttu-id="b5937-118">In Windows ist das Handle ein globaler Speicherhandle (der von der **GlobalAlloc** -Funktion zugeordnet wird).</span><span class="sxs-lookup"><span data-stu-id="b5937-118">In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b5937-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5937-119">See also</span></span>

- [<span data-ttu-id="b5937-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="b5937-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="b5937-121">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="b5937-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

