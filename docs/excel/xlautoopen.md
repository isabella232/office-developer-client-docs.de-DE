---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- xlAutoOpen-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406647"
---
# <a name="xlautoopen"></a><span data-ttu-id="62734-104">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="62734-104">xlAutoOpen</span></span>

 <span data-ttu-id="62734-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="62734-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="62734-106">Rückruffunktion, die von jeder gültigen XLL implementiert und exportiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="62734-106">Callback function that must be implemented and exported by every valid XLL.</span></span> <span data-ttu-id="62734-107">Die **xlAutoOpen** -Funktion wird empfohlen, um die XLL-Funktionen und-Befehle zu registrieren, Datenstrukturen zu initialisieren, die Benutzeroberfläche anzupassen usw.</span><span class="sxs-lookup"><span data-stu-id="62734-107">The **xlAutoOpen** function is the recommended place from where to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a><span data-ttu-id="62734-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="62734-108">Parameters</span></span>

<span data-ttu-id="62734-109">Diese Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="62734-109">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="62734-110">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62734-110">Property value/Return value</span></span>

<span data-ttu-id="62734-111">Die Implementierung dieser Funktion muss 1 zurückgeben (**Int**).</span><span class="sxs-lookup"><span data-stu-id="62734-111">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="62734-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="62734-112">Remarks</span></span>

<span data-ttu-id="62734-113">Microsoft Excel ruft **xlAutoOpen** auf, wenn die XLL aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="62734-113">Microsoft Excel calls **xlAutoOpen** whenever the XLL is activated.</span></span> <span data-ttu-id="62734-114">Die XLL wird in den folgenden Situationen aktiviert:</span><span class="sxs-lookup"><span data-stu-id="62734-114">The XLL is activated in the following situations:</span></span> 
  
- <span data-ttu-id="62734-115">Am Anfang einer Excel-Sitzung, wenn Sie in der letzten Excel-Sitzung aktiv war, die normal beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="62734-115">At the start of an Excel session if it was active in the last Excel session that ended normally.</span></span>
    
- <span data-ttu-id="62734-116">Wenn es während einer Excel-Sitzung geladen wird.</span><span class="sxs-lookup"><span data-stu-id="62734-116">If loaded during an Excel session.</span></span>
    
- <span data-ttu-id="62734-117">Eine XLL kann auf verschiedene Arten geladen werden:</span><span class="sxs-lookup"><span data-stu-id="62734-117">An XLL can be loaded in several ways:</span></span>
    
- <span data-ttu-id="62734-118">Durch Auswählen von **Öffnen** im Menü **Datei** (wobei die Version von Excel diese Methode zum Laden von XLLs unterstützt).</span><span class="sxs-lookup"><span data-stu-id="62734-118">By choosing **Open** on the **File** menu (where the version of Excel supports this method of loading XLLs).</span></span> 
    
- <span data-ttu-id="62734-119">Verwenden des Add-In-Managers.</span><span class="sxs-lookup"><span data-stu-id="62734-119">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="62734-120">Von einer anderen XLL, die [xlfRegister](xlfregister-form-1.md) mit dem Namen dieser DLL als das einzige Argument aufruft.</span><span class="sxs-lookup"><span data-stu-id="62734-120">From another XLL that calls [xlfRegister](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="62734-121">Aus einem XML-Makroblatt, das [Register](xlfregister-form-1.md) mit dem Namen dieser DLL als einziges Argument aufruft.</span><span class="sxs-lookup"><span data-stu-id="62734-121">From an XLM macro sheet that calls [REGISTER](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="62734-122">Wenn das Add-in während einer Excel-Sitzung deaktiviert und reaktiviert wird, wird diese Funktion bei der Reaktivierung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="62734-122">If the add-in is deactivated and reactivated during an Excel session, this function is called on reactivation.</span></span>
    
### <a name="example"></a><span data-ttu-id="62734-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="62734-123">Example</span></span>

<span data-ttu-id="62734-124">Sehen Sie sich `SAMPLES\EXAMPLE\EXAMPLE.C` die `SAMPLES\GENERIC\GENERIC.C`Dateien und, und zum Beispielimplementierungen dieser Funktion an.</span><span class="sxs-lookup"><span data-stu-id="62734-124">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C`, and for example implementations of this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="62734-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62734-125">See also</span></span>



[<span data-ttu-id="62734-126">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="62734-126">xlAutoClose</span></span>](xlautoclose.md)
  
[<span data-ttu-id="62734-127">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="62734-127">xlAutoRegister/xlAutoRegister12</span></span>](xlautoregister-xlautoregister12.md)


[<span data-ttu-id="62734-128">Add-In-Manager und XLL-Benutzeroberflächenfunktionen</span><span class="sxs-lookup"><span data-stu-id="62734-128">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

