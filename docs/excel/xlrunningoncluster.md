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
ms.openlocfilehash: f5c630c73899b07e2727a7d42b18eb1891797bab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418288"
---
# <a name="xlrunningoncluster"></a><span data-ttu-id="6fe43-104">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="6fe43-104">xlRunningOnCluster</span></span>

<span data-ttu-id="6fe43-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6fe43-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6fe43-106">Gibt einen Wert zurück, der angibt, ob die benutzerdefinierte Funktion auf einem Cluster ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fe43-106">Returns a value that indicates whether the user-defined function is running on a cluster.</span></span> 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="6fe43-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fe43-107">Parameters</span></span>

<span data-ttu-id="6fe43-108">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="6fe43-108">This function has no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6fe43-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6fe43-109">Return value</span></span>

<span data-ttu-id="6fe43-110">Wenn die Funktion in einem Excel ausgeführt wird, wird 0 in einem **XLOPER12** vom Typ **xlTypeInt zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="6fe43-110">If the function is running in an Excel process, returns 0 in an **XLOPER12** of type **xlTypeInt**.</span></span> <span data-ttu-id="6fe43-111">Wenn die Funktion auf einem Cluster ausgeführt wird, wird der Rückgabetyp und -wert vom Clusterconnectoranbieter bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6fe43-111">If the function is running on a cluster, the return type and value is determined by the cluster connector provider.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="6fe43-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fe43-112">Requirements</span></span>

<span data-ttu-id="6fe43-113">Diese Funktion wird in der Xlcall.h-Headerdatei definiert.</span><span class="sxs-lookup"><span data-stu-id="6fe43-113">This function is defined in the Xlcall.h header file.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6fe43-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fe43-114">See also</span></span>

- [<span data-ttu-id="6fe43-115">Clustersichere Funktionen</span><span class="sxs-lookup"><span data-stu-id="6fe43-115">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
- [<span data-ttu-id="6fe43-116">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="6fe43-116">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

