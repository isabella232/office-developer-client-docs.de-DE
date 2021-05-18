---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- xlautoopen-Funktion [excel 2007]
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
# <a name="xlautoopen"></a><span data-ttu-id="26efa-104">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="26efa-104">xlAutoOpen</span></span>

 <span data-ttu-id="26efa-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="26efa-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="26efa-106">Rückruffunktion, die von jeder gültigen XLL implementiert und exportiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="26efa-106">Callback function that must be implemented and exported by every valid XLL.</span></span> <span data-ttu-id="26efa-107">Die **xlAutoOpen-Funktion** ist der empfohlene Ort zum Registrieren von XLL-Funktionen und -Befehlen, Initialisieren von Datenstrukturen, Anpassen der Benutzeroberfläche und so weiter.</span><span class="sxs-lookup"><span data-stu-id="26efa-107">The **xlAutoOpen** function is the recommended place from where to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a><span data-ttu-id="26efa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="26efa-108">Parameters</span></span>

<span data-ttu-id="26efa-109">Diese Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="26efa-109">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="26efa-110">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26efa-110">Property value/Return value</span></span>

<span data-ttu-id="26efa-111">Die Implementierung dieser Funktion muss 1 zurückgeben (**Int**).</span><span class="sxs-lookup"><span data-stu-id="26efa-111">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26efa-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="26efa-112">Remarks</span></span>

<span data-ttu-id="26efa-113">Microsoft Excel **aufruft xlAutoOpen,** wenn die XLL aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="26efa-113">Microsoft Excel calls **xlAutoOpen** whenever the XLL is activated.</span></span> <span data-ttu-id="26efa-114">Die XLL wird in den folgenden Situationen aktiviert:</span><span class="sxs-lookup"><span data-stu-id="26efa-114">The XLL is activated in the following situations:</span></span> 
  
- <span data-ttu-id="26efa-115">Zu Beginn einer Excel sitzung, wenn sie in der letzten Sitzung aktiv Excel, die normal beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="26efa-115">At the start of an Excel session if it was active in the last Excel session that ended normally.</span></span>
    
- <span data-ttu-id="26efa-116">Wird während einer Sitzung Excel geladen.</span><span class="sxs-lookup"><span data-stu-id="26efa-116">If loaded during an Excel session.</span></span>
    
- <span data-ttu-id="26efa-117">Eine XLL kann auf verschiedene Weise geladen werden:</span><span class="sxs-lookup"><span data-stu-id="26efa-117">An XLL can be loaded in several ways:</span></span>
    
- <span data-ttu-id="26efa-118">Durch Auswählen **von Öffnen** im Menü **Datei** (wobei die Version von Excel diese Methode zum Laden von XLLs unterstützt).</span><span class="sxs-lookup"><span data-stu-id="26efa-118">By choosing **Open** on the **File** menu (where the version of Excel supports this method of loading XLLs).</span></span> 
    
- <span data-ttu-id="26efa-119">Verwenden des Add-In-Managers.</span><span class="sxs-lookup"><span data-stu-id="26efa-119">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="26efa-120">Von einer anderen XLL, die [xlfRegister mit](xlfregister-form-1.md) dem Namen dieser DLL als einziges Argument aufruft.</span><span class="sxs-lookup"><span data-stu-id="26efa-120">From another XLL that calls [xlfRegister](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="26efa-121">Aus einem XLM-Makroblatt, das [REGISTER](xlfregister-form-1.md) mit dem Namen dieser DLL als einziges Argument aufruft.</span><span class="sxs-lookup"><span data-stu-id="26efa-121">From an XLM macro sheet that calls [REGISTER](xlfregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="26efa-122">Wenn das Add-In während einer Excel deaktiviert und reaktiviert wird, wird diese Funktion zur Reaktivierung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="26efa-122">If the add-in is deactivated and reactivated during an Excel session, this function is called on reactivation.</span></span>
    
### <a name="example"></a><span data-ttu-id="26efa-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="26efa-123">Example</span></span>

<span data-ttu-id="26efa-124">Sehen Sie sich  `SAMPLES\EXAMPLE\EXAMPLE.C` die Dateien und , und beispielsweise  `SAMPLES\GENERIC\GENERIC.C` Implementierungen dieser Funktion an.</span><span class="sxs-lookup"><span data-stu-id="26efa-124">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C`, and for example implementations of this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="26efa-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26efa-125">See also</span></span>



[<span data-ttu-id="26efa-126">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="26efa-126">xlAutoClose</span></span>](xlautoclose.md)
  
[<span data-ttu-id="26efa-127">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="26efa-127">xlAutoRegister/xlAutoRegister12</span></span>](xlautoregister-xlautoregister12.md)


[<span data-ttu-id="26efa-128">Add-In-Manager und XLL-Benutzeroberflächenfunktionen</span><span class="sxs-lookup"><span data-stu-id="26efa-128">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

