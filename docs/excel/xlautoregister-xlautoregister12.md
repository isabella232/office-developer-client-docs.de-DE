---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- xlautoregister-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421165"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="969d3-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="969d3-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="969d3-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="969d3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="969d3-106">Excel ruft die [xlAutoRegister-Funktion](xlautoregister-xlautoregister12.md) auf, wenn ein Aufruf der XLM-Funktion **REGISTER** oder der C-API-äquivalenten [xlfRegister-Funktion](xlfregister-form-1.md)erfolgt ist, und die Rückgabe- und Argumenttypen der registrierten Funktion fehlen.</span><span class="sxs-lookup"><span data-stu-id="969d3-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="969d3-107">Die XLL kann ihre internen Listen exportierter Funktionen und Befehle durchsuchen, um die Funktion mit den angegebenen Argument- und Rückgabetypen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="969d3-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="969d3-108">Ab Excel 2007 ruft Excel die **xlAutoRegister12-Funktion** vor der **xlAutoRegister-Funktion** auf, wenn sie von der XLL exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="969d3-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="969d3-109">Excel erfordert keine XLL zum Implementieren und Exportieren einer dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="969d3-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="969d3-110">Wenn **xlAutoRegister** /  **xlAutoRegister12** versucht, die Funktion zu registrieren, ohne das Argument und die Rückgabetypen zu liefern, tritt eine rekursive Aufrufschleife auf, die schließlich die Aufrufliste überläuft und Excel.</span><span class="sxs-lookup"><span data-stu-id="969d3-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="969d3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="969d3-111">Parameters</span></span>

 <span data-ttu-id="969d3-112">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="969d3-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="969d3-113">Der Name der XLL-Funktion, die registriert wird.</span><span class="sxs-lookup"><span data-stu-id="969d3-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="969d3-114">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="969d3-114">Property value/Return value</span></span>

<span data-ttu-id="969d3-115">Die Funktion sollte das Ergebnis des Versuches zurückgeben, die XLL-Funktion  _pxName_ mithilfe der **xlfRegister-Funktion zu** registrieren.</span><span class="sxs-lookup"><span data-stu-id="969d3-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="969d3-116">Wenn die angegebene Funktion nicht zu den Exporten der XLL gehört, sollte die angegebene **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="969d3-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="969d3-117">-Fehler oder **NULL,** Excel bei **#VALUE! interpretiert wird.**</span><span class="sxs-lookup"><span data-stu-id="969d3-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="969d3-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="969d3-118">Remarks</span></span>

<span data-ttu-id="969d3-119">Ihre Implementierung von **xlAutoRegister** sollte eine Suche ohne Groß-/Kleinschreibung durch die internen Listen ihrer XLL mit den Funktionen und Befehlen durchführen, die exportiert werden, um nach einer Übereinstimmung mit dem übergebenen Namen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="969d3-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="969d3-120">Wenn die Funktion oder der Befehl gefunden wird, sollte **xlAutoRegister** versuchen, sie mithilfe der **xlfRegister-Funktion** zu registrieren, und stellen Sie sicher, dass die Zeichenfolge, die Excel den Rückgabe- und Argumenttypen der Funktion sowie alle anderen erforderlichen Informationen über die Funktion ans lichte.</span><span class="sxs-lookup"><span data-stu-id="969d3-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="969d3-121">Sie sollte dann zu Excel zurück, unabhängig davon, welcher Aufruf von **xlfRegister** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="969d3-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="969d3-122">Wenn die Funktion erfolgreich registriert wurde, gibt **xlfRegister** einen **xltypeNum-Wert** zurück, der die Register-ID der Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="969d3-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="969d3-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="969d3-123">Example</span></span>

<span data-ttu-id="969d3-124">Eine  `SAMPLES\EXAMPLE\EXAMPLE.C` Beispielimplementierung dieser Funktion finden Sie in der Datei.</span><span class="sxs-lookup"><span data-stu-id="969d3-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="969d3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="969d3-125">See also</span></span>



[<span data-ttu-id="969d3-126">REGISTRIEREN</span><span class="sxs-lookup"><span data-stu-id="969d3-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="969d3-127">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="969d3-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

