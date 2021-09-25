---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- xlrunningoncluster
ms.localizationpriority: medium
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a5c8a231a1b3dbb7288999f0ac782a89c2b6a943
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576611"
---
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt einen Wert zurück, der angibt, ob die benutzerdefinierte Funktion auf einem Cluster ausgeführt wird. 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="return-value"></a>Rückgabewert

Wenn die Funktion in einem Excel Prozess ausgeführt wird, wird 0 in einem **XLOPER12** vom Typ **xlTypeInt** zurückgegeben. Wenn die Funktion auf einem Cluster ausgeführt wird, werden der Rückgabetyp und der Wert vom Clusterconnectoranbieter bestimmt.
  
## <a name="requirements"></a>Anforderungen

Diese Funktion ist in der Headerdatei Xlcall.h definiert.
  
## <a name="see-also"></a>Siehe auch

- [Clustersichere Funktionen](cluster-safe-functions.md)
- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

