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
ms.openlocfilehash: f42ccbeb94e1fc6b6cf880f1b32ee1bfeb24997e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790632"
---
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt einen Wert, der angibt, ob die benutzerdefinierte Funktion in einem Cluster ausgeführt wird. 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="return-value"></a>R�ckgabewert

Wenn die Funktion in einer Excel-Prozess ausgeführt wird, zurückgegeben in eine **XLOPER12** des Typs **vom Typ XlTypeInt**0. Wenn die Funktion in einem Cluster ausgeführt wird, wird der Rückgabetyp und der Wert von Cluster-Connector-Anbieter bestimmt.
  
## <a name="requirements"></a>Anforderungen

Diese Funktion ist in der Headerdatei Xlcall.h definiert.
  
## <a name="see-also"></a>Siehe auch

- [Clustersichere Funktionen](cluster-safe-functions.md)
- [C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

