---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- xlrunningoncluster
localization_priority: Normal
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f42ccbeb94e1fc6b6cf880f1b32ee1bfeb24997e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790632"
---
# <a name="xlrunningoncluster"></a><span data-ttu-id="b95f6-104">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="b95f6-104">xlRunningOnCluster</span></span>

<span data-ttu-id="b95f6-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b95f6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b95f6-106">Gibt einen Wert, der angibt, ob die benutzerdefinierte Funktion in einem Cluster ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b95f6-106">Returns a value that indicates whether the user-defined function is running on a cluster.</span></span> 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="b95f6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b95f6-107">Parameters</span></span>

<span data-ttu-id="b95f6-108">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="b95f6-108">This function has no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="b95f6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b95f6-109">Return value</span></span>

<span data-ttu-id="b95f6-110">Wenn die Funktion in einer Excel-Prozess ausgeführt wird, zurückgegeben in eine **XLOPER12** des Typs **vom Typ XlTypeInt**0.</span><span class="sxs-lookup"><span data-stu-id="b95f6-110">If the function is running in an Excel process, returns 0 in an **XLOPER12** of type **xlTypeInt**.</span></span> <span data-ttu-id="b95f6-111">Wenn die Funktion in einem Cluster ausgeführt wird, wird der Rückgabetyp und der Wert von Cluster-Connector-Anbieter bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b95f6-111">If the function is running on a cluster, the return type and value is determined by the cluster connector provider.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="b95f6-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b95f6-112">Requirements</span></span>

<span data-ttu-id="b95f6-113">Diese Funktion ist in der Headerdatei Xlcall.h definiert.</span><span class="sxs-lookup"><span data-stu-id="b95f6-113">This function is defined in the Xlcall.h header file.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b95f6-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b95f6-114">See also</span></span>

- [<span data-ttu-id="b95f6-115">Clustersichere Funktionen</span><span class="sxs-lookup"><span data-stu-id="b95f6-115">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
- [<span data-ttu-id="b95f6-116">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="b95f6-116">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

