---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fexit-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310857"
---
# <a name="fexit"></a><span data-ttu-id="5365c-104">fExit</span><span class="sxs-lookup"><span data-stu-id="5365c-104">fExit</span></span>

 <span data-ttu-id="5365c-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5365c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5365c-106">Beispiel für einen benutzerdefinierten Befehl, der generische. XLL entlädt.</span><span class="sxs-lookup"><span data-stu-id="5365c-106">Example user-defined command that unloads GENERIC.xll.</span></span> <span data-ttu-id="5365c-107">Wenn GENERIC. XLL geladen wird, wird ein benutzerdefiniertes Menü generisch erstellt, über das auf diesen Befehl zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="5365c-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="5365c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5365c-108">Parameters</span></span>

<span data-ttu-id="5365c-109">Die Funktion verwendet keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5365c-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="5365c-110">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5365c-110">Property value/Return value</span></span>

<span data-ttu-id="5365c-111">Die Funktion gibt immer 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="5365c-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5365c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5365c-112">Remarks</span></span>

<span data-ttu-id="5365c-113">Hierbei handelt es sich um eine vom Benutzer initiierte Routine zum Beenden von GENERIC. XLL `UNREGISTER("GENERIC.XLL")` .</span><span class="sxs-lookup"><span data-stu-id="5365c-113">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function.</span></span> <span data-ttu-id="5365c-114">Dadurch werden die Registrierung aller Funktionen in dieser DLL erzwungen, auch wenn Sie an einer anderen Stelle registriert sind.</span><span class="sxs-lookup"><span data-stu-id="5365c-114">This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else.</span></span> <span data-ttu-id="5365c-115">Heben Sie die Registrierung der Funktionen stattdessen einzeln auf.</span><span class="sxs-lookup"><span data-stu-id="5365c-115">Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="5365c-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5365c-116">Example</span></span>

<span data-ttu-id="5365c-117">Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="5365c-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5365c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5365c-118">See also</span></span>



[<span data-ttu-id="5365c-119">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="5365c-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

