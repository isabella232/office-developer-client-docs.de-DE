---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- Fexit-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3abb5cd68a45fbcd16665dbc4d492d764bbd315e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790493"
---
# <a name="fexit"></a><span data-ttu-id="7957d-104">fExit</span><span class="sxs-lookup"><span data-stu-id="7957d-104">fExit</span></span>

 <span data-ttu-id="7957d-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7957d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7957d-106">Beispiel benutzerdefinierter Befehl, der GENERIC.xll entladen wird.</span><span class="sxs-lookup"><span data-stu-id="7957d-106">Example user-defined command that unloads GENERIC.xll.</span></span> <span data-ttu-id="7957d-107">Wenn GENERIC.xll geladen wird, erstellt es ein Menü benutzerdefinierte allgemeine, über die auf diesen Befehl zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="7957d-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="7957d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7957d-108">Parameters</span></span>

<span data-ttu-id="7957d-109">Die Funktion akzeptiert keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7957d-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="7957d-110">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7957d-110">Property value/Return value</span></span>

<span data-ttu-id="7957d-111">Die Funktion gibt immer 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="7957d-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7957d-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7957d-112">Remarks</span></span>

<span data-ttu-id="7957d-113">Dies ist eine vom Benutzer initiierte Routine GENERIC.xll beenden, sollten Sie einfach aufrufen `UNREGISTER("GENERIC.XLL")` in dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="7957d-113">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function.</span></span> <span data-ttu-id="7957d-114">Dies würde erzwingen alle Funktionen in diese DLL aufgehoben, selbst wenn sie an einer beliebigen Stelle else registriert sind.</span><span class="sxs-lookup"><span data-stu-id="7957d-114">This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else.</span></span> <span data-ttu-id="7957d-115">Stattdessen Registrierung aufgehoben werden Sie die Funktionen eines zu einem Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="7957d-115">Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="7957d-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7957d-116">Example</span></span>

<span data-ttu-id="7957d-117">Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="7957d-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7957d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7957d-118">See also</span></span>



[<span data-ttu-id="7957d-119">Funktionen in der generische DLL</span><span class="sxs-lookup"><span data-stu-id="7957d-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

