---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- xlautoregister-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303948"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="392bd-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="392bd-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="392bd-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="392bd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="392bd-106">Excel Ruft die [xlAutoRegister-Funktion](xlautoregister-xlautoregister12.md) immer dann auf, wenn ein Aufruf an das XML-Funktions **Register**oder die äquivalente [XLFREGISTER-Funktion](xlfregister-form-1.md)der C-API erfolgt, wobei die Rückgabe-und Argumenttypen der registrierten Funktion fehlen.</span><span class="sxs-lookup"><span data-stu-id="392bd-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="392bd-107">Es ermöglicht der XLL, die internen Listen der exportierten Funktionen und Befehle zu durchsuchen, um die Funktion mit dem angegebenen Argument und den zurückgegebenen Rückgabetypen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="392bd-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="392bd-108">Ab Excel 2007 ruft Excel die **xlAutoRegister12** -Funktion bevorzugt für die **xlAutoRegister** -Funktion auf, wenn Sie von der XLL exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="392bd-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="392bd-109">Excel erfordert keine XLL zum Implementieren und Exportieren einer dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="392bd-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="392bd-110">Wenn **xlAutoRegister**/ **xlAutoRegister12** versucht, die Funktion ohne Angabe des Arguments und der Rückgabetypen zu registrieren, tritt eine rekursive Aufruf Schleife auf, die schließlich die Aufrufliste überschreitet und Excel abstürzt.</span><span class="sxs-lookup"><span data-stu-id="392bd-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="392bd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="392bd-111">Parameters</span></span>

 <span data-ttu-id="392bd-112">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="392bd-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="392bd-113">Der Name der XLL-Funktion, die registriert wird.</span><span class="sxs-lookup"><span data-stu-id="392bd-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="392bd-114">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="392bd-114">Property value/Return value</span></span>

<span data-ttu-id="392bd-115">Die Funktion sollte das Ergebnis des Versuchs zurückgeben, die XLL-Funktion _pxName_ mithilfe der **xlfRegister** -Funktion zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="392bd-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="392bd-116">Wenn es sich bei der angegebenen Funktion nicht um einen Export der XLL handelt, sollte Sie die #VALUE zurückgeben **!**</span><span class="sxs-lookup"><span data-stu-id="392bd-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="392bd-117">Fehler oder **null** , die Excel bei **#VALUE!** interpretiert.</span><span class="sxs-lookup"><span data-stu-id="392bd-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="392bd-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="392bd-118">Remarks</span></span>

<span data-ttu-id="392bd-119">Bei der Implementierung von **xlAutoRegister** sollte bei der Suche nach einer Übereinstimmung mit dem übergebenen Namen durch die internen Listen der Funktionen und Befehle, die exportiert werden soll, eine Groß-/Kleinschreibung nicht beachtet werden.</span><span class="sxs-lookup"><span data-stu-id="392bd-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="392bd-120">Wenn die Funktion oder der Befehl gefunden wird, sollte **xlAutoRegister** versuchen, Sie zu registrieren, indem Sie die **xlfRegister** -Funktion verwenden, indem Sie sicherstellen, dass die Zeichenfolge bereitGestellt wird, die Excel die Rückgabe-und Argumenttypen der Funktion sowie alle anderen erforderlichen Informationen zur Funktion.</span><span class="sxs-lookup"><span data-stu-id="392bd-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="392bd-121">Sie sollte dann zu Excel zurückkehren, unabhängig vom Aufruf von **xlfRegister** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="392bd-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="392bd-122">Wenn die Funktion erfolgreich registriert wurde, gibt **xlfRegister** einen **xltypeNum** -Wert zurück, der die Register-ID der Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="392bd-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="392bd-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="392bd-123">Example</span></span>

<span data-ttu-id="392bd-124">Eine Beispielimplementierung `SAMPLES\EXAMPLE\EXAMPLE.C` dieser Funktion finden Sie in der Datei.</span><span class="sxs-lookup"><span data-stu-id="392bd-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="392bd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="392bd-125">See also</span></span>



[<span data-ttu-id="392bd-126">Registrieren</span><span class="sxs-lookup"><span data-stu-id="392bd-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="392bd-127">Registrierung</span><span class="sxs-lookup"><span data-stu-id="392bd-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

