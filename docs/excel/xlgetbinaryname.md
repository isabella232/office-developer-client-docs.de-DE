---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- Xlgetbinaryname-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790601"
---
# <a name="xlgetbinaryname"></a><span data-ttu-id="1b39b-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="1b39b-104">xlGetBinaryName</span></span>

<span data-ttu-id="1b39b-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1b39b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1b39b-106">Verwendet, um ein Handle für das von der [Funktion "xlDefineBinaryName"](xldefinebinaryname.md)gespeicherte Daten zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1b39b-106">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md).</span></span> <span data-ttu-id="1b39b-107">Mit einem definierten Namen für die binäre Daten werden mit der Arbeitsmappe gespeichert und namentlich jederzeit zugegriffen werden können.</span><span class="sxs-lookup"><span data-stu-id="1b39b-107">Data with a defined binary name is saved with the workbook and can be accessed by name at any time.</span></span> <span data-ttu-id="1b39b-108">Weitere Informationen finden Sie unter "Binär nennen Bereich Einschränkung" unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="1b39b-108">For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="1b39b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b39b-109">Parameters</span></span>

<span data-ttu-id="1b39b-110">_pxRes_ (**XltypeBigData** oder **XltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="1b39b-110">_pxRes_ (**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="1b39b-111">Bigdata-Struktur, die angibt, dass die abgerufenen Daten oder ein Fehler ist die Daten konnten nicht abgerufen werden, oder der Name ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="1b39b-111">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined.</span></span> <span data-ttu-id="1b39b-112">Wenn die Funktion zurückgibt, das **Hdata** Mitglied der **XLOPER**/ **XLOPER12** enthält einen Handle für die benannten Daten.</span><span class="sxs-lookup"><span data-stu-id="1b39b-112">When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.</span></span>  <span data-ttu-id="1b39b-113">_PxRes_ sollte in einem Aufruf von **XlFree** bei Bedarf nicht mehr freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1b39b-113">_pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="1b39b-114">_pxName_ (**XltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="1b39b-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="1b39b-115">Eine Zeichenfolge zur Angabe der Name der Daten.</span><span class="sxs-lookup"><span data-stu-id="1b39b-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1b39b-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1b39b-116">Remarks</span></span>

<span data-ttu-id="1b39b-117">Microsoft Excel besitzt das Arbeitsspeicher-Handle in **Hdata**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b39b-117">Microsoft Excel owns the memory handle returned in **hdata**.</span></span> <span data-ttu-id="1b39b-118">In Windows ist das Handle einer globalen Arbeitsspeicher Handle (von der Funktion **GlobalAlloc** zugewiesen).</span><span class="sxs-lookup"><span data-stu-id="1b39b-118">In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1b39b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b39b-119">See also</span></span>

- [<span data-ttu-id="1b39b-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="1b39b-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="1b39b-121">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen</span><span class="sxs-lookup"><span data-stu-id="1b39b-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

