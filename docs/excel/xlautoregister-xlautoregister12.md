---
title: XlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- Xlautoregister-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e6430a54b0c0ed3b6e08d3c9256cae7dcde926ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19790584"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="90886-104">XlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="90886-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="90886-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="90886-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="90886-106">Excel Ruft die [XlAutoRegister-Funktion](xlautoregister-xlautoregister12.md) , wenn ein Anruf an XLM-Funktion **Registrieren**, oder die C-API entsprechende [XlfRegister-Funktion](xlfregister-form-1.md), mit dem Zurückgeben und -Argument der Funktion registrierende fehlenden vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="90886-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="90886-107">Es ermöglicht die XLL zum Suchen der internen Liste der exportierten Funktionen und Befehle aus, um die Funktion mit dem Argument registrieren und Rückgabetypen angegeben.</span><span class="sxs-lookup"><span data-stu-id="90886-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="90886-108">Ab Excel 2007, ruft Excel die Funktion **xlAutoRegister12** anstelle der **XlAutoRegister** -Funktion aus, wenn es von der XLL exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="90886-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="90886-109">Excel erforderlich keine XLL zu implementieren und exportieren Sie eine dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="90886-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="90886-110">Wenn **XlAutoRegister**/ **xlAutoRegister12** die Funktion ohne das Argument registrieren und Rückgabetypen versucht, eine rekursive aufrufende Schleife tritt auf, die schließlich überschreitet die Aufrufliste und stürzt Excel.</span><span class="sxs-lookup"><span data-stu-id="90886-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="90886-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="90886-111">Parameters</span></span>

 <span data-ttu-id="90886-112">_pxName_ (**XltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="90886-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="90886-113">Der Name der XLL-Funktion, die registriert wird.</span><span class="sxs-lookup"><span data-stu-id="90886-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="90886-114">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90886-114">Property value/Return value</span></span>

<span data-ttu-id="90886-115">Die Funktion sollte das Ergebnis der Versuch zum Registrieren von XLL-Funktion _PxName_ mithilfe der **XlfRegister** -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="90886-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="90886-116">Wenn die angegebene Funktion nicht von der XLL-Exporten ist, sollte Zurückgeben der **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="90886-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="90886-117">Fehler oder **NULL** interpretiert Excel am **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="90886-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="90886-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90886-118">Remarks</span></span>

<span data-ttu-id="90886-119">Die Implementierung von **XlAutoRegister** sollte eine Groß-/Kleinschreibung unterschieden Suche durchsehen Ihrer XLL interne von Funktionen und Befehle, dass er eine Übereinstimmung mit dem Namen übergebenen Nachrichtensymbol exportiert ausführen.</span><span class="sxs-lookup"><span data-stu-id="90886-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="90886-120">Wenn die Funktion oder den Befehl gefunden werden kann, sollten **XlAutoRegister** versuchen, registrieren, mit der **XlfRegister** -Funktion, wie die Zeichenfolge bereitstellen, auf denen Excel die Return und das Argument Typen von der Funktion als auch andere erforderliche angewiesen wird sichergestellt werden kann Informationen über die Funktion.</span><span class="sxs-lookup"><span data-stu-id="90886-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="90886-121">Dann sollte nach Excel zurückgeben was beim Aufruf von **XlfRegister** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="90886-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="90886-122">Wenn die Funktion erfolgreich registriert wurde, gibt **XlfRegister** einen **XltypeNum** -Wert, der mit der ID registrieren der Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="90886-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="90886-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="90886-123">Example</span></span>

<span data-ttu-id="90886-124">Finden Sie in der Datei `SAMPLES\EXAMPLE\EXAMPLE.C` für eine Beispiel-Implementierung dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="90886-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="90886-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90886-125">See also</span></span>



[<span data-ttu-id="90886-126">REGISTRIEREN</span><span class="sxs-lookup"><span data-stu-id="90886-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="90886-127">AUFHEBEN DER REGISTRIERUNG</span><span class="sxs-lookup"><span data-stu-id="90886-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

