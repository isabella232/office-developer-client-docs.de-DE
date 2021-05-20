---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fexit-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429915"
---
# <a name="fexit"></a><span data-ttu-id="f63a6-104">fExit</span><span class="sxs-lookup"><span data-stu-id="f63a6-104">fExit</span></span>

 <span data-ttu-id="f63a6-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f63a6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f63a6-106">Beispiel für benutzerdefinierten Befehl, der GENERIC.xll auslädt.</span><span class="sxs-lookup"><span data-stu-id="f63a6-106">Example user-defined command that unloads GENERIC.xll.</span></span> <span data-ttu-id="f63a6-107">Wenn GENERIC.xll geladen wird, wird ein benutzerdefiniertes Menü, Generic, erstellt, über das auf diesen Befehl zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="f63a6-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="f63a6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f63a6-108">Parameters</span></span>

<span data-ttu-id="f63a6-109">Die Funktion nimmt keine Parameter an.</span><span class="sxs-lookup"><span data-stu-id="f63a6-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f63a6-110">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f63a6-110">Property value/Return value</span></span>

<span data-ttu-id="f63a6-111">Die Funktion gibt immer 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="f63a6-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f63a6-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f63a6-112">Remarks</span></span>

<span data-ttu-id="f63a6-113">Dies ist eine vom Benutzer initiierte Routine zum Beenden von GENERIC.xll Sie sollten vermeiden, einfach  `UNREGISTER("GENERIC.XLL")` in dieser Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f63a6-113">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function.</span></span> <span data-ttu-id="f63a6-114">Dadurch würde die Registrierung aller Funktionen in dieser DLL auch dann aufgehoben, wenn sie an einem anderen Ort registriert sind.</span><span class="sxs-lookup"><span data-stu-id="f63a6-114">This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else.</span></span> <span data-ttu-id="f63a6-115">Aufheben sie stattdessen die Registrierung der Funktionen nach und nach.</span><span class="sxs-lookup"><span data-stu-id="f63a6-115">Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="f63a6-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f63a6-116">Example</span></span>

<span data-ttu-id="f63a6-117">Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="f63a6-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f63a6-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f63a6-118">See also</span></span>



[<span data-ttu-id="f63a6-119">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="f63a6-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

