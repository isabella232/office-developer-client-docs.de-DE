---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- fdialog-Funktion [excel 2007],fDialog12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58d0df500c38534ec1315d2dab1517c1f5272ad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431526"
---
# <a name="fdialogfdialog12"></a>fDialog/fDialog12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für einen benutzerdefinierten Befehl, der veranschaulicht, wie eine Microsoft Excel UDD (benutzerdefiniertes Dialogfeld) in einer DLL mithilfe der Dialogfeldfunktionen in der C-API erstellt wird. Wenn GENERIC.xll geladen wird, wird ein benutzerdefiniertes Menü, Generic, erstellt, über das auf diesen Befehl zugegriffen wird.
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a>Parameter

Die Funktion nimmt keine Parameter an.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt immer 1 zurück.
  
### <a name="example"></a>Beispiel

Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

