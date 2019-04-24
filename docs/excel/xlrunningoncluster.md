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
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f5c630c73899b07e2727a7d42b18eb1891797bab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310101"
---
# <a name="xlrunningoncluster"></a><span data-ttu-id="a3a41-104">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="a3a41-104">xlRunningOnCluster</span></span>

<span data-ttu-id="a3a41-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a3a41-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a3a41-106">Gibt einen Wert zurück, der angibt, ob die benutzerdefinierte Funktion in einem Cluster läuft.</span><span class="sxs-lookup"><span data-stu-id="a3a41-106">Returns a value that indicates whether the user-defined function is running on a cluster.</span></span> 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="a3a41-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3a41-107">Parameters</span></span>

<span data-ttu-id="a3a41-108">Diese Funktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="a3a41-108">This function has no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="a3a41-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3a41-109">Return value</span></span>

<span data-ttu-id="a3a41-110">Wenn die Funktion in einem Excel-Prozess ausgeführt wird, gibt 0 in einem **XLOPER12** vom Typ **xlTypeInt**zurück.</span><span class="sxs-lookup"><span data-stu-id="a3a41-110">If the function is running in an Excel process, returns 0 in an **XLOPER12** of type **xlTypeInt**.</span></span> <span data-ttu-id="a3a41-111">Wenn die Funktion in einem Cluster läuft, wird der Rückgabetyp und der Wert vom Cluster-Connector-Anbieter bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a3a41-111">If the function is running on a cluster, the return type and value is determined by the cluster connector provider.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="a3a41-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3a41-112">Requirements</span></span>

<span data-ttu-id="a3a41-113">Diese Funktion ist in der Headerdatei xlcall. h definiert.</span><span class="sxs-lookup"><span data-stu-id="a3a41-113">This function is defined in the Xlcall.h header file.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a3a41-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3a41-114">See also</span></span>

- [<span data-ttu-id="a3a41-115">Clustersichere Funktionen</span><span class="sxs-lookup"><span data-stu-id="a3a41-115">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
- [<span data-ttu-id="a3a41-116">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen</span><span class="sxs-lookup"><span data-stu-id="a3a41-116">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

