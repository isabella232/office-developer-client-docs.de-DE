---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- XlAutoOpen-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: bf64841cbd75e25443abe5cfc7d3d7419757e245
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790580"
---
# <a name="xlautoopen"></a><span data-ttu-id="37304-104">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="37304-104">xlAutoOpen</span></span>

 <span data-ttu-id="37304-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="37304-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="37304-106">Callback-Funktion, die implementiert und von jedem gültigen XLL exportiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="37304-106">Callback function that must be implemented and exported by every valid XLL.</span></span> <span data-ttu-id="37304-107">Die **XlAutoOpen** -Funktion ist der empfohlene Ausgangspunkt woher Register XLL-Funktionen und Befehle, Initialisieren von Datenstrukturen, Anpassen der Benutzeroberfläche und so weiter.</span><span class="sxs-lookup"><span data-stu-id="37304-107">The **xlAutoOpen** function is the recommended place from where to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a><span data-ttu-id="37304-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="37304-108">Parameters</span></span>

<span data-ttu-id="37304-109">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="37304-109">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="37304-110">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37304-110">Property value/Return value</span></span>

<span data-ttu-id="37304-111">Die Implementierung dieser Funktion muss 1 (**Int**) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="37304-111">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37304-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="37304-112">Remarks</span></span>

<span data-ttu-id="37304-113">Microsoft Excel **XlAutoOpen** aufgerufen, wenn die XLL aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="37304-113">Microsoft Excel calls **xlAutoOpen** whenever the XLL is activated.</span></span> <span data-ttu-id="37304-114">Die XLL wird in den folgenden Situationen aktiviert:</span><span class="sxs-lookup"><span data-stu-id="37304-114">The XLL is activated in the following situations:</span></span> 
  
- <span data-ttu-id="37304-115">Am Anfang einer Excel-Sitzung, wenn es in der letzten Excel-Sitzung aktiv war, die normalerweise beendet.</span><span class="sxs-lookup"><span data-stu-id="37304-115">At the start of an Excel session if it was active in the last Excel session that ended normally.</span></span>
    
- <span data-ttu-id="37304-116">Wenn während einer Sitzung Excel geladen.</span><span class="sxs-lookup"><span data-stu-id="37304-116">If loaded during an Excel session.</span></span>
    
- <span data-ttu-id="37304-117">Eine XLL kann auf verschiedene Weise geladen werden:</span><span class="sxs-lookup"><span data-stu-id="37304-117">An XLL can be loaded in several ways:</span></span>
    
- <span data-ttu-id="37304-118">Wählen Sie **Öffnen** im Menü **Datei** (wobei die Version von Excel diese Methode des Ladens XLLs unterstützt).</span><span class="sxs-lookup"><span data-stu-id="37304-118">By choosing **Open** on the **File** menu (where the version of Excel supports this method of loading XLLs).</span></span> 
    
- <span data-ttu-id="37304-119">Verwenden Sie den Add-In-Manager.</span><span class="sxs-lookup"><span data-stu-id="37304-119">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="37304-120">Aus einer anderen XLL aufruft, [XlfRegister](xlfregister-form-1.md) mit dem Namen dieser DLL als einziges Argument.</span><span class="sxs-lookup"><span data-stu-id="37304-120">From another XLL that calls [xlfRegister](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="37304-121">Aus einer XLM-Makrovorlage aufruft, [Registrieren](xlfregister-form-1.md) mit dem Namen dieser DLL als einziges Argument.</span><span class="sxs-lookup"><span data-stu-id="37304-121">From an XLM macro sheet that calls [REGISTER](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="37304-122">Wenn das Add-in deaktiviert und während einer Sitzung Excel erneut aktiviert ist, wird diese Funktion für eine erneute Aktivierung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="37304-122">If the add-in is deactivated and reactivated during an Excel session, this function is called on reactivation.</span></span>
    
### <a name="example"></a><span data-ttu-id="37304-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="37304-123">Example</span></span>

<span data-ttu-id="37304-124">Finden Sie die Dateien `SAMPLES\EXAMPLE\EXAMPLE.C` und `SAMPLES\GENERIC\GENERIC.C`, beispielsweise die Implementierung dieser Funktion und.</span><span class="sxs-lookup"><span data-stu-id="37304-124">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C`, and for example implementations of this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="37304-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37304-125">See also</span></span>



[<span data-ttu-id="37304-126">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="37304-126">xlAutoClose</span></span>](xlautoclose.md)
  
[<span data-ttu-id="37304-127">XlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="37304-127">xlAutoRegister/xlAutoRegister12</span></span>](xlautoregister-xlautoregister12.md)


[<span data-ttu-id="37304-128">Add-In-Manager und Funktionen von XLL-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="37304-128">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

