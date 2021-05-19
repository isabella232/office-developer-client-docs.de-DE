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
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt einen Wert zurück, der angibt, ob die benutzerdefinierte Funktion auf einem Cluster ausgeführt wird. 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="return-value"></a>Rückgabewert

Wenn die Funktion in einem Excel ausgeführt wird, wird 0 in einem **XLOPER12** vom Typ **xlTypeInt zurückgegeben.** Wenn die Funktion auf einem Cluster ausgeführt wird, wird der Rückgabetyp und -wert vom Clusterconnectoranbieter bestimmt.
  
## <a name="requirements"></a>Anforderungen

Diese Funktion wird in der Xlcall.h-Headerdatei definiert.
  
## <a name="see-also"></a>Siehe auch

- [Clustersichere Funktionen](cluster-safe-functions.md)
- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

